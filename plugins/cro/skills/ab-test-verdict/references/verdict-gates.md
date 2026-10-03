# Verdict gates

The gates run in this order. A result that fails gate 1 at the Invalid level prints no effect at all.

## Gate 1. Traffic split (sample ratio mismatch, SRM)

Chi-square goodness of fit of the visitors per arm against the planned shares (any split, any number of arms; degrees of freedom = arms − 1):

```
expected_i = total × planned share_i
χ² = Σ (observed_i − expected_i)² / expected_i
```

| p-value | Level | What happens |
|---|---|---|
| below 0.0005 | **Invalid** | The effect is not read. Find the cause, fix it, rerun. |
| 0.0005 to below 0.01 | **Warning** | The effect is shown, but the verdict is capped at Inconclusive until the cause is found. |
| 0.01 or above | pass | Continue. |

Sources: an article by the Microsoft Research Experimentation Platform team on diagnosing SRM (https://www.microsoft.com/en-us/research/articles/diagnosing-sample-ratio-mismatch-in-a-b-testing/, read 2026-10-03) uses p < 0.0005 as its conservative bar and reports that about 6% of A/B tests analysed at Microsoft had an SRM; it builds on Fabijan et al., KDD 2019, pp. 2156–2164. A Statsig blog guide to SRM (https://www.statsig.com/blog/sample-ratio-mismatch, read 2026-10-03) treats p below 0.01 as unbalanced. Two levels keep the strict bar for throwing a test away while still flagging the grey zone. Checking the split every day raises the chance of a false alarm, which is another reason 0.01 only warns.

Worked checks: 50,000 vs 51,200 on 50/50 → χ² = 14.23, p = 0.00016 → Invalid. 10,000 vs 10,400 on 50/50 → χ² = 7.84, p = 0.0051 → Warning. 10,000 vs 10,150 → χ² = 1.12, p = 0.29 → pass.

Where to look, by stage:
- Assignment: bucketing bug, a variant that crashes or redirects, bots or internal traffic in one arm.
- Execution: the variant loads slower so fewer visitors are logged; a redirect drops tracking; caching serves one arm.
- Log processing: filtering or deduplication that removes more visitors from one arm.
- Analysis: the wrong start date, a segment applied to one arm, visitors counted after triggering in only one arm.

## Gate 2. Unit

The unit of randomisation must equal the unit of analysis. Randomised by user but analysed by session or pageview → flag: "variance is understated; ask your platform for a user-level or delta-method analysis". Unfixable → Invalid.

## Gate 3. Run length and stopping

- Planned n per arm reached? If not, print the share reached.
- Whole weeks? If not, flag weekday imbalance.
- Stopped early when the p-value first dipped below 0.05, with no sequential method chosen in advance → "this p-value is not valid at face value"; the verdict is capped at Inconclusive. Evan Miller (2010-04-18, https://www.evanmiller.org/how-not-to-run-an-ab-test.html, read 2026-10-03) simulated a test with a 50% baseline and no real effect, stopped at the first significant look or after 150 observations, and found 26.1% false positives instead of 5%. That is his worst case, with a look after every observation; fewer looks inflate less, but any unplanned stop inflates.
- Variant or tracking changed mid-test → flag; read only the period after the change if it is long enough, else Inconclusive.

## Gate 4. Novelty

With daily or weekly counts, compare the first week with the rest. A lift that is clearly present in week 1 and absent later is flagged as novelty: "the early effect may fade; read the later weeks".

## Gate 5. Too good to be true (Twyman flag)

A relative lift larger than 3 × the smallest lift worth having, or larger than 50% when no plan exists → "check tracking and the split before believing it". Kohavi, Tang & Xu (2020, chapter 3, "Twyman's Law") make the point that a striking result more often signals a data error than a discovery. The thresholds here are heuristics of this plugin.

## Effect table

| Arm | Visitors | Conversions | Rate [Wilson 95%] |
|---|---|---|---|

Then: absolute difference with its Newcombe 95% interval; relative lift with its log-ratio interval; pooled two-sided p-value (formulas in `rates-and-intervals.md`). For a continuous metric given as mean, SD and n per arm: difference of means with a Welch interval (mean difference ± 1.96 × √(sd_A²/n_A + sd_B²/n_B)).

Wording rules:
- Never "there is a 95% chance B is better". A p-value is the probability of data this extreme if there were no difference (ASA statement, Wasserstein & Lazar 2016, The American Statistician 70(2)).
- A platform's "chance to beat control" or "probability of being the top arm" depends on that platform's prior and model. Explain it in one line; do not recompute it and do not treat it as the chance of being right.

## False-positive risk

Only when the result is significant. With π = the share of the user's past tested ideas that really won:

```
FPR = (α/2)·(1 − π) ÷ [ (α/2)·(1 − π) + power·π ]
```

If π is unknown, print three rows: π = 10% → 22.0%; π = 20% → 11.1%; π = one third → 5.9%. Source: Kohavi, Deng & Vermeer, "A/B Testing Intuition Busters", KDD 2022, Table 2 (read 2026-10-03), which also lists 8% → 26.4% for one company's search tests. Meaning: these figures describe the procedure, not this result. Over many tests whose ideas win at rate π, about this share of the results that reach p < 0.05 are false wins. They are never the probability that this particular result is false, and a result with a p far below 0.05 carries less risk than these rows.

## Several arms or metrics (Holm)

More than two arms, or several declared primary metrics: Holm's step-down (Holm 1979, Scandinavian Journal of Statistics 6(2)). Sort the m p-values from smallest; compare the i-th smallest with α ÷ (m − i + 1); stop at the first that fails; everything after it fails too.

Example: A 600/20,000; B 690/20,000; C 640/20,050. B vs A p = 0.011 against 0.025 → passes; C vs A p = 0.27 against 0.05 → fails. B is significant after correction, C is not.

Second example: 4 arms × 5 metrics = 15 comparisons, smallest p = 0.03 → compared with 0.05 ÷ 15 = 0.0033 → fails; nothing is significant.

Segments and metrics not declared before the test are exploratory: Holm-adjusted and labelled "a hypothesis for the next test, not a decision". Up to two pre-declared segments are shown with intervals.

## Guardrails

A guardrail (revenue per visitor, refunds, lead quality, error rate, page speed) whose interval excludes 0 in the harmful direction blocks Ship.

## Decision rule, applied in order

The same text is written into the plan before launch.

1. **Invalid — rerun:** split p below 0.0005, or a unit mismatch that cannot be fixed.
2. **Don't ship:** the interval for B − A lies entirely below 0 (a real loss: "learn what moved it"), or a guardrail is breached.
3. **Ship:** the interval lies entirely above 0 and guardrails hold. If its upper end is below the smallest lift worth having, add "the effect is real but smaller than the lift you said was worthwhile". If only its lower end is below that lift, add "it may be smaller than worthwhile". Compare in the same unit: the relative (log-ratio) interval with a relative lift worth having, or the percentage-point interval with that lift converted to points at the control rate (10% of 3.0% = 0.30 pp).
4. **Inconclusive:** everything else. Print the range still plausible and the n per arm that the observed rate and the smallest lift worth having would need. A split Warning, an early stop or a mid-test change caps the verdict here.

"Inconclusive" is a result, not a failure: the test ruled out effects outside the interval, that is gains above its upper end and losses below its lower end.

## What you can claim

One sentence that matches the verdict, for example: "B raised signups by between 0.08 and 0.52 percentage points on desktop and mobile traffic in the four weeks tested." No extrapolation to other pages, periods or traffic.

## Learning-log entry

| Field | Content |
|---|---|
| Test | name, page or step, dates (whole weeks) |
| Hypothesis | barrier → change → expected behaviour |
| Primary metric, smallest lift worth having | |
| n per arm, split check | |
| Effect | difference and interval; relative lift and interval |
| Guardrails | |
| Verdict | Invalid / Don't ship / Ship / Inconclusive |
| What we now believe | one line |
| Next step | |

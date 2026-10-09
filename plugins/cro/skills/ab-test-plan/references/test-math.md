# Test math

All sizing in this plugin uses the normal approximation for two independent proportions. Defaults: α = 0.05 two-sided, power = 0.80 (z = 1.95996 and 0.84162). The user may change either; print the values used. Results are per arm, rounded up to whole visitors.

## Inputs to collect

| Input | Notes |
|---|---|
| Baseline rate p₁ | With its numerator, denominator and period. A rate with no denominator is used but labelled "n not given". |
| Smallest lift worth having | Relative (e.g. 10%) or absolute (e.g. 0.3 pp). This is a business threshold — the smallest change that would be worth shipping — not a forecast of what the change will do. |
| Weekly eligible visitors | Only visitors who reach the changed element (the trigger point). Sitewide visits overstate traffic when the change sits on one step. |
| Arms and split | Default two arms, 50/50. |
| Metric type | Conversion (yes/no per visitor) or a continuous metric such as revenue per visitor. |

## Two proportions

```
p₂ = p₁ × (1 + relative lift)        p̄ = (p₁ + p₂) / 2
n per arm = [ z₁₋α/₂ · √(2·p̄·(1−p̄)) + z₁₋β · √(p₁(1−p₁) + p₂(1−p₂)) ]² ÷ (p₂ − p₁)²
```

Source: the standard two-sample proportion formula without continuity correction; every worked figure below was recomputed for this build. Cross-check: n ≈ 16·σ²/δ² with σ² = p(1−p) gives nearly the same figure (Kohavi, Tang & Xu, *Trustworthy Online Controlled Experiments*, Cambridge University Press 2020; Evan Miller, 2010-04-18, https://www.evanmiller.org/how-not-to-run-an-ab-test.html, read 2026-10-03, prints the same rule of thumb).

Worked checks (each computed, rounded up):

| Baseline | Lift worth having | n per arm |
|---|---|---|
| 3.0% | 10% relative (3.0 → 3.3%) | 53,211 |
| 1.1% | 20% relative (1.1 → 1.32%) | 38,769 |
| 5.0% | 10% relative | 31,234 |
| 10.0% | 50% relative | 686 |
| 1.0% | 10% relative | 163,095 |

## Duration

```
weeks = ceil( arms × n per arm ÷ weekly eligible visitors ), minimum 1
```

Always whole weeks, so each weekday appears equally often in both arms. A test that would end mid-week is extended to the end of that week. Example: 2 × 53,211 ÷ 6,000 = 17.7 → 18 weeks.

## Affordable lift

Invert the formula: for a fixed number of weeks, n per arm = weeks × weekly eligible ÷ arms; find the smallest p₂ whose n does not exceed it. Print it for 2, 4 and 8 weeks, each lift rounded **up** to one decimal (a rounded-down lift understates what the test needs). Example at 3.0% and 6,000 a week: 31.2% relative at 2 weeks, 21.7% at 4 weeks (3.0 → 3.65%), 15.1% at 8 weeks.

## Feasibility verdict (heuristic of this plugin, editable)

| Weeks needed | Verdict |
|---|---|
| 1–4 | **Run** |
| 5–8 | **Run only with** one of: the full number of weeks computed (print it) if the decision can wait that long, a bolder change, a higher-traffic step, or a metric closer to the change (keep the final metric as a guardrail) |
| more than 8 | **Do not A/B test this lift.** Fix now if it is a clarity fix or a bug; otherwise research first; or pool pages that share one template into one test |

The same 2, 4 and 8 weeks are used in the affordable-lift table, so the two always agree.

## More than two arms (A/B/n)

At planning, divide α by the number of comparisons with control (k − 1), a Bonferroni split; at the verdict, Holm is used (the A/B test verdict skill). Example: three arms at 3.0 → 3.3% use α = 0.025 → 64,439 per arm (four arms, α = 0.05 ÷ 3 ≈ 0.0167 → 70,974 per arm), against 53,211 for a plain A/B. More arms cost traffic; they do not find winners faster.

## Unequal split

With share w in the variant and 1 − w in control, the total sample needed grows by a factor of 0.25 ÷ (w(1 − w)) compared with 50/50 (normal approximation). 90/10 → 2.78× the total. The split check at the end uses the planned shares, not 50/50.

## "Ship if not worse" (non-inferiority)

For clean-up changes (removing a field, simplifying a step) where the question is whether the rate drops by more than a margin m the user accepts:

```
n per arm = (z₁₋α + z₁₋β)² · 2·p·(1−p) ÷ m²        one-sided α = 0.05
```

Example: 3.0% baseline, margin 0.3 pp → 39,981 per arm. The decision: ship when the lower bound of the 90% interval for B − A (equivalently the one-sided 95% bound) lies above −m.

## Continuous metric (revenue per visitor, order value)

```
n per arm = 2 · (z₁₋α/₂ + z₁₋β)² · σ² ÷ δ²   ≈ 16·σ²/δ² at the defaults
```

σ is the per-visitor standard deviation from the user's own data, zeros for non-buyers included. Example: σ = 40, δ = 2 → 6,280 per arm. Without σ: "cannot size this metric; paste the per-visitor standard deviation of the metric for a recent period". Ratio metrics randomised by user but counted per session (for example revenue per session) need a delta-method or user-level analysis; ask the testing platform for it.

## Trigger point

Count only visitors who could see the change. A change on the payment step is sized on visitors who reach payment, not on all visitors. Analysing everyone dilutes the effect; analysing only visitors who reached the trigger point in both arms keeps it, as long as control counts the visitors who would have seen the change at the same point (Kohavi, Tang & Xu 2020, chapter on triggering).

## Stopping rule (write before launch)

- Fixed horizon: read once, at the planned n and whole weeks.
- Early looks are valid only under a method chosen before launch: the testing platform's sequential or always-valid mode (Johari, Pekelis & Walsh, always-valid p-values, https://arxiv.org/abs/1512.04922, read 2026-10-03), or Evan Miller's simple sequential test (2015-10-13, https://www.evanmiller.org/sequential-ab-testing.html, read 2026-10-03): with a planned N conversions in total, stop and declare the treatment the winner if treatment conversions minus control conversions reach 2√N; stop with no winner when the total reaches N. That is one-sided; his two-sided version uses about 2.25√N in either direction. N comes from his calculator or the platform, not from this plugin.
- An A/A test first when the tool or the set-up is new.

# Test math

Rates, intervals, sample size and the threshold read. Every rate is printed as `k/n = p% [low% – high%]`.

## Wilson score interval (95%)

For k successes out of n, p = k ÷ n and z = 1.96:

```
centre = (p + z²/(2n)) / (1 + z²/n)
half   = z × sqrt( p(1 − p)/n + z²/(4n²) ) / (1 + z²/n)
interval = [centre − half, centre + half]
```

Source: E. B. Wilson (1927), "Probable inference, the law of succession, and statistical inference", Journal of the American Statistical Association 22(158): 209–212. It stays inside 0–100% and behaves sensibly at small n, unlike p ± 1.96 standard errors.

Worked checks (check the arithmetic against these):

| k / n | rate | 95% interval |
|---|---|---|
| 0 / 120 | 0.0% | 0.0% – 3.1% |
| 5 / 18 | 27.8% | 12.5% – 50.9% |
| 2 / 5 | 40.0% | 11.8% – 76.9% |
| 61 / 1,900 | 3.2% | 2.5% – 4.1% |
| 4 / 61 | 6.6% | 2.6% – 15.7% |

## Labels (heuristics of this plugin)

- **Thin sample**: n below 20.
- **Few events**: fewer than 5 successes.
- A labelled rate is shown with its interval but never decides scale or stop on its own, and two labelled rates are never ranked against each other. Decisions rest on the interval against the line, not on the point value.
- n = 0: print "no data", not 0%.

## Zero successes

Print the Wilson upper bound. Cross-check with the rule of three: with zero events in n, the 95% upper bound is close to 3 ÷ n (Hanley and Lippman-Hand, "If nothing goes wrong, is everything all right?", JAMA 249(13), 1983). For 0/120: 3 ÷ 120 = 2.5%, Wilson upper 3.1%. With n of 20 or more, zero successes may support "stop" when the upper bound is below the rate the pass line needs; that is the one case a "few events" result can decide.

## Sample size to estimate a rate

To estimate a rate p within ± d at 95%:

```
n ≈ 1.96² × p × (1 − p) ÷ d²
```

p is the user's guess or a labelled assumption. Worked check: p = 3%, d = 2 points: 3.8416 × 0.03 × 0.97 ÷ 0.0004 = 279.5, so 280 people.

## Threshold read

When the n above is larger than the reach available, or expected events (reach × p) are fewer than 5, the test cannot estimate the rate. It can still answer "did at least k happen?". Say so in the card:

- Pass if at least k of N, within the time box. k comes from the user's goal or from the affordability line (spend ÷ affordable per customer, rounded up). With neither, use the expected count at the assumed rate, rounded down, marked "change me".
- Stop at 0 or 1 event, whichever the user prefers; mark it.
- Offer the three ways to make the rate readable: more reach, a longer window, or measuring an earlier step that happens more often.

## Decision against a pre-set line

| Situation | Decision |
|---|---|
| Lower bound of the interval at or above the pass line, no label | scale |
| Upper bound below the stop line (or below the pass line when no stop line was set), no label | stop |
| Zero successes, n of 20 or more, upper bound below the rate the pass line needs | stop (the one labelled case) |
| No pre-set line; zero successes, n of 20 or more | stop (provisional), stated against the upper bound ("the rate is at most X%"); inconclusive instead if the user names a worthwhile rate at or below the upper bound; no worthwhile rate is assumed; scale is never called on provisional lines |
| A threshold count met or missed as written on the card | as the card says |
| The interval spans the line, or a label applies | inconclusive: name the next read point |
| Missed, but one named change could plausibly fix the converter or the offer | iterate once, with the change and a new line written before the rerun |

Lines written after the data was seen are "provisional" and are proposed for the next round only.

## Cost lines

Cost per signup = spend ÷ signups; cost per customer = spend ÷ customers. The range: spend ÷ (n × each end of the interval). The click ceiling with observed rates = affordable per signup × observed visit-to-signup rate. Worked check: a $4.76 per-signup line, $420 spent, 61 signups from 1,900 clicks: cost per signup $6.89, and $5.39 even at the interval's upper bound (4.1%), so the line is missed; click ceiling 4.76 × 61 ÷ 1,900 = $0.15 against an actual $0.22 per click.

Kohavi, Tang and Xu, *Trustworthy Online Controlled Experiments* (2020), is the background for setting criteria before the data arrive and for not reading underpowered tests as answers.

## Minimum run time (heuristics of this plugin)

- At least one full weekly cycle before any read, because weekdays and weekends differ.
- Two weekly cycles when the channel's delivery system needs a learning period.
- Subscription payback is read after at least one quarter.

## Extending an inconclusive test

Find the reach that clears every label at the observed rates, and take the larger:
- "thin sample" on a step: reach needed = 20 ÷ (that step's n ÷ reach so far);
- "few events" on the last step: reach needed = 5 ÷ (successes ÷ reach so far).

Worked check: 18 stores reached, 5 trials, 2 paying. Twenty trials need 20 ÷ (5 ÷ 18) = 72 stores; five paying need 5 ÷ (2 ÷ 18) = 45 stores. Read again at 72 stores.

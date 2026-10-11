# Rates and intervals

Show count rates as k/n and dollar ratios with monetary numerator, denominator and unit. Historical closed-only rates describe that cohort; current-deal calibration requires a compatible target cohort and definition version. Add sampling intervals only for a stated inferential target and an appropriate trial/dependence model. Wilson 95% is the default for suitable binary trials; accept requested confidence levels. Do not automatically attach intervals to complete-cohort ledgers or saved-period frequencies. Show requested metric inputs and arithmetic; print interval derivations only when asked.

## Wilson score interval

For k successes out of n trials, p = k / n and z = 1.96:

```
centre = (p + z²/(2n)) / (1 + z²/n)
half   = z × sqrt( p(1−p)/n + z²/(4n²) ) / (1 + z²/n)
interval = [centre − half, centre + half]
```

Source: E. B. Wilson (1927), "Probable inference, the law of succession, and statistical inference", Journal of the American Statistical Association 22(158): 209–212. It behaves well for small n and for rates near 0% or 100%, where the plain "p ± 1.96 × standard error" range can go below 0 or above 100.

Worked check: 14 of 50 → 28.0% [17.5% – 41.7%].

## Reading intervals

- A stated value outside the interval: "stated X% is outside the observed range".
- Comparing two separate groups (different sources, segments or cohorts, with no record in both): compute the interval for the difference (below). If it excludes 0, say the difference shows at this sample size; if it includes 0, say "this check does not show a difference". Overlapping single-rate intervals alone do not mean the gap is noise.
- Small n: keep the row and distinguish the exact observed difference from uncertain generalisation. There is no universal n = 20 significance threshold. Use a dependence-appropriate difference interval only for justified inference; the independent-proportions method below requires independent groups.
- n = 0: print "no data", not 0%.
- A rate the user gives without a denominator: print "n not given" instead of an interval.

## Interval for a difference of two rates

Newcombe's hybrid score method, built from the two Wilson intervals. With p1 [l1, u1] and p2 [l2, u2], d = p1 − p2:

```
low  = d − sqrt( (p1 − l1)² + (u2 − p2)² )
high = d + sqrt( (u1 − p1)² + (p2 − l2)² )
```

Source: R. G. Newcombe (1998), "Interval estimation for the difference between independent proportions: comparison of eleven methods", Statistics in Medicine 17(8): 873–890. Worked check: 18/30 = 60.0% [42.3% – 75.4%] vs 8/30 = 26.7% [14.2% – 44.4%] → difference 33.3 pp [8.3 pp – 53.2 pp]. The single intervals overlap, yet the interval for the difference excludes 0.

## Dollar-weighted rates

A dollar-weighted win rate is won amount ÷ closed amount (won + lost) on the same pipeline definition. Print it next to the count rate when both are possible, and say which one each downstream number uses. An interval is printed for the count rate only; for the dollar rate print the count n it rests on.

## Medians

Durations (days in stage, days to first contact, cycle length) use the median, with n. Print a requested or decision-relevant mean with its label, alongside the median when useful. <delete>

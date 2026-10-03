# Statistics glossary

One set of definitions for every skill in this plugin. z = 1.96 throughout.

## Rate with a Wilson 95% interval

Printed as `k / n = p%  [low% – high%]`. With p = k / n:

```
centre = (p + z²/(2n)) / (1 + z²/n)
half   = z × sqrt( p(1−p)/n + z²/(4n²) ) / (1 + z²/n)
interval = [centre − half, centre + half]
```

Check: 90 of 360 → 25.0% [20.8% – 29.7%].
Source: E. B. Wilson (1927), Journal of the American Statistical Association 22(158): 209–212.

## Difference of two rates with a Newcombe 95% interval

For two independent groups, d = p1 − p2. Take the Wilson interval of each rate, (l1, u1) and (l2, u2):

```
lower = d − sqrt( (p1 − l1)² + (u2 − p2)² )
upper = d + sqrt( (u1 − p1)² + (p2 − l2)² )
```

Reading: if the interval contains 0, write "effect not established"; otherwise "effect shown, between X and Y points". Never decide by checking whether two separate intervals overlap.
Check: 54 of 360 against 4 of 40 → +5.0 points [−8.5, +12.3], effect not established. 20 of 50 against 40 of 450 → +31.1 points [+18.4, +45.1], effect shown.
Source: R. G. Newcombe (1998), "Interval estimation for the difference between independent proportions", Statistics in Medicine 17: 873–890 (method 10).

## Signal measures

| Term | Formula |
|---|---|
| Rate if fired | cancelled among accounts where the signal fired ÷ accounts where it fired |
| Rate if not fired | cancelled among the rest ÷ the rest |
| Lift | rate if fired ÷ rate if not fired (a relative risk). Print the overall cancel rate beside it |
| Recall (coverage) | cancellers the signal fired for ÷ all cancellers |
| Precision | cancellers among fired ÷ fired (equals rate if fired) |
| Lead time | median days from the first firing to the cancel request, with n |

Lift gets no interval of its own; the decision uses the Newcombe interval of the difference.

## Save measures (save-offer economics)

| Term | Formula |
|---|---|
| Naive save | accepted ÷ shown the offer |
| Retained | paying full price in the first billing cycle after the discount ends ÷ everyone shown the offer (accepted or not) |
| Holdout retained | paying in the same cycle ÷ holdout members (shown no offer) |
| Incremental | retained − holdout retained, with the Newcombe interval |
| Net save | an accepter who pays full price in the first billing cycle after the discount or pause ends |

## Sample size for two groups

People per group to detect a change from p1 to p2, two-sided α = 0.05, power 0.8 (both editable):

```
p̄ = (p1 + p2) / 2
n = ( 1.96 × sqrt(2 p̄ (1−p̄)) + 0.8416 × sqrt(p1(1−p1) + p2(1−p2)) )² / (p1 − p2)²
```

Round up. Check: 10% → 15% gives 685.6, so 686 per group.

## Other rules

- Mix shares (what fraction of declines are of each type) are shown as counts and percentages with no interval.
- n = 0: print "no data", not 0%.
- n below 20: keep the row, add "thin sample" (heuristic).
- Durations: median with n; the mean only if asked, beside the median.
- Rounding: compare with any threshold first, then round half away from zero.

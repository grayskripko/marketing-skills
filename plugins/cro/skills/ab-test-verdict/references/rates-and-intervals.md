# Rates and intervals

Every rate is printed as `k / n = p% [low% – high%]`, a Wilson 95% interval, with z = 1.96.

## Wilson score interval

For k conversions out of n visitors, p = k / n:

```
centre = (p + z²/(2n)) / (1 + z²/n)
half   = z × √( p(1−p)/n + z²/(4n²) ) / (1 + z²/n)
interval = [centre − half, centre + half]
```

Source: E. B. Wilson (1927), Journal of the American Statistical Association 22(158): 209–212. It stays inside 0–100% and behaves at small n and at rates near 0, where "p ± 1.96 × standard error" does not.

Worked check: 840 of 2,400 → 35.0% [33.1% – 36.9%].

## Difference between two groups (Newcombe)

Newcombe's hybrid score interval (method 10 in R. G. Newcombe 1998, Statistics in Medicine 17(8): 873–890), built from the two Wilson intervals. For group B with pB [lB, uB] and group A with pA [lA, uA], d = pB − pA:

```
low  = d − √( (pB − lB)² + (uA − pA)² )
high = d + √( (uB − pB)² + (pA − lA)² )
```

Worked check: desktop 572/1,100 = 52.0% vs mobile 840/2,400 = 35.0% → +17.0 pp [+13.5 pp – +20.5 pp].

Reading it: if the interval excludes 0, the gap shows at this sample size; if it includes 0, write "this check does not show a difference". Two single-rate intervals that overlap do not by themselves mean the gap is noise; use the interval for the difference.

## Relative lift

Relative lift = pB / pA − 1. Its interval is computed on the log of the ratio (the Katz method):

```
se = √( 1/kB − 1/nB + 1/kA − 1/nA )
interval = (pB/pA) × exp(± 1.96 × se) − 1
```

Worked check: A 300/10,000, B 345/10,150 → +13.3% [−2.7% – +31.9%]. Never divide the Newcombe bounds by the control rate to get a relative interval; that ignores the control's own uncertainty and understates the width.

## Two-proportion z-test

Pooled p = (kA + kB) / (nA + nB); z = (pB − pA) / √( p(1−p)(1/nA + 1/nB) ); two-sided p-value from the normal distribution. The p-value is reported next to the interval, never instead of it.

## Thin samples and edge cases

- n below 20: "thin sample" (heuristic of this plugin). Shown, never declared different from another group.
- n = 0: "no data", not 0%.
- A rate given without its denominator: "n not given", no interval.

## Rounding

Compare with thresholds before rounding. Rates one decimal (two below 1%), differences in percentage points two decimals below 1 pp and one decimal otherwise, p-values two significant figures (below 0.0001 print "< 0.0001"). Visitors and weeks rounded up. Round half away from zero.

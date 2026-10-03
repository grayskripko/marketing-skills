# Rates and intervals

## Wilson 95% interval for k successes out of n

z = 1.96, p = k/n.
centre = (p + z²/(2n)) / (1 + z²/n)
half-width = z × sqrt(p(1-p)/n + z²/(4n²)) / (1 + z²/n)
interval = centre ± half-width, clipped to 0–100%.

Print as "k/n = p% (low–high%)". Examples: 48/300 = 16.0% (12.3–20.6%); 7/12 = 58.3% (32.0–80.7%), thin sample.

## Newcombe 95% interval for a difference p1 − p2

Take the Wilson limits (l1, u1) and (l2, u2) of each group.
lower = (p1 − p2) − sqrt((p1 − l1)² + (u2 − p2)²)
upper = (p1 − p2) + sqrt((u1 − p1)² + (p2 − l2)²)
Print in percentage points. If the interval includes 0, say "no clear difference in this data".
Example: 42/84 against 6/36 is 33.3 pp (14.9–47.0).

## Rules

- Never judge a difference by whether two intervals overlap; print the difference interval.
- Compare with thresholds before rounding; print one decimal; round half away from zero.
- n under 20: print the row, add "thin sample" (heuristic of this plugin), and do not call it different from another group.
- A difference between groups is an association. Write "association, not proof" and name one plausible other cause (for example, clearer first posts may attract both replies and returns).
- Durations: median and 75th percentile, with n. No means for durations.
- A rate the user gives without a denominator is marked "n not given" and gets no interval.

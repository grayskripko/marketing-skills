# Rates, intervals and rounding

## Share across conversations

k = conversations where the item appears, n = conversations read. Share = k ÷ n, one decimal.

## Wilson 95% interval for k of n

With p = k ÷ n and z = 1.96:

- centre = (p + z² ÷ (2n)) ÷ (1 + z² ÷ n)
- half-width = z × √(p(1 − p) ÷ n + z² ÷ (4n²)) ÷ (1 + z² ÷ n)
- interval = centre ± half-width, clipped to 0% and 100%.

Worked example: k = 11, n = 30. p = 0.3667; z² = 3.8416; 1 + z² ÷ n = 1.1281; centre = (0.3667 + 0.0640) ÷ 1.1281 = 0.3818; half-width = 1.96 × √(0.007741 + 0.001067) ÷ 1.1281 = 0.1631; interval 21.9% to 54.5%.

Print it at any n of 1 or more. The interval is the range of shares consistent with the count; it is not a forecast.

## Labels

- n below 20: "thin sample", a heuristic of this plugin. Shown, never called different from another group.
- k = 1: "n = 1, single mention".
- Two groups are compared only through the interval for their difference, never by whether their two intervals overlap; with thin samples, or groups that share conversations, not at all.

## Rounding

- Compare with any threshold before rounding.
- Percentages: one decimal. Money: whole units. Hours: two decimals at most, as given by the hour model.
- Round half away from zero.
- Keep unrounded values through a chain of calculations; round only when printing.

## Counts that are not shares

Word counts, question counts and turn lengths are exact integers and need no interval. When fewer than 3 calls are compared, print each call's figure; no averages.

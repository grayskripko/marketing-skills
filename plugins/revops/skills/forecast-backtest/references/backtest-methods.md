# Backtest methods and error definitions

## Methods

Each method is applied to what was open at the start of each past period (a snapshot), then compared with what actually closed won in that period.

| Id | Method | Needs |
|---|---|---|
| M1 | Stated probability × amount, summed | stage and amount per deal in each snapshot, stated probability per stage |
| M2 | Historical stage-to-close rate × amount | the same, plus closed history before each period to compute the rates |
| M3 | M2, but deals older than the median age of won deals at that stage use that stage's aged-deal rate: the win rate, with n, of closed deals that sat at that stage longer than that median | deal age in stage |
| M4 | Category rollup: sum of amounts in the categories the user counts (for example commit plus a share of best case) | category per deal and the user's rule |

If the user pastes each method's past forecast directly, use those numbers and skip the rebuild.

## Errors

For each period t with actual A_t and forecast F_t:

```
signed error  e_t = (F_t − A_t) ÷ A_t
absolute      |e_t|
MAPE          = mean of |e_t| over periods with A_t ≠ 0
bias          = mean of e_t over the same periods
```

A period with A_t = 0 has no percentage error. Exclude it from MAPE and bias and list it with the absolute difference F_t − A_t.

## Verdict rules

- A method is "closest" in a period if its |e_t| is the smallest. Compare errors before rounding; if two or more methods have exactly the same |e_t|, each gets half a win (a third for three, and so on).
- Name a closest method overall only if its wins, counting partial wins, are more than half of the usable periods. Otherwise say "no method is consistently closer" and add the lowest MAPE and the lowest absolute bias as separate facts.
- With 4 or fewer usable periods print "n = k periods, weak evidence" (heuristic of this plugin).
- Without at least two past periods for at least two methods, say that a backtest is not possible with this data and stop. Do not produce a number of your own in that case.
- By default the output ends with the verdict. Only when the user asks what each method says for the current period, show one row per method next to that method's past MAPE and bias, headed "what each method would say, not a forecast". Never one blended number.

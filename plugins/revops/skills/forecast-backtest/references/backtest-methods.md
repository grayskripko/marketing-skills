# Backtest methods and error definitions

## Methods

The ids M1–M4 are for this file only; in the answer, use the user's method names or the plain names below.

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

For each pair, dollar error = forecast − actual; positive means overforecast. MAE = mean absolute dollar error; dollar bias = mean signed dollar error. These include zero-actual periods. Percentage error = (forecast − actual) ÷ actual; MAPE and percentage bias use only nonzero-actual periods and report their coverage. Zero actual makes percentages undefined, not dollar errors or closest-period wins. Use requested/business-relevant metrics; do not add unrelated percentage comparisons.

## Verdict rules

- Closest-period wins follow the chosen loss, include zero periods when that loss is defined there, and split exact ties equally before rounding.
- Use the requested loss to name the best method; report frequency wins separately. Majority is necessary only for a majority claim.
- Four or fewer periods is a default caution. Assess representative history, horizon, dependence, seasonal/regime coverage and advantage stability; five periods does not establish adequacy.
- Evaluate errors for every available forecast/actual pair. One method supports absolute evaluation; at least two comparable methods are needed for relative comparison. Label a single-period comparison a postmortem; reserve consistency claims for sufficiently representative repeated history. Missing actuals block only affected pairs.
- Lead with the requested verdict. Only when the user asks what each method says for the current period, show one row per method next to that method's past MAPE and bias, headed "what each method would say, not a forecast". Never one blended number.

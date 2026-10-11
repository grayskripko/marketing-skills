# ARR bridge definitions

These are the definitions this plugin uses by default. If the user's company defines a term differently, use theirs and say so.

## Period and cohort

- Name the period in every header: one month, one quarter, or a trailing twelve months.
- Starting cohort = accounts with revenue above zero at the start of the period.
- Revenue can be MRR or ARR; keep the user's unit and say which. ARR = MRR × 12 only if the user asks for the conversion.

## Movements, per account, start to end of the period

| Movement | Rule |
|---|---|
| New | not in the starting cohort, never had revenue before, has revenue at the end (with no earlier history given, count it as new and say once that it is a reactivation if it paid before) |
| Reactivation | not in the starting cohort, had revenue in an earlier period, has revenue at the end |
| Expansion | in the cohort, end > start |
| Contraction | in the cohort, 0 < end < start |
| Churn | in the cohort, end = 0 |

For a multi-month period, movements compare the start and end values only; an account that expanded and then churned inside the period counts as churn of its starting value. Say this in a note if the monthly detail shows such cases.

## Bridge and reconciliation

```
start + new + reactivation + expansion − contraction − churn = computed end
reconciliation = reported end − computed end   (must be 0)
```

If reconciliation is not 0, report the gap and affected accounts only when identifiable. Do not allocate unknown adjustments. Calculate requested GRR/NRR provisionally on the classified starting-cohort basis if their inputs are known; withhold final reconciliation sign-off and state the unknown adjustment’s unresolved retention effect. Unknown required inputs or a zero denominator make the affected ratio undefined.

## Retention

```
GRR = (start − contraction − churn) ÷ start        over the starting cohort
NRR = (start + expansion − contraction − churn) ÷ start
```

New and reactivated accounts are outside the starting cohort and appear in neither. GRR cannot exceed 100% under this definition.

Customer-count view, when the user asks for churn, customer counts or a full bridge: starting customers, churned customers, customer-count churn % with k/n; a 95% range only when justified inference is requested, as in `rates-and-intervals.md`.

## Worked check

Monthly, start 100k, new 8k, expansion 5k, contraction 2k, churn 6k → end 105k, GRR 92.0%, NRR 97.0%.

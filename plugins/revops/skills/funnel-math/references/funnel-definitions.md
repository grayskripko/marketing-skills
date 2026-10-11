# Funnel definitions

## Cohorts

Group by when records entered the funnel, using the user's reporting/event cadence (monthly by default), never conversion period. Check every cohort's step-specific follow-up and unresolved outcomes. Mark incompletely observed cohorts; median age is only a quick warning, not proof of maturity. Use comparable fixed-horizon outcomes or an appropriate censoring-aware method when needed. Show k/n and requested duration summaries; intervals follow the rate-evidence rule.

## Cohort table

| Cohort | Entered | Step | Converted | Rate | 95% interval | Median days (n) |
|---|---|---|---|---|---|---|

One row per cohort and available step, crossed with source when periods and sources are requested together. Rates show k of n; intervals follow the rate-evidence rule. Cross response metrics by the same cohort × source, showing requested period changes.

## Time to first contact

- From record creation to the first logged touch, in hours.
- Median with n and target compliance as k/n by the requested source and period; for time-and-source comparisons show cohort × source and cohort totals. Exactly the target counts as within.
- Add 75th percentiles only when requested or useful, using linear interpolation. Intervals follow `rates-and-intervals.md`. If no target is given, show the distribution without inventing one.
- Record ids over the target are listed only if the user asks.
- Faster first contact is associated with better lead outcomes in published research (Oldroyd, McElheran and Elkington, "The Short Life of Online Sales Leads", Harvard Business Review, 2011). Use it only as a reason to measure; never quote its figures as the user's expected gain.

## Segment view

Use available funnel steps by the requested source/segment and cohort. Lead with the finding that answers the question. Describe observed differences with counts; for justified inference use `rates-and-intervals.md`, accounting for dependence and follow-up. Do not require uncollected downstream fields or ban comparison solely because n is small.

## Velocity

```
velocity per day = open opportunities × count win rate × average won size ÷ median cycle days
         or      = open pipeline $ × dollar-weighted win rate ÷ median cycle days
```

State which form was used. Never multiply the dollar-weighted rate by average won size: the size is already inside that rate. Print every input. If any input is missing, velocity goes to "Not checked".

## What this data cannot show

Mention a limitation beside the affected result only when it prevents a material misreading; do not append a generic caveat section. Do not claim causes, rep effort or market changes from these rows.

# Funnel definitions

## Cohorts

Group records by the period they entered the funnel (created month or quarter), not by the period they converted. A cohort's later steps can still be open; say "cohort still maturing" when the newest cohort is younger than the median time to the step being measured.

## Cohort table

| Cohort | Entered | Step | Converted | Rate | 95% interval | Median days (n) |
|---|---|---|---|---|---|---|

One row per cohort and step. Rates with n and interval as in `rates-and-intervals.md`.

## Time to first contact

- From record creation to the first logged touch, in hours.
- Median and 75th percentile by source, with n. Percentiles use linear interpolation between ranks.
- Share over the user's response-time target, with n and interval. If the user gives no target, report the distribution and ask.
- Record ids over the target are listed only if the user asks.
- Faster first contact is associated with better lead outcomes in published research (Oldroyd, McElheran and Elkington, "The Short Life of Online Sales Leads", Harvard Business Review, 2011). Use it only as a reason to measure; never quote its figures as the user's expected gain.

## Segment view

Per segment and per source: opportunities, win rate by count with interval, dollar-weighted win rate, median cycle, average won size. To compare two groups, print the interval for the difference (see `rates-and-intervals.md`); do not decide from whether the two single-rate intervals overlap. Thin-sample rows are shown but not compared. Never lead the output with this table; it follows the cohort table.

## Velocity

```
velocity per day = open opportunities × count win rate × average won size ÷ median cycle days
         or      = open pipeline $ × dollar-weighted win rate ÷ median cycle days
```

State which form was used. Never multiply the dollar-weighted rate by average won size: the size is already inside that rate. Print every input. If any input is missing, velocity goes to "Not checked".

## What this data cannot show

Close the output with this short section: causes, rep effort, market changes, and anything outside the pasted rows.

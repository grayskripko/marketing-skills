# Revenue plan math

## Reverse funnel

Keep unrounded values through the chain; round whole units up only when printing.

```
won deals needed = target ÷ average won deal size
opportunities    = won deals ÷ count win rate
SQLs             = opportunities ÷ SQL-to-opportunity rate
MQLs             = SQLs ÷ MQL-to-SQL rate        (only if given)
```

Which win rate:
- Counts (opportunities, SQLs, MQLs) use the count win rate: won deals ÷ closed deals.
- If only a dollar-weighted rate is given, go through dollars instead: `pipeline $ needed = target ÷ dollar-weighted win rate`, then `opportunities = pipeline $ ÷ average opportunity size`. If average opportunity size is missing, use average won size and print "assumes lost deals were about the size of won ones" in the Assumptions box.
- Never divide a deal count by a dollar-weighted rate.

Worked check: target 600,000, average won deal 18,000, count win rate 22%, SQL-to-opportunity 40% → 33.3 won deals, 151.5 opportunities, 378.8 SQLs; printed as 34, 152, 379.

## Rounding across months

Compute the period total unrounded and round it once. Monthly rows show the unrounded value and a rounded-up column; the rounded-up months may add up to more than the period total, by at most (months − 1). Say so under the table. Worked check: 378.8 SQLs over three months → 126.3 per month, printed 127, 127, 127 (sum 381) against a quarter total of 379.

## Lag

Shift each step back by the median time between steps (or the whole cycle if only that is given). With a 60-day cycle, SQLs for a quarter's closes are needed about two months earlier; show a month-by-month table with the month each count must land in. Use the period labels the user gives; do not add a year.

## Coverage

```
coverage needed = 1 ÷ dollar-weighted win rate    (same pipeline definition)
```

This is a dollar-to-dollar ratio. At a 20% dollar-weighted rate it is 5.0×. Multiples print with one decimal. Print it next to "3× is a common rule of thumb, not a property of your funnel".

## Capacity

Inputs: people carrying a number, start months, ramp months, quota per ramped person, expected attainment (a team-level assumption).

```
month index k = 1 in the month a person starts, 2 the next month, and so on
ramp factor   = min(1, k ÷ ramp months)
ramped equivalents in a month = sum of ramp factors (fully ramped people count 1)
expected bookings = ramped equivalents × monthly quota × attainment
gap = target − expected bookings
pipeline needed for the gap = gap ÷ dollar-weighted win rate
```

Print the ramp factor per person group per month. Team level only; never per person unless the user asks, and then under the people rule.

## Sensitivity grids

Two separate grids, because capacity bookings do not depend on funnel rates:

- Funnel grid: rows are the count win rate −5 pp, as given, +5 pp; columns are the SQL-to-opportunity rate −5 pp, as given, +5 pp; cells show SQLs needed per month.
- Capacity grid: rows are attainment −10 pp, as given, +10 pp; columns are ramp months as given and +1; cells show expected bookings against target.

Mark the base cell in each. All inputs appear in an Assumptions box the user can edit.

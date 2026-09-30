# Calibration table

## Counting rule

For each stage S:

- reached(S) = closed deals whose furthest stage was S or later. If the export has one "furthest stage" column, a deal reached every stage up to it.
- won(S) = deals in reached(S) that closed won.
- observed(S) = won(S) ÷ reached(S), with n = reached(S) and a Wilson 95% interval.
- Deals still open are excluded, because their outcome is not known yet. Count them per stage in a note: "k open deals that reached this stage are not counted."
- If only stage counts are given ("50 reached Stage 3, 14 won"), use them directly and say that censoring could not be checked.

## Output

| Stage | Stated % | Reached (n) | Won | Observed % | 95% interval | Verdict |
|---|---|---|---|---|---|---|
| Stage 3 | 60.0% | 50 | 14 | 28.0% | 17.5% – 41.7% | stated outside interval |

Verdicts: "stated inside interval", "stated outside interval", "thin sample" (n below 20, heuristic), "no data".

Then:

- Adjacent stages whose intervals overlap: "this table does not show that these two stages separate outcomes". The same deals sit in both rows, so no test for a difference is run between them.
- A suggested probability per stage, written as "from your data: 28.0%, n = 50". Never smoothed or blended with outside figures.
- The period the closed deals cover, and whether stage definitions changed inside it (if the user says so, split at that date).

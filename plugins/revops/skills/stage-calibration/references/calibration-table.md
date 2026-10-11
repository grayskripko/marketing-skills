# Calibration table

## Counting rule

For each stage S:

Use actual stage-entry history where available and separate pipeline paths/definition versions. Furthest-stage inference means a deal reached every prior stage only after mandatory sequential traversal is confirmed; otherwise affected exposure denominators are unknown.
- won(S) = deals in reached(S) that closed won.
- observed(S) = won(S) ÷ reached(S), with n = reached(S); add an appropriate interval only under the rate-evidence rule.
- Deals still open are excluded, because their outcome is not known yet. Count them per stage in a note: "k open deals that reached this stage are not counted."
- If only stage counts are given ("50 reached Stage 3, 14 won"), use them directly and say that censoring could not be checked.

## Output

| Stage | Stated | Reached (n) | Won | Observed | 95% range | Verdict |
|---|---|---|---|---|---|---|
| Stage 3 | 60% | 50 | 14 | 28.0% | 17.5% – 41.7% | stated outside range |

The Stated column shows the user's figure exactly as given. Verdicts: "stated inside range", "stated outside range", "no data"; with n below 20 (a heuristic of this plugin), "thin sample; stated inside/outside range", so a thin sample never hides a stated value outside its range.

Then:

- Do not infer overlap from aggregate stage counts or separation from marginal-interval overlap. Confirm the traversal/dependence model; use suitable paired or transition evidence when available.
- A suggested probability per stage, written as "from your data: 28.0%, n = 50". Never smoothed or blended with outside figures.
- The period the closed deals cover, and whether stage definitions changed inside it (if the user says so, split at that date).

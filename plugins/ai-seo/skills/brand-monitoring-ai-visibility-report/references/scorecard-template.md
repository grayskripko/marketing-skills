# Scorecard template

Use only requested sections. Keep engines separate; never add a blended total.

## 1. The answer

One line per engine, for example: "Engine A, unbranded: 21 of 90 runs (23.3%) in 2026-08, 33 of 90 (36.7%) in 2026-09, +13.3 points: observed increase."

## 2. Changes between periods

Per engine: before → after with counts and the point change. Add a threshold column only when the user asked for a threshold.

## 3. Scorecard (unbranded prompts)

| Engine | Period | Mention rate | Citation rate | Share of voice (if asked) | Stability (if asked) | n (runs) |
|---|---|---|---|---|---|---|
| Engine A | 2026-08 | 21/90 (23.3%) | 6/90 (6.7%) | 21/75 (28.0%) | 14/20 (70.0%) | 90 |

Repeat for branded prompts, with a note on any wrong facts recorded in `notes`.

## 4. Lost prompts

Only the lost prompts; the full per-prompt table only on request.

| Engine | Period | Prompt ID | Runs | Runs with any competitor | Runs with the brand |
|---|---|---|---|---|---|

## 5. Cited instead

| Engine | Host | Citations | Brand's own? |
|---|---|---|---|

## 6. Next steps (only when requested)

Route each item in words to a page check, an answer-gap check or the off-site plan, and name the next run date.

## 7. Data quality and calculation table

- Periods, engines, prompts, runs.
- Default thin flag: median repeats below 3; use the matched-cell and unequal-allocation checks when supplied cells differ. State the check used, counts, mixed settings and excluded rows only when present.

| Engine | Period | Group | Runs | Runs with mention | Runs with brand citation | Brand mentions | Competitor mentions | Prompts | Prompts all agreeing |
|---|---|---|---|---|---|---|---|---|---|

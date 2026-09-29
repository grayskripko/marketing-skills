# Scoring rules

## Input columns

The log uses the panel sheet columns: `prompt_id, bucket, branded, phrasing, prompt, engine, run, date, settings, brand_mentioned, brand_position, brand_cited_url, competitors_mentioned, cited_urls, notes`. The minimum needed for scoring is `prompt_id`, `branded`, `engine`, `date` and `brand_mentioned`. Without `brand_cited_url` the citation rate is "not available"; without `competitors_mentioned` share of voice is "not available".

A **run** is one row. A **prompt** is one `prompt_id` plus `phrasing`. A **period** is a calendar month of `date` unless the user names other periods.

## Groups

Compute every metric per engine and per period, and separately for `branded = no` (unbranded) and `branded = yes` (branded). The headline numbers are the unbranded ones, because they show whether the brand comes up when buyers do not name it.

## Metrics

| Metric | Formula | Notes |
|---|---|---|
| Mention rate | runs with `brand_mentioned = yes` ÷ runs | Print as numerator/denominator and percent |
| Citation rate | runs with a non-empty `brand_cited_url` ÷ runs | "Not available" for a surface that shows no sources |
| Share of voice | brand mentions ÷ (brand mentions + competitor mentions) | Each brand counts at most once per run; only the tracked competitors count |
| Stability | prompts where every run has the same `brand_mentioned` value ÷ prompts with at least 2 runs | Low stability means answers vary a lot between runs |
| Average first position | mean of `brand_position` over runs where it is filled | Report with the count of runs it is based on |

Rounding: compare values with thresholds before rounding; print percentages and point changes to one decimal, rounding half away from zero (a change of 6.25 points prints as +6.3).

## Thin sample

An engine-period group is **thin** when the median number of runs per prompt is below 3 (heuristic). Thin groups are scored and shown, but no change involving them is called real.

## Noise rule (heuristic)

Compare the unbranded mention rate of the same engine between two periods. The change is **real** only when all three hold:

1. The absolute change is at least 10 percentage points.
2. Each period has at least 30 unbranded runs for that engine, and neither period is thin.
3. At least 3 `prompt_id`s changed their own mention rate in the same direction as the overall change (both phrasings pooled per `prompt_id`).

Otherwise the change is **within run-to-run variation**. Print the three conditions with their values for every engine. Apply the same rule to citation rate if the user asks.

Why a rule is needed: AI answers change often. Ahrefs observed AI Overview content changing about every 2.15 days on average, with about 45.5% of cited sources new when it changed (ahrefs.com/blog/ai-overview-change/, published 2025-11-11). A single difference between two small samples is often noise. The thresholds above are heuristics, not statistical tests; say so when reporting.

## Lost prompts

An unbranded `prompt_id` is **lost** for an engine and period when the brand is mentioned in none of its runs and more than half of its runs mention at least one tracked competitor. Any tracked competitor counts: count runs that name one or more competitors, not individual competitors. Both phrasings are pooled per `prompt_id`.

Print the per-prompt table before the lost list: engine | period | prompt_id | runs | runs with any competitor | runs with the brand | lost?

## Cited instead

Split `cited_urls` on `;`, reduce each URL to its host without `www.`, and count hosts per engine and period. Show the top 10 with counts and mark the brand's own domain.

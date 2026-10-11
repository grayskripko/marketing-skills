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

## Repetition and uncertainty

Report runs, distinct prompt IDs, allocation, independent observation days and settings where supplied. Median repetitions below 3 may be flagged as below the manual monitoring default, but are not a universal adequacy test. Report observed rates for small groups; do not confuse an observed difference with reliability or causal attribution.

## Optional manual monitoring alert

For a requested comparison where this preset is useful, check an absolute rate change of at least 10 percentage points, at least 30 relevant runs per period with median repetitions of at least 3, and at least 3 prompt IDs moving in the overall direction, pooling phrasings. Print conditions only when using this preset. State "meets" or "does not meet the default monitoring alert," never proven change versus noise. Unknown conditions remain unknown. User goals and measurement design determine practical thresholds and uncertainty analysis.

Retain the cited Ahrefs AI Overview volatility study as background motivating repeat observations, not as a derivation of these thresholds or a guarantee of applicability to other engines. Preserve its original source and date in the background evidence.

Background evidence: Ahrefs observed AI Overview content changing about every 2.15 days on average, with about 45.5% of cited sources new when it changed (ahrefs.com/blog/ai-overview-change/, published 2025-11-11).

## Lost prompts

An unbranded `prompt_id` is **lost** for an engine and period when the brand is mentioned in none of its runs and more than half of its runs mention at least one tracked competitor. Any tracked competitor counts: count runs that name one or more competitors, not individual competitors. Both phrasings are pooled per `prompt_id`.

List only the lost prompts with their counts. Print the full per-prompt table (engine | period | prompt_id | runs | runs with any competitor | runs with the brand | lost?) only if the user asks for it.

## Cited instead

Split `cited_urls` on `;`, reduce each URL to its host without `www.`, and count hosts per engine and period. Show the top 10 with counts and mark the brand's own domain.

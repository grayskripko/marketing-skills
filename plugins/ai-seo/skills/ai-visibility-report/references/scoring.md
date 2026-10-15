# Scoring rules

## Input columns

The log uses the panel sheet columns: `prompt_id, bucket, branded, phrasing, prompt, engine, run, date, settings, brand_mentioned, brand_position, brand_cited_url, competitors_mentioned, cited_urls, notes`. Use the supplied `prompt_id`, `branded` and `brand_mentioned` data with engine and period labels from columns or accompanying context as needed for the requested calculation. Without `brand_cited_url` the citation rate is "not available"; without `competitors_mentioned` share of voice is "not available".

A **run** is one row. A **prompt** is one `prompt_id` plus `phrasing`. Default period: calendar month. Use equal-length windows aligned to supplied change dates when a launch or campaign splits a month; retain comparable settings and prompt coverage, and name the boundaries used.

## Groups

Compute every metric per engine and per period, and separately for `branded = no` (unbranded) and `branded = yes` (branded). The headline numbers are the unbranded ones, because they show whether the brand comes up when buyers do not name it.

## Metrics

| Metric | Formula | Notes |
|---|---|---|
| Mention rate | runs with `brand_mentioned = yes` ÷ runs | Print as numerator/denominator and percent |
| Citation rate | runs with a non-empty `brand_cited_url` ÷ runs | "Not available" for a surface that shows no sources |
| Share of voice | brand mentions ÷ (brand mentions + competitor mentions) | Each brand counts at most once per run; only the tracked competitors count |
| Stability | prompts where every run has the same `brand_mentioned` value ÷ prompts with at least 2 runs | Keep 2 as the mathematical minimum for comparing repeats; with fewer than 2, report stability unavailable, not 100%. State the eligible prompt count. |
| Average first position | mean of `brand_position` over runs where it is filled | Report with the count of runs it is based on |

Rounding: compare values with thresholds before rounding; default display: one decimal, half away from zero; use two decimals if distinct supplied decision-relevant values collide at one decimal, and state the precision. Compare unrounded values.

## Repetition evidence

For change comparisons with uneven repetitions, compare only matched prompt/phrasing cells with comparable allocation and show the minimum and range. Still report observed rates. The numerical repetition gate belongs to the optional monitoring heuristic below; it does not replace the two-run denominator for descriptive stability.

## Noise rule (heuristic, only on request)

Default: a descriptive verdict from observed rates, matched prompt movement, repeatability and settings; none of these establish cause. Compare each engine separately on the same unbranded prompt IDs and phrasings with fixed settings. Never pick observations by their answers, fill in missing runs, or treat changed composition or settings as improvement.

Only when the user asks for a threshold or an alert boundary: this monitoring heuristic calls a change clear at an unrounded change of at least 10 points, at least 30 matched unbranded runs per period, a median of at least 3 repetitions per prompt/phrasing, and at least 3 matched prompt IDs moving in the overall direction. Call it a heuristic, not a significance test; failing it does not prove noise. A validated method the user supplies replaces it.

Why repeats matter: AI answers change often. In its November 2025 study, Ahrefs reported average AI Overview persistence of 2.15 days and average cited-URL overlap of 54.5% between consecutive responses, a historical sample, not a refresh schedule <!-- ahrefs.com/blog/ai-overview-change/, published 2025-11-11 -->. A single difference between two small samples is often noise. The thresholds above are heuristics, not statistical tests; say so when reporting.

## Lost prompts

When the user requests diagnostic classification, an unbranded prompt ID is **lost in this panel** when brand mentions are 0 and strictly more than 50% of its runs name a tracked competitor, pooling matched phrasings. Use **possible gap, insufficient repetition** when it has fewer than 3 repetitions per observed phrasing; retain the observed 0/n and competitor k/n. When the brand appears but competitor appearances outnumber brand appearances, use **competitor-dominated**, not lost. Never infer market absence.

List only the lost prompts with their counts. Print the full per-prompt table (engine | period | prompt_id | runs | runs with any competitor | runs with the brand | lost?) only if the user asks for it.

## Cited instead

Split `cited_urls` on `;`, reduce each URL to its host as written, and count hosts per engine and period. List a `www.` and a bare form separately and say they may be the same site. Default: show the top 10 with counts and mark the brand domain. Use all hosts when there are fewer than 10; include every tie at the tenth count, and show all supplied hosts when the user asks for a complete inventory.

# Scoring rules

## Input columns

The log uses the panel sheet columns: `prompt_id, bucket, branded, phrasing, prompt, engine, run, date, settings, brand_mentioned, brand_position, brand_cited_url, competitors_mentioned, cited_urls, notes`. The minimum needed for scoring is `prompt_id`, `branded`, `engine`, `date` and `brand_mentioned`. Without `brand_cited_url` the citation rate is "not available"; without `competitors_mentioned` share of voice is "not available".

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

## Thin sample

Default: an engine-period group is **thin** when median repetitions per prompt and phrasing are below 3. Use **insufficient repeated evidence** for a change involving such a group; still report every observed rate. When repetitions are uneven, also print the minimum and range and compare only matched prompt/phrasing cells with comparable allocation. State whether the median default or the uneven-allocation check determined the verdict.

## Noise rule (heuristic)

Default to a descriptive verdict from observed rates, matched prompt movement, repeatability and settings; these do not establish intervention causation. Apply the following numerical monitoring heuristic, its gate verdicts and gate-reporting instructions only when the user explicitly asks to apply it, has adopted it for this panel, or asks you to choose an operational alert boundary. Otherwise do not use its gates to qualify an ordinary observed increase. The following matching, allocation, no-fabrication and no-causation safeguards still apply to every comparison. Compare each engine separately on the same unbranded prompt IDs and phrasings, with fixed settings and comparable allocation. Default monitoring rule: **clear change under the monitoring heuristic** requires an unrounded absolute change of at least 10 percentage points, at least 30 matched unbranded runs in each period, median repetitions per prompt/phrasing at least 3 in each period, and at least 3 matched prompt IDs whose own rates move in the overall direction (phrasings pooled within each ID). Print the observed rates, run counts and every gate's measured value after the decisive verdict.

When matching, settings or repetition evidence is missing, report **observed increase/decrease; clear-change conditions unverified**, naming the missing evidence. When runs are below 30, median repetitions below 3, or fewer than 3 matched IDs are available, report **insufficient evidence under the default monitoring rule**, with the observed change and failed counts. For 1-2 matched IDs that meet the effect, volume and repetition gates and all move together, additionally describe **consistent movement in this narrow panel**; this does not pass the default breadth gate. Adequate comparable data that fail the effect or direction gate receive **no clear change under the stated monitoring rule**; failure does not prove noise or no change.

For uneven allocations, show minimum/range of repetitions and use comparable matched-cell allocation; state retained and excluded counts and the deterministic selection rule. Never pick observations by their answers, fabricate missing runs, or treat changed composition/settings as improvement. Retain all valid comparable observations; any separate full-log descriptive rates must identify their different population.

Use an alternative decision boundary only when the user supplies a pre-specified validated analysis and its sampling assumptions hold for these logs; name the method, boundary and adequacy criterion used. Historical no-intervention drift may be shown as context, but do not automatically replace 10 points with the maximum observed historical change or lower it to make a result pass. Apply this comparison to citation rate only when requested. The monitoring heuristic is neither a statistical significance test nor proof that an intervention caused a change.

Why a rule is needed: AI answers change often. Ahrefs observed AI Overview content changing about every 2.15 days on average, with about 45.5% of cited sources new when it changed (ahrefs.com/blog/ai-overview-change/, published 2025-11-11). A single difference between two small samples is often noise. The thresholds above are heuristics, not statistical tests; say so when reporting.

## Lost prompts

Default: an unbranded prompt ID is **lost in this panel** when brand mentions are 0 and strictly more than 50% of its runs name a tracked competitor, pooling matched phrasings. Use **possible gap, insufficient repetition** when it has fewer than 3 repetitions per observed phrasing; retain the observed 0/n and competitor k/n. When the brand appears but competitor appearances outnumber brand appearances, use **competitor-dominated**, not lost. State the label rule used; never infer market absence.

List only the lost prompts with their counts. Print the full per-prompt table (engine | period | prompt_id | runs | runs with any competitor | runs with the brand | lost?) only if the user asks for it.

## Cited instead

Split `cited_urls` on `;`, reduce each URL to its host without `www.`, and count hosts per engine and period. Default: show the top 10 with counts and mark the brand domain. Use all hosts when there are fewer than 10; include every tie at the tenth count, and show all supplied hosts when the user asks for a complete inventory. State the display limit used.

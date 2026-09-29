# Prioritization rules for citation exports

All thresholds here are heuristics; state them in the output and let the user change them.

## Inputs per page

- **Value**: the column the user names, or conversions, then clicks, then sessions.
- **Branded and navigational queries are set aside first.** Exclude every grounding query that contains the brand name (ask for it if it is not clear from the data) or that the export labels Navigational. They are left out of each page's share, the median and the low-share list, and are shown in a separate "branded and navigational" block. A brand's share on its own-name queries is expected to be high and says little about discovery.
- **Citation share**: from the Bing AI Performance export, averaged over the page's remaining grounding queries (simple mean; say so). If only citation counts exist, use citations and say that the rule was applied to counts. Print the citations behind each share next to it; when the pages' citation counts differ by 5 times or more, say so next to the priority list, because a share built on a few citations is less stable.
- **AI-feature impressions**: from the Search Console generative AI report, when present. Used as context, not in the priority rule.

## Calculation table

Print one row per page:

| Page (normalized) | Value | Value rank | Top third by value? | Citation share | Citations behind the share | Median share of the user's cited pages | At or below median? | Priority? |
|---|---|---|---|---|---|---|---|---|

- Value rank: 1 is the highest value. Tied values get the same rank, the smaller number, and the next rank skips (for example 1, 2, 2, 4).
- Top third: rank ≤ ceil(number of pages with a value ÷ 3).
- Median: the median citation share over the user's pages that are cited for at least one grounding query left after the branded and navigational exclusion. With an even count, the mean of the two middle values.
- At or below median: citation share lower than or equal to the median. A page with value but absent from the Bing export has citation share 0 and counts as at or below median; mark it "not cited in the period".
- A page cited only for branded or navigational queries gets no share in this table; list it in the "branded and navigational" block with its value, and do not mark it as a priority.
- Priority: top third by value and at or below median.

Sort the priority list by value rank.

## Action types

| Situation | Action type |
|---|---|
| Priority page, cited for some grounding queries | Strengthen the passages that answer those queries (page check) |
| Priority page, not cited in the period | Check eligibility and quotability first (page check) |
| Low-share grounding query with no page on the site that answers it | Content gap: plan a page or a section |
| Low-share grounding query where a page exists | Answer gap for that query, with pasted answers |

## Re-measure

Set a re-measure date at least 4 weeks after the changes ship and compare periods of equal length.

# Prioritization rules for citation exports

This is an optional prioritization heuristic, not a required ranking. Use the user's method when supplied; otherwise state this convention and its confirmed joined population if used. Keep unknown shares outside the ranking.

## Inputs per page

- **Value**: the column the user names, or conversions, then clicks, then sessions.
- **Branded and navigational queries are set aside first.** Exclude every grounding query that contains the brand name (ask for it if it is not clear from the data) or that the export labels Navigational. They are left out of each page's share, the median and the low-share list, and are shown in a separate "branded and navigational" block. A brand's share on its own-name queries is expected to be high and says little about discovery.
- **Citation share**: from the Bing AI Performance export, averaged over the page's remaining grounding queries (simple mean; say so). If only citation counts exist, use a stated value/count ordering; do not substitute counts into a citation-share formula. Print the citations behind each share next to it; when the pages' citation counts differ by 5 times or more, say so next to the priority list, because a share built on a few citations is less stable.
- **AI-feature impressions**: from the Search Console generative AI report, when present. Used as context, not in the priority rule.

## Ordered priorities

When the user supplies a method, use it. Otherwise, for a requested ordered list, use the optional editorial index value × (1 − mean eligible observed citation share as a fraction), descending. Show the method, value, mean share, citation counts and arithmetic once. The index is not expected additional conversions, a search rank or proof that edits will increase citations. With counts alone, use a stated value/count ordering, not the share formula.

Rank all eligible confirmed matches with observed shares. Do not truncate the order to a top third. Unknown shares, unconfirmed hosts and pages with only branded/navigational observations stay outside this order, identified as measurement gaps or branded retrieval evidence. Never zero-fill absent rows without established completeness and omission semantics.

## Action types

| Situation | Action type |
|---|---|
| Priority page, cited for some grounding queries | Strengthen the passages that answer those queries (page check) |
| Priority page, not cited in the period | Check eligibility and quotability first (page check) |
| Low-share grounding query with no page on the site that answers it | Content gap: plan a page or a section |
| Low-share grounding query where a page exists | Answer gap for that query, with pasted answers |

## Re-measure

If requested, choose comparable equal-length post-change periods. Four weeks is an optional cadence, not a minimum waiting requirement.

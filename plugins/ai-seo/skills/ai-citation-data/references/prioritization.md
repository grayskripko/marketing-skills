# Prioritization rules for citation exports

This is an optional prioritization heuristic, not a required ranking. Use the user's method when supplied; otherwise state this convention and its confirmed joined population if used. Keep unknown shares outside the ranking.

## Inputs per page

- **Value**: the column the user names, or conversions, then clicks, then sessions.
When the user specifies the ranking population, follow it; for an unfiltered count ranking include every supplied row, including branded and navigational rows. The following exclusion applies only to the default discovery analysis or a user-requested discovery filter. - **Branded and navigational queries are set aside first.** Exclude every grounding query that contains the brand name (ask for it if it is not clear from the data) or that the export labels Navigational. They are left out of each page's share, the median and the low-share list, and are shown in a separate "branded and navigational" block. A brand's share on its own-name queries is expected to be high and says little about discovery.
- **Citation share**: default simple mean over eligible nonbranded/nonnavigational grounding queries; state this averaging method. Use an exposure-weighted mean only when the export supplies comparable per-query exposure denominators matching the share definition; show weights. Counts alone require a stated value/count ordering, not a share substitute. Apply the ≥5× citation-count flag only when the user requests that diagnostic or it changes the interpretation. When defending a share-based order, explain that citation counts are not exposure weights; show a weighting sensitivity check only if supplied comparable denominators support it. Keep GA4 conversions separate from page-value conversions unless their non-overlap is established; unknown overlap can double-count value. Use a low-support warning regardless of ratio when an export explicitly supplies low-volume, suppressed or incomplete observations; use “volume ratio unavailable” when counts are missing, and show 0 versus nonzero directly rather than dividing by zero. Never turn counts into a confidence level without the sampling design.
- **AI-feature impressions**: from the Search Console generative AI report, when present. Used as context, not in the priority rule.

## Ordered priorities

When the user supplies a method, use it. Otherwise, for a requested ordered list, default to the optional editorial index value × (1 − mean eligible observed citation share as a fraction), descending. Use the supplied value/count ordering when these exports contain counts but no observed shares, or the user’s supplied priority method when specified. The constant 1 is the whole-share complement and must not be tuned; absent shares remain unknown. Show the method, value, mean share, citation counts and arithmetic once. The index is not expected additional conversions, a search rank or proof that edits will increase citations. With counts alone, use a stated value/count ordering, not the share formula.

Rank all eligible confirmed matches with observed shares. Do not truncate the order to a top third. Unknown shares, unconfirmed hosts and pages with only branded/navigational observations stay outside this order, identified as measurement gaps or branded retrieval evidence. Never zero-fill absent rows without established completeness and omission semantics.

## Action types

| Situation | Action type |
|---|---|
| Priority page, cited for some grounding queries | Strengthen the passages that answer those queries (page check) |
| Priority page, not cited in the period | Check eligibility and quotability first (page check) |
| Low-share grounding query with no page on the site that answers it | Content gap: plan a page or a section |
| Low-share grounding query where a page exists | Answer gap for that query, with pasted answers |

## Re-measure

Default: equal-length 4-week post-change and comparison windows. Use equal-length windows aligned to supplied campaign dates or the user’s actual reporting cadence when those differ; retain comparable settings and query population. State dates and duration used. Four weeks is a workload cadence, not a minimum biological/algorithmic waiting period.

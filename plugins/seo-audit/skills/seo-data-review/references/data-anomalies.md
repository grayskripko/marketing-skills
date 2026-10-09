# Known Search Console data anomalies

Only entries confirmed by Google's own documentation are listed. Each has its source. The list was checked on 2026-09-29 and re-read on 2026-10-08; newer anomalies may exist, so when the user's dates fall after the check date, ask the user to look at Google's page for those dates:
https://support.google.com/webmasters/answer/6211453 (Search Console Help, "Data anomalies in Search Console").

## How to use this list

- If the export's date range crosses an entry, say so in the answer. If the range is unknown, mention it in one line under Not checked.
- Do not compare the affected metric across the boundary. Compare an unaffected metric instead (usually clicks).
- Do not "correct" the data by guessing. Say what is unreliable and what is still usable.

## Entries

| Dates | What happened | Affected | Unaffected | Source |
|---|---|---|---|---|
| 2025-05-13 to 2026-04-27 | A logging error meant Search impressions were not reported accurately. Google says that after the fix you may see a decrease in impressions; it gives no size. Treat impressions, CTR and average position in that window as unreliable. | Impressions, CTR, average position in Search performance | Clicks | Search Console Help, Data anomalies, entry of 2026-04-03 |
| Current (per Google's AI features page) | AI Overviews and AI Mode appearances are counted inside the normal Performance report under the Web search type. Search Console also has a separate Generative AI performance report (named in the entry of 2026-08-13 below); this skill does not analyze it. | Interpretation of impressions, CTR and position for queries that show AI features | Nothing is missing; it is blended | Google Search Central, "AI features and your website" |
| From 2026-05-07 | FAQ rich results stopped appearing in Google Search, so impressions for the FAQ search appearance fall. | FAQ search appearance rows | Other appearances | Search Console Help, Data anomalies, entry of 2026-05-07 |
| 2026-04-16 to 2026-04-27 | A logging error affected reporting for job listing and job details search appearances. | Impressions and clicks for those appearances | Other appearances | Search Console Help, Data anomalies |
| 2026-02-28 and 2026-03-01 | Some properties are missing these two days in bulk data exports. | Bulk data export tables | Not stated by Google | Search Console Help, Data anomalies |
| 2026-05-07 to 2026-05-08, 2026-05-21, 2026-06-24, 2026-08-13 | Logging errors lowered reported clicks and impressions for Discover (and Generative AI in Discover on some dates). | Discover performance | Search performance | Search Console Help, Data anomalies |
| 2026-08-13 to 2026-08-17 | A logging error lowered impressions in the Generative AI performance report for Search; Google reported the missing data restored on 2026-08-21. | That report, for those dates | Web search performance | Search Console Help, Data anomalies |

## Standing caveats

- Average position is averaged over all impressions, including positions far down the results. Compare it within a query group, not site-wide.
- Some rare queries are hidden for privacy, so totals by query add up to less than totals by page. Compare like with like.
- For trends, clicks are the primary measure. Impressions react more to reporting changes and to changes in the layout of search results.

## Changes not listed here

Some widely reported shifts in Search Console numbers were not published by Google as data anomalies, for example the drop in desktop impressions many sites saw in September 2025 after Google stopped supporting a URL parameter used by rank-tracking tools to request 100 results per page. Because there is no dated entry from Google, this plugin does not treat it as a fact. Use the general rule instead: if impressions fall sharply while clicks stay flat and average position improves, suspect a measurement change before a ranking loss, and compare clicks.

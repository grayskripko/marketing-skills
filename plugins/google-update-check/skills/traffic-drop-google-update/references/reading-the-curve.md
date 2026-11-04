# Reading the curve

## First day of the fall

A heuristic of this check, not a Google rule; say so when you use it.

- The first day of the fall is the first of at least 3 days in a row more than 20% below the median of the previous 28 days. Where the site has a weekly pattern, compare the same weekdays. Ignore single-day dips and public holidays. Name the day you used.
- The level-off day is the first of 7 days in a row within 10% of each other after the fall.
- With weekly or monthly numbers only, give the week or month and say that the first day is not known.

## Search Console versus analytics

- A real traffic fall shows in both Search Console clicks and analytics sessions from Google organic.
- A fall in Search Console only, with analytics flat, points to the report.
- A fall in analytics only, with Search Console clicks flat, points to tracking (a tag, a consent banner, a property change).
- Impressions down with clicks flat and average position better points to measurement or query mix before ranking loss.

## Which anomaly affects which metric

The tool gives each Search Console data anomaly with `surfaces` and `metrics`. Match them to where the user saw the fall. This table only says how to match; the dated entries come from the tool.

| Anomaly surface (tool value) | Explains a fall in | Does not explain a fall in |
|---|---|---|
| `web_search` | the named metrics in the Search results performance report | analytics sessions; Discover; metrics the entry says were not affected |
| `discover` | Discover performance report clicks and impressions | web search clicks or impressions; analytics sessions |
| `generative_ai_search` | Generative AI performance report (Search) impressions | web search clicks or impressions in the main report; analytics sessions |
| `generative_ai_discover` | Generative AI features in Discover impressions | web search; analytics sessions |
| `search_appearance_job_listings`, `search_appearance_faq` | impressions or clicks filtered to that search appearance, or its rich result report | the site's total clicks, unless that appearance carried most of them |
| `bulk_data_export` | rows missing from BigQuery bulk exports on those days | the Search Console interface; analytics |

- An entry with `data_logging_only: true` means Google says real traffic was not affected, only the report.
- An entry with `data_logging_only: false` can describe a real change on Google's side (for example a results feature that stopped showing). Say what Google wrote and that the fall may be real.
- An entry on impressions only (`metrics` without `clicks`) does not explain a fall in clicks.

## Control checks on the user's own data

Run only the checks the data allows. Show the numbers. The 10% and 14-day figures are heuristics of this check; say so once if you use them.

1. **Clicks against impressions (Search Console).** Impressions fell and clicks held within about 10%: suspect a reporting or layout change before a ranking loss. Both fell together: a real loss of visibility is more likely.
2. **Google against other sources on the same days (analytics).** Organic visits from Google fell while Bing, direct and referral visits held: it points to Google. Everything fell at once: tracking, a site outage or demand is more likely than a Google event.
3. **Sitewide against a few page groups (Search Console pages or analytics landing pages).** Compare the 14 days before the change with the 14 days after. Losses spread over most page groups fit a broad Google change. Losses in one template, folder or a handful of URLs fit a site change on those pages (a release, a noindex, a redirect, removed content).

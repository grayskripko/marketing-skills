# Content Strategy Kit

Content strategy for teams with limited hours: what to keep, fix or retire, what to make next and what not to make now, with the rule or calculation behind each decision. Covers content audits, pruning, topic maps, briefs, lead magnets and a plan sized to real capacity. It plans; it does not write the content or build campaigns.

## What it does

- **content-inventory:** keep, update, merge, redirect, retire or leave alone for each page, with its rule id.
- **topic-map:** topics by buyer stage, intent and committee role, each with its source of new information or marked commodity.
- **content-prioritize:** a plan sized to the team's hours, with a 0-12 planning score and a not-now list.
- **content-brief:** a writer brief with proof slots and a success metric.
- **lead-magnet-plan:** one asset for one conversion point, with a gate decision.

## Examples

- Keep, update, merge or cut: /blog/ap-tips-2021 (40 visits), /blog/ap-automation-guide (2,100), /blog/ap-tips-2023 (35).
- Demo goal, 1 writer 6h/wk. Topics: ROI guide (own data), customer story (own data), AP glossary (none). What fits this quarter?
- Topic map for Northwind Ledger: AP automation for 50-500 staff firms, goal demo requests, we have 40 customer interviews.

## How it works

Fate row: `/blog/ap-tips-2023 | G1 | visits 35 | merge into /blog/ap-tips-2021 | R2 | S`. Score row: `1 | Month-end close checklist | 4 h | 2 2 2 1 2 2 | 11`. Dates never decide a fate; scores are for planning, not traffic forecasts.

## Data and network

Only the content-inventory skill fetches anything: when you give a sitemap URL, it reads at most 3 sitemap files as lists of URLs without visiting those URLs, and it fetches at most 10 public pages that you name on the same site, after checking that site's robots.txt and skipping disallowed paths; it never logs in, submits forms or follows links, and no skill runs web searches or calls any other service. If the assistant has a code tool, it may use it to compute the tables and totals from what you pasted; the plugin ships no code and stores nothing.

## Troubleshooting

- A rule was skipped: add the column named under Not checked.
- The plan looks small: it matches the hours you gave; change the hours or the reserved share.
- A fetch failed: paste the list instead.

## Support

Open an issue: https://github.com/grayskripko/marketing-skills/issues

## License

MIT. See LICENSE.

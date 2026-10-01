# Programmatic SEO Gate

For template-based SEO pages built from a dataset, not programmatic advertising. Decide whether a page set deserves to exist, specify the template, check sample pages and roll out in gated batches. It never writes the pages.

| Rows | Pass (UV ≥ 3) | Pass share | Largest duplicate group | Verdict |
|---|---|---|---|---|
| 40 | 10 | 25.0% | 75.0% | Narrow: build the 10 passing rows |

## What it does

| Skill | Give it | You get |
|---|---|---|
| pseo-viability | page-set idea plus rows or columns | column classes, per-row score, duplicate groups, Go / Narrow / No-go with the passing rows |
| pseo-template-spec | approved page type and columns | block table, variable-text target, banned blocks, noindex and merge rules, block map for one row |
| pseo-sample-qa | 3 to 20 pasted sample pages | similarity matrix after removing the shared template, flags and an action per page |
| pseo-rollout | page count and URL pattern, later typed batch counts | hierarchy, sitemap split, pilot size, stop check, rollback |

## Examples

- "Page per tool? tool,fee,days,currencies,api / Acme,1.2%,2,3,y / Globex,1.2%,2,3,y / Initech,0.9%,5,12,n / Umbra,0.7%,1,8,n"
- "Spec a template for 'Northwind Ledger vs {competitor}' pages. Columns: competitor, fee, payout_days, currencies, api"
- "Rollout for 800 integration pages: batch 1 published 40, indexed 15, 6 indexed with zero impressions. Continue or stop?"

## How it works

Every verdict comes after a printed table. Thresholds are labelled as this plugin's heuristics. Missing values become `[DATA NEEDED]`; nothing is estimated or invented, including search volume. Requests for many near-identical pages, or for pages about private individuals, are declined with a dataset check offered instead.

## Data and network

Network scope: this plugin fetches nothing and runs no web search. It works only on rows, tables and page text you paste or attach, runs nothing and changes no files or settings unless you ask, and may use the assistant's code or spreadsheet tool to compute the tables it shows. It stores nothing.

## What it will not do

Write or generate pages, audit a live site, estimate keyword volume, plan editorial calendars, or suggest content shown only to crawlers.

## Troubleshooting

No verdict means no rows were pasted. A column you think matters scored zero: reclassify it as distinguishing and rerun. Pages too short to compare are flagged thin.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.

# Programmatic SEO Gate

For SEO pages built from a dataset, one page per city, tool, integration or product (not programmatic advertising). Before you build hundreds of template pages, it tells you which rows have enough facts of their own to deserve a page, what the template must contain, whether your sample pages are near-copies, and when to stop a rollout. It never writes the pages.

Example: six payment tools, where three share the same fee, payout time, currencies and API, and two others match each other. Answer: build three pages, not six; tools with identical facts share a page.

## What it does

| Skill | Give it | You get |
|---|---|---|
| pseo-viability | page-set idea plus rows or columns | which rows deserve a page, which share one, and the table behind it |
| pseo-template-spec | chosen page type and columns | block table, how much of each page must change per row, banned blocks, noindex and merge rules, block map for one row |
| pseo-sample-qa | 3 to 20 pasted sample pages | keep, merge or noindex per page, with the similarity table behind it |
| pseo-rollout | page count and URL pattern, later typed batch counts | hierarchy, sitemap split, pilot size, continue or stop, rollback |

## Examples

- "Page per tool? tool,fee,days,currencies,api / Acme,1.2%,2,3,y / Globex,1.2%,2,3,y / Initech,0.9%,5,12,n / Umbra,0.7%,1,8,n"
- "Spec a template for 'Northwind Ledger vs {competitor}' pages. Columns: competitor, fee, payout_days, currencies, api"
- "Rollout for 800 integration pages: batch 1 published 40, indexed 15, 6 indexed with zero impressions. Continue or stop?"

## How it works

Each answer opens with the decision, then the table behind it. Thresholds are given as plain recommendations, and Google is named only where a recommendation rests on it. Missing facts are named; nothing is estimated or invented, including search volume. Requests for many near-identical pages, or for pages about private individuals, are declined with a dataset check offered instead.

## Data and network

Network scope: this plugin fetches nothing and runs no web search. It works only on rows, tables and page text you paste or attach, does not search your folders or files for data, runs nothing and changes no files or settings unless you ask, and may use the assistant's code or spreadsheet tool to compute the tables it shows. It stores nothing.

## What it will not do

Write or generate pages, audit a live site, estimate keyword volume, plan editorial calendars, or suggest content shown only to crawlers.

## Troubleshooting

No verdict means no rows were pasted. A column you think matters was ignored: say it changes what a reader would do, and the check reruns with it. Pages too short to compare are flagged thin.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.

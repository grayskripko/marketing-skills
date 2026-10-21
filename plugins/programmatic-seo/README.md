# Programmatic SEO Gate

For SEO pages built from a dataset, one page per city, tool, integration or product (not programmatic advertising). Before you build hundreds of template pages, it tells you which rows carry facts a reader would act on, what the template must contain, whether your sample pages are near-copies, and whether your batch numbers say continue or pause. It never writes the pages.

Example: six payment tools, where three share the same fee, payout time, currencies and API. Those three would be the same page under different names, so they can share one.

## What it does

| Skill | Give it | You get |
|---|---|---|
| pseo-viability | page-set idea plus rows or columns | which rows deserve a page, which can share one, and what data is missing |
| pseo-template-spec | chosen page type and columns | block spec, empty-field handling, title pattern, block map for one row |
| pseo-thin-content-check | pasted sample pages | keep, merge or change per page, with the reason |
| pseo-rollout | page count and URL pattern, later typed batch counts | launch plan, count check, continue or pause, action per group of pages |

## Examples

- "Page per tool? tool,fee,days,currencies,api / Acme,1.2%,2,3,y / Globex,1.2%,2,3,y / Initech,0.9%,5,12,n / Umbra,0.7%,1,8,n"
- "Spec a template for 'Northwind Ledger vs {competitor}' pages. Columns: competitor, fee, payout_days, currencies, api"
- "Rollout for 800 integration pages: batch 1 published 40, indexed 15, 6 indexed with zero impressions. Continue or stop?"

## How it works

Each answer opens with the decision and keeps to what you asked. Your constraints (budgets, required fields, windows, approved plans) are kept as given, and no cutoffs or scores are invented; Google is named only where a point rests on it. Missing facts are named; nothing is estimated or invented, including search volume. Requests to write the pages themselves, or for pages about private individuals, are declined.

## Data and network

Network scope: this plugin fetches nothing and runs no web search. It works only on rows, tables and page text you paste or attach, does not search your folders or files for data, has no scripts of its own, and changes files or settings only if you ask the assistant to. The assistant's code or spreadsheet tool may be used only to compute the tables it shows. The Google links in the skills are reference text and are not fetched. It stores nothing.

## What it will not do

Write or generate pages, audit a live site, estimate keyword volume, plan editorial calendars, or suggest content shown only to crawlers.

## Troubleshooting

No verdict means no rows were pasted. A column you think matters was ignored: say it changes what a reader would do, and the check reruns with it. Pages too short to compare are flagged thin.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.

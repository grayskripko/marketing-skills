# Site Architecture & Faceted Navigation

Plan how your website is organised: where each page sits and what its URL is, what the menus and breadcrumbs say, which internal links to add, which filter URLs search engines should index, and where old URLs redirect when you move. Built from your own page list or exports; it does not present proposed URLs as existing and identifies new addresses individually, or once for an entirely new set.

Example: laptop filters brand 8, RAM 4, GPU 6, screen 5, price 6 (single-select) give 9 · 5 · 7 · 6 · 7 = 13,230 filter states, × 4 sort options = 52,920 URLs. facet-policy prints that formula, then marks as indexable only the filter pages your search-demand data supports.

## What it does

| Skill | Give it | You get |
|---|---|---|
| information-architecture | page list, menus or your domain | the parts you ask for: URL tree, URL rules, navigation and breadcrumb spec, moved-URL list |
| internal-linking-plan | links export (source, target) | depth and inlinks, the most useful 30 or so link edits first when you give no number (or the complete plan you ask for), and what the edits change |
| hub-design | pages on one subject | hub outline, links between the pages, pages that seem to overlap (for you to decide) |
| facet-policy | filters and values, optional queries | URL count, index decision per filter, rules sheet, conflicts |
| site-migration-redirect-map | old and new URLs, or a draft map | redirect map checked for chains, loops and homepage targets, launch checklist on request |

## How it works

Each skill answers the question you asked first and gives the plan, in a form a web team can build, and keeps the URLs and page decisions you fixed.

## Data and network

Network scope: this plugin calls no service of its own and stores nothing. It reads what you paste or attach and, in the information-architecture skill only, when you name your own site and your assistant has a web tool, that site's robots.txt, up to three sitemap files it lists and up to five public HTML pages, all on the same host; it fetches no other site. It changes no files, sites or settings unless you ask, and it may use your assistant's code or spreadsheet tool to compute the tables it shows. See PRIVACY.md.

## What it will not do

Audit a site, decide which content to keep, research keywords, write copy, change a live site, or predict traffic.

## Troubleshooting

No web tool: paste a URL list, menu HTML or links export. Large export with no code or spreadsheet tool: about 200 links by hand; above that, it asks for the relevant subset. Inlink totals and a partial outlink sample can guide priorities but cannot establish exact whole-site depths.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues. MIT license.

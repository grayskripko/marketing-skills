# Site Architecture Kit

Website structure plans that show their working: one parent per page, link plans built only from your own URLs, filter URLs counted, redirect maps tested.

Example: laptop filters brand 8, RAM 4, GPU 6, screen 5, price 6 (single-select) give 9 · 5 · 7 · 6 · 7 = 13,230 filter states, × 4 sort options = 52,920 URLs. facet-policy prints that formula, then indexes only what your query data supports. URL lists end with "n of n URLs checked against your data"; new pages are marked NEW.

## What it does

| Skill | Give it | You get |
|---|---|---|
| site-architecture | page list, menus or your domain | URL tree, page table, URL rules, nav spec, checks, moved-URL list |
| link-plan | links export (source, target) | depth and inlinks, up to 30 new links, depth after |
| hub-design | pages on one subject | node types, same-intent pairs, hub outline, link matrix |
| facet-policy | filters and values, optional queries | URL count, index decision per filter, rules sheet, conflicts |
| redirect-map | old and new URLs, or a draft map | redirect map, ten checks, launch checklist |

## How it works

Each skill prints its calculation, gives the plan, then runs numbered checks with the failing rows. Rules cite Google Search Central or Nielsen Norman Group, or are labelled heuristics you can change.

## Data and network

Network scope: this plugin calls no service of its own and stores nothing. It reads what you paste or attach and, only when you name your own site and your assistant has a web tool, that site's robots.txt, up to three sitemap files it lists and up to five public HTML pages, all on the same host; it fetches no other site. It changes no files, sites or settings unless you ask, and it may use your assistant's code or spreadsheet tool to compute the tables it shows. See PRIVACY.md.

## What it will not do

Audit a site, decide which content to keep, research keywords, write copy, change a live site, or predict traffic.

## Troubleshooting

No web tool: paste a URL list, menu HTML or links export. Large export with no code or spreadsheet tool: up to 200 rows by hand; above that, see the link-plan fallback.

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues. MIT license.

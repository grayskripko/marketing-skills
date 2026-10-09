# Site Architecture Kit

Plan how your website is organised: where each page sits and what its URL is, what the menus and breadcrumbs say, which internal links to add, which filter URLs search engines should index, and where old URLs redirect when you move. Built from your own page list or exports; it never invents a URL and marks every new page NEW.

Example: laptop filters brand 8, RAM 4, GPU 6, screen 5, price 6 (single-select) give 9 · 5 · 7 · 6 · 7 = 13,230 filter states, × 4 sort options = 52,920 URLs. facet-policy prints that formula, then marks as indexable only the filter pages your search-demand data supports.

## What it does

| Skill | Give it | You get |
|---|---|---|
| site-architecture | page list, menus or your domain | URL tree, page table, URL rules, nav spec, checks, moved-URL list |
| link-plan | links export (source, target) | depth and inlinks, up to 30 new links, depth after |
| hub-design | pages on one subject | hub outline, links between the pages, pages that overlap |
| facet-policy | filters and values, optional queries | URL count, index decision per filter, rules sheet, conflicts |
| redirect-map | old and new URLs, or a draft map | redirect map checked for chains, loops and homepage targets, launch checklist |

## How it works

Each skill gives the plan first, then the calculation behind it and any problems its checks found. Rules cite Google Search Central or Nielsen Norman Group, or are labelled as this plugin's own defaults you can change.

## Data and network

Network scope: this plugin calls no service of its own and stores nothing. It reads what you paste or attach and, only when you name your own site and your assistant has a web tool, that site's robots.txt, up to three sitemap files it lists and up to five public HTML pages, all on the same host; it fetches no other site. It changes no files, sites or settings unless you ask, and it may use your assistant's code or spreadsheet tool to compute the tables it shows. See PRIVACY.md.

## What it will not do

Audit a site, decide which content to keep, research keywords, write copy, change a live site, or predict traffic.

## Troubleshooting

No web tool: paste a URL list, menu HTML or links export. Large export with no code or spreadsheet tool: up to 200 rows by hand; above that, it asks for two smaller exports instead (inlinks per page, and the links on your homepage and main section pages).

## Support

Issues: https://github.com/grayskripko/marketing-skills/issues. MIT license.

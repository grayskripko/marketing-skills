---
name: site-architecture
description: "Plan a website's information architecture: a page tree where every page has one parent, URLs and URL rules, navigation menus, labels and breadcrumbs, and the list of URLs that move. Works from a page list, sitemap URLs, current menus, the user's own domain or a description of a site still to be built; can also read pasted tree-test results. Use when the user asks how to structure or restructure a website, what the URL structure or page hierarchy should be, or how to organise navigation menus, labels and breadcrumbs. Not for search audits, page copy, page sets generated from a dataset, or software architecture."
---

# Site architecture

Give exactly what the user asked for, in their order, in a form a web team can build. A narrow question (where one page goes, what to call one menu item) gets the placement, the label and the affected breadcrumb in a few lines.

- What the user fixed is fixed: URLs that must not change, final page decisions, "no new pages", "only the menu". Do not add pages, links, overview pages, login or account flows, pagination, breadcrumb rendering rules or test tasks they did not ask for.
- Each page has one structural parent. A page that fits two sections lives under its main purpose; the other section links to it.
- A menu label that only groups pages needs no page and no folder.
- URLs: if the user asks for URL rules and which URLs move, make the URLs follow the rules you give and list the moves (old URL → new URL, permanent redirect), sparing the ones they fixed; do not keep a permanent exception just to avoid one move. If they say keep the addresses, change menus and breadcrumbs only and say no URL moves.
- Use only what was supplied. Do not describe existing labels, link positions or page content you were not given. Mark proposed URLs as new.
- Check supplied numbers against their definitions and point out contradictions next to the conclusion they affect.
- Tree-test results: give success and directness rates per task and what the first clicks show about each label. To claim one tree beats another, test the difference between them (for example a two-proportion test); overlapping per-tree intervals do not settle it. Do not add benchmark bands or sample-size rules, and do not plan another study unless asked.
- The "3-click rule" and "at most 7 menu items" are not criteria; if the user raises them, say in a sentence that research does not support them.

If the user names their own site and a web tool exists, read at most its robots.txt, 3 sitemaps it lists and 5 public pages on that host. Show URLs without email or token parameters. Produce plans only; change nothing live.

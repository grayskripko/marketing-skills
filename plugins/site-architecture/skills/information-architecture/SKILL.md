---
name: information-architecture
description: "A question about the page tree, URL structure, menus or breadcrumbs of your own website, even a quick one-liner. Plan a website's information architecture: a page tree where every page has one parent, URLs and URL rules, navigation menus, labels and breadcrumbs, and the list of URLs that move. Works from a page list, sitemap URLs, current menus, the user's own domain or a description of a site still to be built; can also read pasted tree-test results. Use when the user asks how to structure or restructure a website, what the URL structure or page hierarchy should be, or how to organise navigation menus, labels and breadcrumbs. Not for search audits, page copy, page sets generated from a dataset, or software architecture."
---

# Site architecture

First line answers the question asked (which option, which labels to fix, ranked worst first). Then give exactly what the user asked for, in their order, in a form a web team can build. A narrow question (where one page goes, what to call one menu item) gets the placement, the label and the affected breadcrumb in a few lines.

- What the user fixed is fixed: URLs that must not change, final page decisions, "no new pages", "only the menu". Do not add pages, overview pages, pagination, breadcrumb rows or rules, or test tasks they did not ask for.
- Take the user's measurements and figures (click counts, paths, test results) as given. When they ask what to change or say a path is too deep, list each concrete edit (which link or menu item to add, move or regroup, and where) and give the new click count per target; "change nothing" only if no edit helps. Name what each change replaces in the current menu or path, and say which URLs stay unchanged.
- To shorten a deep path, link the target from a page already one click from Home (a key page or header item). Count clicks the same way on every route: opening a dropdown is a click.
- Plan logged-in states (for example "Log in" becomes "My account") only when the site has accounts and the task touches them. An item the user says is hard to find, or that sits only in the footer or sitemap while visitors need it, moves up into the header.
- Each menu item appears once: not both inside a dropdown and beside it.
- Each page has one structural parent. A page that fits two sections lives under its main purpose; the other section links to it.
- A menu label that only groups pages needs no page, no folder and no breadcrumb step; build it as a button that opens its group (`aria-expanded`), not a link to nowhere and not the ARIA `menu` role. <!-- w3.org/WAI/ARIA/apg/patterns/disclosure/examples/disclosure-navigation/ : top-level items are disclosure buttons with aria-expanded; site navigation does not use the menu role. checked 2026-10-15 -->
- URLs: if the user asks for URL rules and which URLs move, make the URLs follow the rules you give and list the moves (old URL → new URL, permanent redirect), sparing the ones they fixed; do not keep a permanent exception just to avoid one move. If they say keep the addresses, change menus and breadcrumbs only and say no URL moves.
- Use every supplied page, label and content section somewhere in the answer, and nothing beyond them. Do not describe existing labels, link positions or page content you were not given. Mark proposed URLs as new.
- If two supplied numbers contradict each other, say so next to the conclusion they affect.
- Tree-test results: give success and directness rates per task and what the first clicks show about each label. To claim one tree beats another, test the difference between them (for example a two-proportion test); overlapping per-tree intervals do not settle it. Do not add benchmark bands or sample-size rules, and do not plan another study unless asked. Compute p-values with a script, not by hand. Check the counts fit together (direct successes cannot exceed successes or correct first clicks) and flag any that do not. End with the decision (which label or tree to use) and what to look at next.
- The "3-click rule" and "at most 7 menu items" are not criteria; if the user raises them, say in a sentence that research does not support them.
- A general question with no page list or menu: answer it in a few lines from these rules; ask for the page list or menu only if the user wants a plan.

If the user names their own site and a web tool exists, read at most its robots.txt, 3 sitemaps it lists and 5 public pages on that host. Show URLs without email or token parameters. Produce plans only; change nothing live.

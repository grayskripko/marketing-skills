# Structure checks SA-01 to SA-10

Report failing checks only, with the rows involved, the fix and the evidence level (ground rule 10). Thresholds marked "heuristic" can be changed by the user.

| Id | Check | Fails when | Source |
|---|---|---|---|
| SA-01 | One parent per page | A page sits under two sections in the tree, or has no parent. Fix: one home chosen by dominant intent; the other section links to it from body text (guest link). For a page with several plausible parents, NN/g's breadcrumb guidance also asks for one canonical path. | convention of this plugin, NN-BC (guideline 3) |
| SA-02 | Breadcrumb and structural parent agree | A proposed breadcrumb or upward structural link conflicts with the approved structural chain. A URL folder mismatch is a maintenance consideration, not automatic authorization to move an existing page; curated hub membership is not parentage. Breadcrumbs show hierarchy, not visitor history. | convention of this plugin, NN-BC (guideline 2), U-07 |
| SA-03 | Coherent patterns within scope | A proposed new URL or authorized move violates the agreed pattern within its namespace/version/CMS constraints. Existing pages in several folders are a maintenance consideration, not automatic MOVED status. | U-10, convention of this plugin |
| SA-04 | No two pages share a primary intent | Two pages answer the same need, for example `/plans` and `/pricing`. Listed as a merge question for the user or hub-design; this skill does not set fate. A fragment such as `/faq#pricing` is a section, not a page, and is not counted. | convention of this plugin, G-url |
| SA-05 | Every page has at least one inbound structural link in the plan | A page is reachable only from the sitemap or not at all. | G-links |
| SA-06 | Important tasks have suitable access routes | An important audience task has no suitable entry route. Select header, section/hub, search or account routes from the journey; depth and menu counts are not pass marks. | NN-3click, NN-FD, heuristic of this plugin |
| SA-07 | Growing sections have listing pages with crawlable paginated links | A section expected to grow has no listing, or pages beyond the first are reachable only through script or a "load more" button, with no `<a href>` link to them. | G-page |
| SA-08 | URL rules sheet respected | Any rule in `url-rules.md` broken; list the URLs with the rule written out. | url-rules.md |
| SA-09 | Help and support content has its own hub, linked from product pages | Help articles are reachable only from the footer. | convention of this plugin |
| SA-10 | Every MOVED, MERGED or removed URL is in the hand-off list | A status change without a hand-off row. With no current URLs given, Not checked, never a pass. | G-move |

Utility pages (about, contact, legal, trust) form a sitewide layer in the header or footer. They are not forced into a topical section and do not fail SA-01 for sitting outside one (convention of this plugin).

# Structure checks SA-01 to SA-10

Each check reports pass or fail, a count, the failing rows and an evidence level. Thresholds marked "heuristic" can be changed by the user.

| Id | Check | Fails when | Source |
|---|---|---|---|
| SA-01 | One parent per page | A page sits under two sections in the tree, or has no parent. Fix: one home chosen by dominant intent; the other section links to it from body text (guest link). For a page with several plausible parents, NN/g's breadcrumb guidance also asks for one canonical path. | PR, NN-BC (guideline 3) |
| SA-02 | Breadcrumb parent = URL folder = upward link | Any of the three disagrees, for example a hub child breadcrumbed under Blog. Breadcrumbs show the hierarchy, not the visitor's history. | PR, NN-BC (guideline 2), U-07 |
| SA-03 | One URL pattern per page type | Pages of one type live under two folders, for example `/product/analytics` and `/features/sso`. Pick one; the rest are MOVED. | U-10, convention of this plugin |
| SA-04 | No two pages share a primary intent | Two pages answer the same need, for example `/plans` and `/pricing`. Listed as a merge question for the user or hub-design; this skill does not set fate. A fragment such as `/faq#pricing` is a section, not a page, and is not counted. | PR, G-url |
| SA-05 | Every page has at least one inbound structural link in the plan | A page is reachable only from the sitemap or not at all. | G-links |
| SA-06 | Tier-A pages linked from the header, or from a hub the header links to | A tier-A page has neither a header link nor a link from a hub, section index or dropdown that the header links to. Depth is reported for every page; no click count is a pass mark. Categories are judged by how distinct they are, not by item counts. | NN-3click, NN-FD, heuristic of this plugin |
| SA-07 | Growing sections have listing pages with crawlable paginated links | A section expected to grow has no listing, or pages beyond the first are reachable only by script or a "load more" button without links. | G-page |
| SA-08 | URL rules sheet respected | Any line of `url-rules.md` broken; list the URLs and the rule number. | url-rules.md |
| SA-09 | Help and support content has its own hub, linked from product pages | Help articles are reachable only from the footer. | PR |
| SA-10 | Every MOVED, MERGED or removed URL is in the hand-off list | A status change without a hand-off row. | G-move |

Utility pages (about, contact, legal, trust) form a sitewide layer in the header or footer. They are not forced into a topical section and do not fail SA-01 for sitting outside one (PR).

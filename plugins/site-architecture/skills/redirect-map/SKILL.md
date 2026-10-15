---
name: redirect-map
description: "Build or check a redirect map for URL changes and site moves: each old URL mapped to its new URL or to 404/410, with chains, loops, homepage targets, temporary codes and case or slash variants fixed, plus a launch checklist when asked. Takes old URLs with their decided fate, plus the new URL list or rules, or a draft map to check. Use when the user moves to a new domain, CMS or URL scheme, merges pages whose fate is decided, or asks to build or review redirects. Not for deciding which pages to keep or prune."
---

# Redirect map

Lead with the corrected map: old | destination | code | what changed. Keep the user's page decisions; do not reopen them.

- Every redirect goes in one hop to the final 200 URL: collapse chains, break loops, use 301 or 308 for permanent moves.
- Unchanged pages answer 200 with no redirect. Removed pages with no replacement answer the decided 404 or 410, never the homepage. Merged pages go to the page they were merged into.
- A row without a decided fate stays unresolved with one question; clicks and backlinks set priority, not fate.
- Flag a destination that is not 200 or is noindexed.
- Variants: cover case and trailing slash. Redirects pass the query string through; never strip utm, gclid or other parameters the site uses for attribution.

When a launch checklist is asked for, make it something a team can tick, before / at / after launch, with the expected result for each row (status code, one hop, the right `Location`):
- before: test every row on staging; update internal links, canonicals and the sitemap to final 200 URLs only; save the old configuration for rollback; record a baseline of traffic and errors; keep analytics and Search Console verification working through the change; make sure catch-all or CMS fallback rules cannot override specific redirects;
- at launch: remove development blocks (noindex, robots.txt disallow, passwords); check every old URL on production; check key pages render and journeys work; submit the sitemap; say whether Change of Address applies (only when the domain or subdomain changes);
- after: recheck all rows right away, then watch errors, redirect hits and indexing, highest-exposure URLs first; keep the redirects at least a year.

Server rule lines only if the stack is named, marked to test on staging. Produce plans only; change nothing live.

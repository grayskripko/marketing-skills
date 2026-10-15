---
name: link-plan
description: "Build an internal link plan from a links export (one row per link: source URL and target URL, optionally anchor, link position and status): click depth over followable links, the links to add with anchor text and placement, using only URLs found in the export, and depth recomputed with the new links. Use when the user shares a source-to-target links export or list and asks where to add internal links, for a link plan for key pages, or how click depth changes after new links. Not for audit reports from per-page crawl tables or Search Console exports."
---

# Link plan

Lead with one table of link edits: source | target | anchor | placement | reason. Put additions, anchor changes, links repointed from redirects to final URLs, and buttons converted to `<a href>` links in the same table. When the supplied link set is small and the user asks to compare before and after, show every supplied link that matters in that table, each marked added, changed or unchanged.

- Use only URLs in the export. A placement on the source page is "existing" only when the export says where the link sits; otherwise call it proposed. Choose placements the supplied page content supports.
- Depth is counted from the homepage over followable `<a href>` links; nofollow links, buttons and script-only links do not count. If the export is partial, a path you find is an upper bound, not the site-wide shortest path, and a missing path means unknown, not unreachable.
- After the edits, recompute and show before → after for the pages the user asked about, with the route (Home → page → page). Report unchanged depths plainly.
- If no number of links is given and many qualify, give the most useful first (about 30) and say how many more remain.
- No anchor-text quotas, no repeated exact-match anchors, no internal nofollow.
- Without a code or spreadsheet tool, work by hand up to about 200 links; above that, ask for the relevant subset.

Show URLs without email or token parameters. Produce plans only; change nothing live.

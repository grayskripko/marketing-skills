---
name: internal-linking-plan
description: "A question about internal links or click depth on your own website, even a quick one-liner before you have a links export. Build an internal link plan from a links export (one row per link: source URL and target URL, optionally anchor, link position and status): click depth over followable links, the links to add with anchor text and placement, using only URLs found in the export, and depth recomputed with the new links. Use when the user shares a source-to-target links export or list and asks where to add internal links, for a link plan for key pages, or how click depth changes after new links. Not for audit reports from per-page crawl tables or Search Console exports."
---

# Link plan

Lead with one table of link edits: source | target | anchor | placement | reason. Put additions, anchor changes, links repointed from redirects to final URLs, and buttons converted to `<a href>` links in the same table.

- Use only URLs in the export. A placement on the source page is "existing" only when the export says where the link sits; otherwise call it proposed. Choose placements the supplied page content supports.
- Depth is counted from the homepage over followable `<a href>` links; nofollow links, buttons and script-only links do not count. If the export is partial, a path you find is an upper bound, not the site-wide shortest path, and a missing path means unknown, not unreachable.
- Before → after compares what the edits change: for each target page, the followable `<a href>` links pointing to it (count and sources) before and after; add depth with the route (Home → page → page) only where depth changes. Leave out rows that do not change; one line can say the rest are unchanged.
- If no number of links is given and many qualify, give the most useful first (about 30) and say how many more remain.
- No anchor-text quotas, no repeated exact-match anchors, no internal nofollow.
- Without a code or spreadsheet tool, work by hand up to about 200 links; above that, ask for the relevant subset.
- A general question with no export (how many links a page needs, whether a button counts as a link): answer it in a few lines from these rules, then say which export rows would settle it for the user's site.

Show URLs without email or token parameters. Produce plans only; change nothing live.

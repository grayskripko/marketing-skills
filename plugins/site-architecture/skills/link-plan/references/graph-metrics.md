# Graph metrics

All values are computed on followable links after the data gate. Print each formula once with its inputs.

## Depth

- Convention: the start URL (usually the homepage) has depth 0. If the user did not name it, take the shortest root URL in the data, say so, and ask once at the end. A page linked from it has depth 1, and so on.
- Method: breadth-first search from the start URL over followable links. Depth = number of links on the shortest path.
- Report per folder or template: n, median, p90 (nearest-rank), max, and pages with no path ("unreached").
- Second pass: remove links whose source or target is a paginated listing beyond page 1 (`?page=`, `/page/n`), then recompute. Pages that become unreached depend on pagination alone; list their count by folder.
- Example: `/` → `/blog` → `/blog/okta-setup` → `/features/sso` gives `/features/sso` depth 3. Adding `/features` (depth 1) → `/features/sso` makes it depth 2.

## Inlinks

- Inlinks per page = distinct source pages with a followable link to it.
- Split by link position: navigation (header, menu, footer, sidebar, breadcrumb) vs body (content). Without a position column, the split is Not checked.
- Report: pages in the user's important list with 0 or 1 body inlinks; pages with navigation inlinks only.

## Links to redirects and errors

- Count followable links whose target answers 3xx or 4xx, grouped by source template or folder, with the final URL for each 3xx target. Updating internal links to the final URL removes a hop for every visit (G-move).

## Anchors

- Generic anchors: anchors that say nothing about the target ("click here", "read more", "learn more", "here"), with counts (G-links).
- One anchor, several targets: the same anchor text pointing to two or more different URLs.

## Value share (only with tiers or clicks)

| Tier | Share of pages | Share of body inlinks | Gap |
|---|---|---|---|
| A | A pages / all pages | body inlinks into A pages / all body inlinks | second − first |

- A negative gap means the important pages get fewer body links than their number suggests. No pass mark. The idea of linking by business value rather than demand alone comes from practitioner practice (PR).

## Clusters (only when the user labels clusters)

- Links within a cluster / all links from that cluster's pages. Printed for information; no threshold.

## After the plan

- Add every planned link as a body link and rerun depth and inlinks. Print before → after for each page the plan touches, and the number of tier-A pages that still have no body-link path.

## By hand

- Up to 200 edges without a code tool: list adjacency by source, run the search level by level, and mark "computed by hand — check". Above 200 edges, do not attempt it (rule 4).

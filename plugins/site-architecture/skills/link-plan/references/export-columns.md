# Edge-list columns

An edge list has one row per link: the page the link is on (source) and the page it points to (target). A per-URL crawl table (one row per page, with counts) is not an edge list; with only that, depth can be read from its depth column if present, but no link plan can be checked against real links. Say so and ask for the links export.

| Meaning | Common header names | Required |
|---|---|---|
| source | Source, From, Source URL, Referrer, Page URL | yes |
| target | Destination, Target, To, Link URL, Address | yes |
| anchor | Anchor, Anchor Text, Alt Text (for image links) | no; without it anchor checks are Not checked |
| link position | Link Position, Position, Placement (values such as navigation, header, footer, content, sidebar) | no; without it the navigation/body split is Not checked |
| follow | Follow, Rel, Nofollow | no |
| link type | Type (hyperlink, image, canonical, redirect, script) | no; keep only hyperlinks and image links for depth |
| target status | Status Code, Status | no; without it links to 3xx/4xx are Not checked |
| final URL | Redirect URL, Final URL, Redirects To | no |

Desktop crawlers and site-audit tools offer a links export with these or similar headers (often called all inlinks or all links). Map by meaning internally; show the mapping only when requested or needed to resolve a material ambiguity, and ask if a required column is unclear.

Clean-up before computing:
- Drop rows whose target is on another host, rows where source = target, and fragment-only targets.
- Normalise case, trailing slash and protocol by the site's own policy before matching.
- Strip parameters that carry an email address or token-like value, and count the rows affected (rule 11).
- Treat a row as followable only if it is an `<a href>` hyperlink (or a linked image) without nofollow.

## Also accepted

- A pasted list of `source -> target` lines.
- An optional page sheet: URL, tier (A/B/C) or a value column (clicks, sign-ups, revenue), folder or template, and whether the page is a paginated listing.

## Too large to compute here

Without computational tooling, use 200 edges as a conservative guardrail and assess complexity. Ask for tooling or complete relevant edges for exact before/after. Aggregate inlinks and partial homepage/section outlinks support priorities and observed paths only: observed path length bounds true shortest depth above, while absent paths leave reachability unknown.

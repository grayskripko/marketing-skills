# Link plan rows

## Row format

| # | Source URL | Target URL | Anchor | Placement on the source | Reason |
|---|---|---|---|---|---|

- Anchor: a few words that tell a reader what the target page is, in the reader's language. No anchor repeated across rows for ranking; vary naturally (rule 8, G-links).
- Placement: propose a relevant section of the source page and mark it proposed. Do not describe an existing link as already in that section unless the input says so; otherwise its current placement is not supplied. Avoid a footer or generic related-links dump.
- Reason: one line, for example "tier A, no body inlink", "depth 4, nearest relevant page is depth 1", "next step after this how-to".

## Order

1. Tier-A pages with no body-link path.
2. Tier-A pages at the greatest depth.
3. Pages with exactly one body inlink.
4. Anything else the user asked for.
Without tiers, use the user's list of important pages, then depth.

## Caps (heuristics of this plugin — change them if you like)

- At most 30 rows per run.
- At most 3 new links added to any one source page per run.
- Sources are pages whose subject is close to the target; a source with no connection to the target is not used, even when it would cut depth.

## Provenance check

Before printing, check every source and target against the input; the answer does not report the check. A row whose URL is not found is removed and counted, never kept. If the user asks to make up URLs, decline that part (rule 3) and offer NEW pages as a separate list for site-architecture.

## Off-topic inlinks (optional)

For a hub, list existing body links into it from pages outside its subject, for the user to review. Adding new links does not cancel old off-topic ones (convention of this plugin).

# Rollout rules

All numbers here are rules of thumb of this plugin unless a Google page is named.

## Hierarchy

- Hub page, category pages, then individual pages. Every individual page sits within three clicks of the hub; print the actual depth (hub → category → page is 2).
- Each individual page links to its category and to a few related pages that share a fact. No block of links to every sibling.
- The hub carries a table of all rows, including rows that are not built as pages.

## Batches

- Pilot: the larger of 20 pages or 5% of planned pages, rounded up.
- Later batches: no more than double the previous batch.
- Measurement window: set by the user; default 8 weeks, labelled.

Sitemaps per batch are a measurement choice (index coverage can be read per file), not a file-limit requirement; say so.

## Inputs per batch

Published pages, indexed pages, and indexed pages with no impressions in the window. A page that is not indexed cannot have impressions, so zero-impression pages are counted among indexed pages only.

Consistency check before any rule: indexed ≤ published, and indexed pages with no impressions ≤ indexed. If the user gives zero-impression pages over all published pages, convert: indexed with no impressions = given count − (published − indexed); if that is negative, the numbers cannot be right: say so and ask, without applying any rule.

## Stop rules per batch

| Rule | Stop when |
|---|---|
| Indexed share | indexed pages divided by published pages is below 50% |
| Zero-impression share | indexed pages with no impressions divided by indexed pages is at least 30% |

Continue only when neither rule fires. The counts say whether to pause, not why Google left pages out; never name a cause from counts alone; a sample check of the pages can show near-duplicates. A batch below 20 pages gets "small sample". If the batch is younger than the window, the verdict is conditional on the window; say so and ask how long the pages have been live.

## Rollback actions

1. Split failing pages by cause:
   - not indexed → improve the page with more row data, or merge it into the hub with a redirect; do not add more pages of that template. noindex only keeps a page out of the index (Block search indexing with noindex, 2025-12-10), so it does not help a page you want indexed.
   - indexed but no impressions after the window → `noindex, follow`, or merge into the hub.
2. Keep noindexed pages crawlable (not blocked in robots.txt).
3. Rule of thumb of this plugin: a page left on `noindex, follow` for a long time may stop passing links; rows that will never be built belong in the hub table, not on noindexed pages.
4. Fix the template and check 3 to 20 sample pages for near-duplicates.
5. Release the next batch only after the fixed batch passes.

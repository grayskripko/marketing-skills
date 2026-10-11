# Rollout rules

All numbers here are rules of thumb of this plugin unless a Google page is named.

## Hierarchy

- Hub page, category pages, then individual pages. Default: each page sits within 3 clicks of the hub; use greater depth only when each extra supplied taxonomy level is a distinct required user choice, show the path and actual depth, and add a crawlable hub shortcut where possible; no orphan pages; print the actual depth (hub → category → page is 2).
- Each individual page links to its category and to a few related pages that share a fact. No block of links to every sibling.
- The hub carries a table of all rows, including rows that are not built as pages.

## Batches

- Pilot: default min(N, max(20, ceil(0.05 × N))) pages, where N is the remaining eligible set; use min(N, supplied review capacity) when the user supplies a lower capacity, ensuring every supplied template/category is checked before its own expansion. State size, capacity constraint and coverage used.
- Default: each later batch is at most 2× the previous mature passing batch, capped by remaining eligible pages and supplied review capacity. Repeat the previous passing size when changing one observed page would cross a stop boundary. Failed or immature subgroups do not expand. State size, capacity and selected branch.
- Measurement window: default 8 weeks from publication for indexing, with a stated 8-week impression interval; use the user-specified window, or a longer maturation interval demonstrated by ages and repeated observations of supplied comparable successful cohorts. For supplied seasonal demand, use the relevant season. State window and dates; younger batches wait rather than fail.

Sitemaps per batch are a measurement choice (index coverage can be read per file), not a file-limit requirement; say so.

## Inputs per batch

Published pages, indexed pages, and indexed pages with no impressions in the window. A page that is not indexed cannot have impressions, so zero-impression pages are counted among indexed pages only.

Consistency check before any rule: indexed ≤ published, and indexed pages with no impressions ≤ indexed. If the user gives zero-impression pages over all published pages, convert: indexed with no impressions = given count − (published − indexed); if that is negative, the numbers cannot be right: say so and ask, without applying any rule.

## Stop rules per batch

| Rule | Stop when |
|---|---|
| Indexed share | default indexed/published <50% after the selected window |
| Zero-impression share | default confirmed-zero-impression indexed/indexed >=30% after the selected window |

Default: pause expansion after the selected window when indexed/published <50% or indexed-with-confirmed-zero-impressions/indexed >=30%. Use user-specified boundaries only when explicitly supplied before evaluating this batch; state the selected boundaries and preserve the < indexing and >= zero-impression operators. Do not infer new thresholds from past cohorts or loosen them because this batch fails. Use matching intended-indexable canonical URL cohorts and the stated impression dates; unavailable metrics are missing, not zero. Compare supplied subgroups separately and pause each failing subgroup. If published=0, there is no batch to evaluate. If indexed=0 and published>0, pause on indexing and report the second rate as undefined. State counts, denominators, window and deciding calculation after the answer-first verdict.

Continue only when neither rule fires. The counts say whether to pause, not why Google left pages out; never name a cause from counts alone; a sample check of the pages can show near-duplicates. Default: below 20 published pages, label the decision "small sample" and apply the gate to observed counts. Use "complete small cohort" when it is the entire planned eligible set. In either case, show the verdict after adding/removing one indexed page or one zero-impression page when that changes it; do not claim significance. State coverage and sensitivity used. If the batch is younger than the window, the verdict is conditional on the window; say so and ask how long the pages have been live.

## Rollback actions

1. Pause expansion and separate observed indexing and confirmed zero-impression outcomes; do not infer causes from counts. Require supplied page-level facts/sample text before URL changes.
   - Not indexed: improve missing row facts only when supplied evidence shows them; merge a duplicate/nonqualifying profile only with supplied page-level evidence. Do not expand that failing template. Noindex cannot help a page intended for indexing.
   - Indexed but no impressions after the window: hold for page-level review; zero impressions alone never mandate merge/noindex. Merge supplied duplicate/nonqualifying profiles only; retain a nonqualifying page needed by users with `noindex, follow`.
2. Keep noindexed pages crawlable (not blocked in robots.txt).
3. Rule of thumb of this plugin: a page left on `noindex, follow` for a long time may stop passing links; rows that will never be built belong in the hub table, not on noindexed pages.
4. Fix the template and check default 3 to 20; use all supplied 1 or 2 pages for a limited check (one has no pairwise score), or labelled groups of at most 20 for larger sets, covering known template variants and weak-data cases with cross-group checks of repeated profiles; state checked count, known total and uncovered variants, never whole-site clearance sample pages for near-duplicates.
5. Release the next batch only after the fixed batch passes.

# Prioritization rules

These rules decide the Impact field and the order of the top 5 and the fix plan. They are heuristics built on how search engines process a site (crawl, then render, then index, then rank), so problems earlier in that chain block everything after it.

## Order of areas

1. Indexing and server responses: important pages returning errors, carrying noindex, blocked by robots.txt, or canonicalized away.
2. Crawl and architecture: pages that cannot be discovered (missing from sitemap, no crawlable links, deep, orphaned), redirect chains, junk URL spaces.
3. Rendering: important content or links missing from the server HTML.
4. On-page: titles, headings, internal anchors.
5. Content: missing intent coverage, near-duplicate templates.
6. Structured data.
7. Performance (field data only).

## Impact

- **High**: prevents important pages (those tied to the business goal) from being crawled, rendered or indexed; or affects a whole template that carries the goal pages; or returns server errors on them.
- **Medium**: weakens how well important pages are understood or chosen (duplicate titles across a template, canonical conflicts, orphaned important pages, missing intent coverage), or wastes crawling on large sites.
- **Low**: cosmetic or marginal (a missing meta description on a minor page, alt text on decorative images).

An excluded URL that should stay excluded has no impact. A pattern marked "Might be intentional" gets its impact only after the owner confirms it is a mistake.

## Effort

- **S**: a config or template change, under a day.
- **M**: several templates or a content batch, a few days.
- **L**: architecture, platform or large content work, a sprint or more.

If the team size or stack is unknown, say the effort is an estimate.

## Ordering the top 5 and the plan

1. All High-impact indexing and server problems first, whatever the effort.
2. Then High impact with S or M effort.
3. Then the remaining quick wins. **Quick wins**: Medium or High impact, S effort, fitting within the user's stated capacity for the next 7 days. High-impact S items are already placed by step 2.
4. Everything else goes to "planned".

Tie-breaker: the change closest to the stated business goal wins.

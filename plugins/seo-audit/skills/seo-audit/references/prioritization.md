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

Preserve supplied effort in the user's units. Otherwise leave effort unknown unless implementation evidence supports a provisional estimate with stated assumptions. Separate hands-on effort, lead time, dependencies and risk. If S/M/L is useful, define it in the team's units; under a day, a few days and a sprint or more are optional planning examples, not estimates inferred from config/template/content/architecture labels. HTML evidence alone does not authorize an estimate.

## Ordering the top 5 and the plan

1. Keep confirmed causal blockers prominent for affected goal pages; repair them before downstream work that depends on them.
2. Rank independent work by affected business value, reach, expected benefit, confidence, dependencies, effort and risk.
3. Quick wins fit the user's capacity and planning horizon with supported effort; use a seven-day horizon only as an explicit fallback assumption. Unknown effort does not establish capacity fit.
4. Separate priority from commitment: retain important deferred blockers and permit useful independent work.

Tie-breaker: the change closest to the stated business goal wins.

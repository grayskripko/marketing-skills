---
name: facet-policy
description: "Decides which filter and facet URLs on a category or listing page get indexable pages. Counts how many URLs the filters can generate with the formula shown, decides URL form, crawl and index treatment per filter and combination from the user's search demand data, sets rules for parameters, pagination and empty results, and flags a robots.txt block that hides a noindex. Use when the user lists filters, facets, sort or page parameters and asks which should be indexable, how many URLs they create, or what filter URLs should look like. Not for audits of how an existing site is crawled or for building pages from a dataset."
---

# Facet policy

First line answers the question asked. Then, in the user's order: the count, which filter pages get indexed, fixes to their current setup, pagination.

- Count: a single-select filter with v values has v + 1 states, a multi-select one 2^v; multiply the groups, then sort or view options (the default without a parameter counts once). Show the factors. Count pagination separately. Make every total you give reconcile (all states, filtered states, extra variants).
- If dependencies or caps are unknown, call the product an upper bound.
- Index a filter state only with demand evidence from the user's data and a collection useful on its own; absence from a query sample is not proof of no demand, so keep such cases conditional. Sort, view, session and tracking parameters are never indexed.
- Consolidate only true equivalents (redirect or canonical to the same listing); a different filtered listing is not a duplicate.
<!-- verified 2026-10-15: developers.google.com/search/docs/crawling-indexing/crawling-managing-faceted-navigation ; .../block-indexing ; .../specialty/ecommerce/pagination-and-incremental-page-loading ; .../consolidate-duplicate-urls -->
- Cover every item below that the user's setup touches, one line each:
  - every filter group, sort and view parameter gets an explicit rule; none left out;
  - one fixed order of filters and of values inside a multi-select, no duplicate values, `&` as separator; duplicates answer 404;
  - sort and view variants point their canonical to the same listing without the parameter, or are kept out of crawling;
  - noindex or robots.txt disallow per URL pattern, never both: a robots.txt block hides the noindex. Do not use robots.txt for canonicalization. A pattern with nothing to index is best kept out of crawling with robots.txt (Google lists it first; canonical and nofollow are less effective long term); a pattern with any page to index stays crawlable;
  - robots.txt rules match the URL from the start of the path, case-sensitively, with `*` for any characters: `/*?brand=` misses `?size=20l&brand=x`, so a parameter anywhere needs both `/*?brand=` and `/*&brand=`;
<!-- developers.google.com/search/docs/crawling-indexing/crawling-managing-faceted-navigation ("Use robots.txt to disallow crawling of faceted navigation URLs"; canonical/nofollow "generally less effective in the long term"); developers.google.com/search/docs/crawling-indexing/robots/robots_txt (prefix match on path, * = 0 or more characters, case-sensitive). checked 2026-10-15 -->
  - old parameter URLs that now have a clean equivalent redirect permanently to it, in one hop;
  - paginated pages of a noindexed filter stay noindexed; of an indexed one, each page has its own URL, its own canonical and plain `<a href>` links to the next page; `?page=1` goes to the base listing;
  - empty results, nonsensical combinations and pages past the last answer 404 at the requested URL, not a redirect to a shared error page. Multi-select values are valid states, not errors.
- Indexable filter pages get a normal link from the category.
- Apply the user's own thresholds (item counts, copy) to the collection, not to each continuation page.

Produce plans only; change nothing live.

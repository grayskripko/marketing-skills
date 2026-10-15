---
name: facet-policy
description: "Decides which filter and facet URLs on a category or listing page get indexable pages. Counts how many URLs the filters can generate with the formula shown, decides URL form, crawl and index treatment per filter and combination from the user's search demand data, sets rules for parameters, pagination and empty results, and flags a robots.txt block that hides a noindex. Use when the user lists filters, facets, sort or page parameters and asks which should be indexable, how many URLs they create, or what filter URLs should look like. Not for audits of how an existing site is crawled or for building pages from a dataset."
---

# Facet policy

Answer in the user's order: the count, which filter pages get indexed, fixes to their current setup, pagination.

- Count: a single-select filter with v values has v + 1 states, a multi-select one 2^v; multiply the groups, then sort or view options (the default without a parameter counts once). Show the factors. Count pagination separately. Make every total you give reconcile (all states, filtered states, extra variants).
- If dependencies or caps are unknown, call the product an upper bound.
- Index a filter state only with demand evidence from the user's data and a collection useful on its own; absence from a query sample is not proof of no demand, so keep such cases conditional. Sort, view, session and tracking parameters are never indexed.
- Consolidate only true equivalents (redirect or canonical to the same listing); a different filtered listing is not a duplicate.
- A URL that relies on noindex must not be blocked in robots.txt, or the noindex is never seen.
- Pagination: each page has its own URL, its own canonical and plain `<a href>` links; `?page=1` goes to the base listing.
- Empty results and impossible combinations answer 404. Multi-select values are valid states, not errors.
- Indexable filter pages get a normal link from the category.
- Apply the user's own thresholds (item counts, copy) to the collection, not to each continuation page.

Produce plans only; change nothing live.

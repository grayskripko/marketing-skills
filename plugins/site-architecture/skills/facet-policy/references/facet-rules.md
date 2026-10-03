# Facet rules

## URL-space formula

- Single-select group with v values: v + 1 states (the +1 is "filter not applied").
- Multi-select group with v values: 2^v states (each value on or off, including none).
- Multiply the states of all filter groups.
- Sort or view with k options: multiply by k when the default option carries no parameter (k − 1 parameters plus the bare URL). If every option, default included, carries a parameter, the bare URL is a further state: multiply by k + 1. Say which case applies.
- Pagination: report separately; it multiplies again by the number of pages per listing.
- Worked check: single-select brand 8, RAM 4, GPU 6, screen 5, price 6 → 9 × 5 × 7 × 6 × 7 = 13,230 filter states; sort with 4 options, default without parameter → × 4 = 52,920 URLs before pagination (66,150 if all four options carried a parameter).
Google's URL guidance gives additive filtering as a typical way URL counts explode (G-url).

## Default decisions

| Case | URL form | Crawl | Index | Source |
|---|---|---|---|---|
| One filter value with demand in the user's data | clean path or stable parameter | allowed | index, own title and H1 | PR |
| Two or more filters, named in the demand data and passing the content gate | clean path or stable parameter | allowed | index | PR |
| Two or more filters, not named in the demand data | parameter or not a link | disallowed or allowed with canonical to the category | not indexed | heuristic of this plugin, from PR |
| Sort, view, session, tracking | parameter | disallowed | never indexed | G-url, G-page |
| Empty result | its own URL | — | answers 404 | G-facet |

## Rules sheet

| # | Rule | Source |
|---|---|---|
| F-01 | Parameters as `key=value`, joined with `&` | G-facet, G-url |
| F-02 | Filters always in one fixed order; the same filter never twice in a URL | G-facet |
| F-03 | A combination with no results answers 404 at its own URL, not a redirect to a shared error page; the same for duplicate or nonsense filters and pagination past the end | G-facet |
| F-04 | Ways Google lists to keep crawlers out of filter URLs: robots.txt disallow, filters in fragments, a canonical to the unfiltered page, nofollow on filter links. The plugin treats nofollow as the least dependable of these | G-facet; ranking is the plugin's own reading |
| F-05 | Each page of a paginated listing has its own URL and its own canonical, linked with `<a href>`; page 1 is not the canonical for the series | G-page |
| F-06 | A URL that relies on noindex must stay crawlable; a robots.txt disallow on it hides the noindex | G-noindex |
| F-07 | Indexable filter pages are reachable through a normal crawlable link from the category | G-links |

## Content gate

An indexable combination lists at least N items (asked; if not answered, "assumed 10, heuristic of this plugin") and has text of its own beyond the product grid (an introduction, buying notes, specific questions). Otherwise noindex. This is a quality rule: Google's spam policies on doorway pages and scaled content are the reason not to publish thin filter pages in bulk.

## Rename and merge table

| Current filter or value | Label in searchers' words | Action | Evidence |
|---|---|---|---|

Actions: rename, new (a demanded filter that does not exist), merge (synonym values), drop (no demand, no use). Evidence is the user's query and volume; without query data the table is "Needs verification". Queries that map to sort or view are listed with action "not a filter page" and no new page is proposed; a page for them is a content decision.

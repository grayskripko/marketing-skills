# Ticket template

```
### <ID>: <imperative title, e.g. "Remove noindex from product template">

- Findings: <finding IDs, or "user-reported">
- Why it matters: <what is being lost and the mechanism, in one or two sentences>
- Where: <URL pattern, template, or path/to/file:line>
- Change: <the exact change; a short code or config sketch if it helps>
- Owner: <developer | content | SEO | platform admin>
- Effort: <S | M | L> (<assumptions behind the estimate>)
- Depends on: <other ticket IDs, or none>
- Acceptance criteria:
  - <observable condition 1, e.g. "the product template's server HTML contains no robots noindex tag">
  - <observable condition 2, e.g. "robots.txt allows /product/">
- How to verify after release:
  - <check and tool, e.g. "URL Inspection on 3 sample product URLs shows indexing allowed">
  - <metric and when, e.g. "Page indexing report: indexed product URLs rise over 2–6 weeks">
```

## Writing rules

- Acceptance criteria are things someone can check in minutes: a tag present or absent, a status code, a URL in or out of the sitemap, a link present in server HTML. Not "SEO improved".
- One change per ticket. Group many URLs under one ticket only when one change fixes them all.
- Name the role, not a person.
- Use the team's words: "template", "component", "route", "CMS field" as the user describes their stack.
- No ranking or traffic promises. State the metric to watch and the expected direction.

## Example

```
### T-3: Make product links crawlable in category listings

- Findings: CRW-2, REN-1
- Why it matters: product cards navigate with a click handler on a div, so crawlers that follow only <a href> links cannot reach products from categories; products are found only through the sitemap, if at all.
- Where: components/ProductCard (category and search listings)
- Change: render the card's main link as <a href="/product/{slug}"> and keep the click handler for analytics only.
- Owner: developer
- Effort: S (one component; assumes no custom router constraints)
- Depends on: none
- Acceptance criteria:
  - Server HTML of /category/shoes contains <a href="/product/..."> for every listed product.
  - No product card uses href="#" or a non-anchor element for navigation.
- How to verify after release:
  - Fetch the category page source and count product links.
  - After 2–6 weeks: more product URLs listed as indexed in the Page indexing report; crawler export shows products at click depth 2–3.
```

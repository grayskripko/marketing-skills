# Ticket template

```
### <ID>: <imperative title, e.g. "Remove noindex from product template">

- From: <the finding number or a few words naming it, or "user-reported">
- Why it matters: <what is being lost and the mechanism, in one or two sentences>
- Where: <URL pattern, template, or path/to/file:line>
- Change: <the exact change; a short code or config sketch if it helps>
- Owner: <developer | content | SEO | platform admin>
- Effort: <S | M | L> (<assumptions behind the estimate>)
- Depends on: <known prerequisites; if unknown, say "confirm before pickup" rather than asserting none>
- Acceptance criteria:
  - <observable condition 1, e.g. "the product template's server HTML contains no robots noindex tag">
  - <observable condition 2, e.g. "robots.txt allows /product/">
- How to verify after release:
  - <check and tool, e.g. "URL Inspection on 3 sample product URLs shows indexing allowed">
  - <only relevant follow-up, conditional on available access; inspect indexed status after recrawl, with no fixed window unless monitoring was requested>
```

## Writing rules

- Acceptance criteria are observable outcomes appropriate to the change: tags, status codes, sitemap membership or server-HTML links for technical work; supported factual coverage, intended-reader utility and editorial review for content work. State necessary expertise and review dependencies. Do not use "SEO improved" as release acceptance.
- One change per ticket. Group many URLs under one ticket only when one change fixes them all.
- Name the role, not a person.
- Use the team's words: "template", "component", "route", "CMS field" as the user describes their stack.
- Preserve supplied effort estimates and mark new estimates as provisional with assumptions. Unknown dependencies remain unknown.
- Verify every changed rule/template and high-risk route, locale and state. Use exhaustive automated population checks when feasible; otherwise justify representative samples for large route inventories and state remaining coverage limits, including shared-template regressions. Do not require Search Console access or indexing requests unless available or explicitly conditional. Add sitemap work only when the finding or release changes the sitemap.
- No ranking, indexing or traffic promises. Later monitoring is optional unless requested; any suggested window is a rule of thumb, not a deadline.

## Example

```
### T-3: Make product links crawlable in category listings

- From: findings 2 and 5 (links in a click handler; listings rendered by JavaScript)
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
  - If indexed-state monitoring was requested and Search Console access exists, inspect product index status after evidence of recrawl. Choose any comparison window from available comparable data. Verify crawlable product links against the supplied navigation structure; do not assume a universal click depth or recovery date.
```

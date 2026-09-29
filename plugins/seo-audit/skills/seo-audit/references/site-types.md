# What to weigh by site type

Use this to choose which templates to sample within the 10-page cap and which checks to weigh more. Weightings are heuristics based on how these sites usually fail, not rules from a search engine.

## SaaS and B2B services
- Sample: homepage, pricing, one feature or solution page, one integration or use-case page, one blog article, the demo or contact page.
- Weigh more: title and heading intent match on feature and solution pages; pricing page indexable; client-side rendering in marketing sites built as single-page apps; comparison and use-case pages missing for queries buyers use; blog pages cannibalizing product pages.
- Common deliberate patterns: app login and dashboard blocked or noindexed.

## E-commerce
- Sample: homepage, a top category, a filtered category URL, a product page, an out-of-stock product if the user points one out, the sitemap.
- Weigh more: product URLs present in the sitemap; faceted navigation and sort parameters generating indexable duplicates; canonical on variants; Product structured data matching visible price and availability; internal search pages open to indexing; pagination links crawlable.
- Common deliberate patterns: filter combinations noindexed; cart, checkout and account blocked.

## Local business
- Sample: homepage, each location page (up to the cap), a service page, contact page.
- Weigh more: one page per location with unique content, address and opening hours in text; LocalBusiness structured data consistent with the page; name, address and phone consistent across pages.

## Publisher and blog
- Sample: homepage, a category or tag page, two articles from different sections, an author page.
- Weigh more: article titles and headings; date signals; author information; tag and archive pages creating thin duplicates; pagination; Article structured data; large volumes of near-identical pages.
- Common deliberate patterns: tag pages noindexed.

## Marketplace and programmatic sites
- Sample: two or three pages from the same generated template, plus the listing page above them.
- Weigh more: template boilerplate share; empty or near-empty generated pages (zero results) answering 200; sitemap volume versus pages worth indexing; internal linking between generated pages.

## Multilingual and multi-regional
- Sample: the same page in two or three language versions, plus the language selector.
- Weigh more: hreflang return links and codes; canonical not pointing across languages; automatic redirects by IP or browser language; translated titles and descriptions actually present.

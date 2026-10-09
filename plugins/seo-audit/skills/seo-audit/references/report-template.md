# Site audit report template

Leave out any section with nothing in it. Keep "Not checked" if a check that could change the top changes was not possible.

```
# SEO audit: <site or section>, <date>

<One sentence: is anything keeping key pages out of the index? If the goal was assumed, one line saying which.>

## Top changes
1. <Short title>
   - Where: <URL pattern or template>
   - What is being lost and why: <the mechanism, e.g. "product pages are not in the sitemap and only reachable through a JavaScript filter, so new products are found late or not at all">
   - Action: <the change>
   - Who: <developer / content / SEO>
   - Metric to watch: <e.g. indexed product pages in the Page indexing report; clicks to /product/* in Search Console>

## Findings
<table or list in the shared finding format, sorted by impact, then effort>

## What not to do now
- <tempting work that will not move the goal yet> — <one-line reason>

## Not checked
- <check> — <why it was not possible> — <how to check it: tool and step>

## Scope
- HTML pages fetched (<n> of 10): <URLs>
- robots.txt and sitemaps read: <list>
- Data provided by the user: <exports, or "none">
- Assumptions: <only those that would change the answer if wrong>

I can turn these into developer tickets with acceptance criteria. If you have Search Console or crawler exports, share them for a review with fixed thresholds.
```

## Writing rules

- Plain sentences. State the evidence, not adjectives.
- No promises about rankings or traffic. Describe the mechanism and the metric to watch.
- Every top change must come from at least one finding.
- If fewer than five changes are worth making, list fewer.

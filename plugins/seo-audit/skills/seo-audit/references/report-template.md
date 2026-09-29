# Site audit report template

Fill every section. If a section is empty, write "None found" or "Not applicable" and say why, so the reader knows it was considered.

```
# SEO audit: <site or section>, <date>

## 1. Scope
- Goal: <the one business goal>
- Site type, market, language: <...>
- Constraints: <developer time, frozen templates, deadlines>
- HTML pages fetched (<n> of 10): <list of URLs>
- robots.txt and sitemaps read: <list>
- Data provided by the user: <exports, or "none">
- Assumptions: <everything assumed rather than seen>

## 2. Top 5 changes
For each:
1. <Short title>
   - Where: <URL pattern or template>
   - What is being lost and why: <the mechanism, e.g. "product pages are not in the sitemap and only reachable through a JavaScript filter, so new products are found late or not at all">
   - Action: <the change>
   - Who: <developer / content / SEO>
   - Metric to watch: <e.g. indexed product pages in the Page indexing report; clicks to /product/* in Search Console>
   - Findings covered: <IDs>

## 3. Findings
<table in the shared finding format, sorted by impact, then effort>

## 4. What not to do now
- <tempting work that will not move the goal yet> — <one-line reason>

## 5. Not checked
- <check> — <why it was not possible> — <how to check it: tool and step>

## 6. Next steps
- Turn findings into developer tickets with acceptance criteria.
- If you have Search Console or crawler exports, share them for a data review with fixed thresholds.
```

## Writing rules

- Plain sentences. State the evidence, not adjectives.
- No promises about rankings or traffic. Describe the mechanism and the metric to watch.
- Every top-5 item must be traceable to at least one finding ID.
- If fewer than five changes are worth making, list fewer and say so.

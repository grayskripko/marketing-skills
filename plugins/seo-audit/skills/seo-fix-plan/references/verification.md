# Verification after release

Use this reference to write applicable post-release checks into tickets for the named owner. Do not fetch, submit indexing requests, resubmit sitemaps or edit links while generating the plan. Executing those steps belongs to a separately authorized task. Include only checks that apply to the supplied findings and requested deliverable. For next-week tickets, live source, headers, status and links normally establish release acceptance. Recrawl requests, sitemap maintenance and later metric windows below are optional follow-up guidance; require access or state the condition, and never add a new fix without evidence.

## Recrawl sequence for changed key pages

Search engines pick up changes at their own pace. These steps make the change discoverable; none of them forces indexing.

1. Confirm the change is live: fetch the page source (not the browser's rendered view) and check the tag, status or link the ticket changed.
2. Make sure the server sends accurate modification signals: the sitemap `lastmod` for the changed URLs reflects the real change date, and if the server sends `Last-Modified` headers, they are accurate.
3. Resubmit the sitemap in Search Console if the sitemap itself changed.
4. For a handful of the most important URLs, request indexing through URL Inspection in Search Console. This has a daily quota and is for a few URLs, not bulk.
5. Link to the changed pages from pages that are crawled often (homepage, main categories, a recent article), if they are not already linked.

## When to look and what counts as success

The windows below are optional monitoring heuristics, not default deliverables or evidence about this site. Include a calendar only when requested, label its assumptions and check tool access. Otherwise verify the release immediately and suggest indexed-state inspection after recrawl where relevant, without a fixed week range. A canonical remains a strong hint, not a guarantee of Google's selection.

| Change | Check right after release | Look again | What to look for (not guaranteed) |
|---|---|---|---|
| noindex removed, robots.txt unblocked, canonical fixed | Page source; robots.txt; URL Inspection live test | 1–4 weeks | URL Inspection shows the page indexed with the expected canonical; Page indexing report counts move |
| Pages added to the sitemap, links made crawlable | Sitemap content; page source | 2–6 weeks | Sitemap report shows URLs discovered; indexed count for that page type rises |
| Soft 404s and error pages fixed | Status codes for sample URLs | 2–6 weeks | Soft 404 and error counts fall in the Page indexing report |
| Redirect chains shortened | Status and target for sample URLs | 2–4 weeks | Crawler export shows single-hop redirects |
| Titles and on-page changes | Page source | 3–8 weeks | Impressions and CTR for the target queries in Search Console, compared with an equal period and checked against known data anomalies |
| Content improvements | Page source | 4–12 weeks | Clicks and position for the target query group |
| Performance fixes | Lab test for the change itself | 4+ weeks | Field data (CrUX is a rolling 28-day window) in the Core Web Vitals report |

Always compare clicks, not only impressions, when a period touches a known Search Console reporting anomaly.

## Re-audit checklist

- The same sample pages fetched again: status, robots meta, canonical, title and main heading match the tickets' acceptance criteria.
- robots.txt and sitemap re-read: no new blocks, key page types present, no errors listed.
- Page indexing report: counts for the statuses the tickets targeted.
- Performance export for the target pages and queries: clicks, impressions, CTR and position against the baseline period.
- New pages or templates released since the last audit, added to the sample.
- Any ticket whose success signal did not appear after its "look again" window goes back to investigation, with the evidence.

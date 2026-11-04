# Watch list for a site change near a Google update

Pick the items for the user's change type. Each item is a check the user can do in their own tools; none needs this plugin.

## Before (any change)

- Write down the change date and the rollout status that day; add an annotation in analytics.
- Save a baseline: 28 days of Search Console clicks, impressions and average position by page group (folder or template), the indexed page count, the top 50 queries, and analytics organic sessions for the same days. If a rollout fell inside those 28 days, also save a baseline from before it began.
- Pick a control: pages or sections the change does not touch. If the control and the changed pages move together, the cause is more likely outside the site (an update or seasonality); if only the changed pages move, more likely the change.

## Launch of a new site or section

- During: the new URLs in the Search Console Page indexing report (indexed or not, and why); the sitemap read without errors; URL Inspection on 5 to 10 main pages; robots rules and noindex tags checked on the live site, not only on staging.
- After: impressions for the new pages start before clicks do; judge clicks only after impressions settle.

## Domain move, platform switch or mass URL change

- Before: a full list of old URLs with their traffic; a redirect map from each old URL to one new URL.
- Day 1 to 3: a sample of old URLs (top traffic first) answers with a single redirect to the right new page; the new sitemap submitted; for a domain move, the Change of Address tool in Search Console.
- Week 1 to 4: indexed count of the new URLs rising as the old falls; Crawl stats (response codes, host status); 404s and redirect errors on old URLs; the share of clicks still landing on old URLs.
- After: compare old-plus-new traffic per page group with the baseline, not the new site alone; expect weeks, not days, before judging a large move.

## Redesign or template change

- During: titles, headings, internal links, structured data and indexable text on the main templates match the old ones, or changed on purpose; compare a sample of rendered pages before and after; the rich result reports in Search Console show no new errors.
- After: Core Web Vitals field data in Search Console covers 28 days, so it reflects the redesign about a month later.

## Content pruning or consolidation

- Before: list the removed pages with their clicks and links; decide redirect or removal per page.
- After: removed URLs either redirect to a close match or return 404 or 410 on purpose; compare the kept pages' traffic with the baseline; check that removed pages leave the index; watch the queries the removed pages used to rank for.

## SEO or A/B test

- Note whether the test window overlaps a rollout. Mark the rollout days as excluded or extend the test; compare test and control groups on the same days only.

## During a rollout (any change)

- Re-check the status every few days; note the day the rollout ends.
- Do not judge the change on daily figures during the window; look at week-over-week by page group, changed pages against the control.

## After the rollout ends

- Wait about one more week (a measurement habit, not a Google rule), then compare the 28 days after with the baseline, by page group, changed pages against the control.
- Split the analysis at the rollout end: compare the baseline with the days after the end, not with the rollout days.
- Before blaming the change or the update for a drop, check the dates against Google's update list and the Search Console data anomalies for those days (the traffic-drop check does this).

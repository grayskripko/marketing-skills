# Map checks, fallback fate and launch checklist

## Map checks M-01 to M-10

| Id | Check | Pass when | Source |
|---|---|---|---|
| M-01 | Chains | every old URL points straight at its final URL. Google follows up to 10 hops, yet asks for short chains: ideally no more than three and fewer than five. This plugin collapses every chain to a single hop | G-move |
| M-02 | Loops | 0 loops (A → B → A, or longer) | G-move |
| M-03 | Bad targets | no target is itself an old URL, a 404/410, or noindexed (when status data is given) | G-move |
| M-04 | Many-to-one | several old URLs share one target only when they were merged into it; Google asks for one-to-one mapping except for consolidation | G-move |
| M-05 | Homepage targets | unrelated old pages do not point at `/`; such redirects may be treated as soft 404s. Any must-map URL pointed at `/` fails, and the closest page is proposed | G-move, G-404 |
| M-06 | Temporary codes | permanent moves use a permanent redirect (301 or 308), not 302 or 307 | G-redir |
| M-07 | Variants | case, trailing-slash, `index.html` and parameter variants of old URLs are covered by a rule | convention of this plugin; G-url says Google treats `/APPLE` and `/apple` as two URLs |
| M-08 | Target exists | every target is in the new structure or marked NEW | rule 3 |
| M-09 | Must-map coverage | every old URL with clicks or backlinks has a row | G-move |
| M-10 | Unresolved fate | rows lacking a decided fate are explicitly unresolved; no fate is assigned from clicks/backlinks alone | this file |

Slug collisions (two different old pages whose new paths would be the same) are reported under M-04 unless they are a declared merge.

## Missing fate

Preserve decided fates. Otherwise leave the row unresolved and ask for keep/move/merge/remove intent; unknown metrics are not zero. Use clicks/backlinks only to prioritize verification. A redirect requires an evidenced equivalent; an approved removal with no replacement returns the decided 404/410. Never redirect an unrelated page to the homepage. Continue decided rows while flagging the unresolved ones.

## Launch checklist (G-move unless marked)

1. Mapping file complete for every old URL with traffic or links.
2. Internal links, canonicals, hreflang annotations and sitemaps point at the new URLs before launch; a sitemap of the new URLs is ready to submit at launch.
3. Development blocks (noindex, robots.txt disallow, password) removed from the new URLs at launch.
4. One kind of change at a time where possible (domain, CMS, layout).
5. Choose rollout sequencing from deployment, testing and rollback constraints, not page count alone. Offer a sequencing recommendation only when requested or required for implementation.
6. Change of address in Search Console only for a domain or subdomain change; "not applicable" for path or folder changes on the same host.
7. Keep the redirects for at least one year, longer if links still arrive.
8. Expect rankings to fluctuate while Google processes the move; for small and medium sites, most pages take a few weeks. No percentage is predicted (rule 5).

## Watch list

Illustrative low-risk schedule only. Verify statuses and targets at launch and immediately after. Adapt later windows to risk, crawl activity, export latency, seasonality and each deployment cohort; compare comparable periods and extend observation when evidence is insufficient.

| When | Compare (from the user's exports) |
|---|---|
| week 1 | old URLs still answering 200; 404s among must-map URLs; new URLs crawled |
| weeks 2 to 4 | indexed count of new vs old URLs; impressions by section, old vs new paths |
| weeks 8 to 12 | clicks by section against the same weeks before the move; remaining redirect hits from internal links |

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
| M-07 | Variants | case, trailing-slash, `index.html` and parameter variants of old URLs are covered by a rule | G-url |
| M-08 | Target exists | every target is in the new structure or marked NEW | rule 3 |
| M-09 | Must-map coverage | every old URL with clicks or backlinks has a row | G-move |
| M-10 | Fallback rows | rows decided by the fallback below are counted and labelled | this file |

Slug collisions (two different old pages whose new paths would be the same) are reported under M-04 unless they are a declared merge.

## Fallback when fate is missing (heuristic of this plugin)

Used only when the user, a content review or the hand-off list gives no fate:
- no clicks and no backlinks → 404 or 410 (Google currently treats them the same; G-404);
- otherwise → 301 to the closest equivalent page, once its content covers the old page's subject (PR);
- never the homepage.
Print: "deciding which pages to keep is a content decision; settle fate first if you have not".

## Launch checklist (G-move unless marked)

1. Mapping file complete for every old URL with traffic or links.
2. Internal links, canonicals, hreflang annotations and sitemaps point at the new URLs before launch; a sitemap of the new URLs is ready to submit at launch.
3. Development blocks (noindex, robots.txt disallow, password) removed from the new URLs at launch.
4. One kind of change at a time where possible (domain, CMS, layout).
5. Small sites can move at once; large sites may move section by section.
6. Change of address in Search Console only for a domain or subdomain change; "not applicable" for path or folder changes on the same host.
7. Keep the redirects for at least one year, longer if links still arrive.
8. Expect rankings to fluctuate while Google processes the move; for small and medium sites, most pages take a few weeks. No percentage is predicted (rule 5).

## Watch list

| When | Compare (from the user's exports) |
|---|---|
| week 1 | old URLs still answering 200; 404s among must-map URLs; new URLs crawled |
| weeks 2 to 4 | indexed count of new vs old URLs; impressions by section, old vs new paths |
| weeks 8 to 12 | clicks by section against the same weeks before the move; remaining redirect hits from internal links |

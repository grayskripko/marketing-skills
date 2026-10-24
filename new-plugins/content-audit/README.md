# Content Audit

Decide which old blog posts to keep, update, merge, redirect or delete in a content audit, content refresh or content pruning review of stale content.
For content owners and editors reviewing existing public pages. Needs pasted page lists and notes, or Google Search Console, GA4 and crawler CSV exports. No accounts, paid APIs or installation beyond the plugin are required.

| Skill | Input | Output |
|---|---|---|
| audit-content | Page list, content notes, search/analytics/crawler exports | Per-URL decisions first, reasons and next edits |
| refresh-content | Existing page text, approved current facts, optional performance exports | Exact editorial changes, retained exceptions and publication checks |
| merge-content | Overlapping pages, chosen survivors, links and crawler records | URL map first, content moves and rollout checks |

Ask “Which old blog posts should I update, merge or delete?”, “What should the editor change in this outdated guide?” or “Merge these articles and preserve old reader links.” Sparse lists get conditional decisions; page text and complete exports make decisions firmer. Old age and low traffic do not automatically mean delete.

Export setup: in Search Console's Search results report, choose the date range, search type and filters, then export page performance; export a comparable earlier period. In GA4, export a Landing page report with sessions, key events, date range and channel filters. From your crawler, export URL, status, redirect destination, canonical, indexability, title and internal links. Include content notes and backlink/referral evidence when deciding removals. UI labels may vary; the assistant can guide the export steps. Never provide passwords or access tokens. Pasted page text and lists are the no-setup path.

Reads files or text you supply. No live Google account connection or site changes. Offline by default. Only when you explicitly request current documentation verification, the assistant may fetch the ten exact Google documentation URLs listed in [PRIVACY.md](PRIVACY.md) and each skill's sources file. It does not fetch your listed pages, robots.txt, sitemaps, account APIs or linked destinations outside that list, or send your exports, private URLs or conversation data to search services. Local file parsing is allowed. No telemetry or plugin storage.

Thresholds are adjustable review defaults with exceptions, not Google deletion rules. Merge plans preserve useful content and working link destinations; results must be measured after rollout.

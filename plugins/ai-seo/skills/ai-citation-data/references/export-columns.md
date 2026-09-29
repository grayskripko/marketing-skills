# Export columns and where to find each report

Column names differ between interface languages, export paths and product updates. Map columns by meaning, confirm the mapping with the user when unsure, and ask for the header row if nothing matches. Report descriptions below were read on 2026-09-29.

## Bing Webmaster Tools: AI Performance

What it covers: how often pages from the site are shown as sources in AI-generated answers across Microsoft Copilot, AI summaries in Bing and some partner integrations (public preview announced 2026-02-10; intents, topics, citation share and compare added in a global preview announced 2026-06-16).

| Meaning | Likely column names |
|---|---|
| Page URL | Page, URL, Cited page |
| Citations for the page or query | Citations, Total citations |
| Grounding query (the phrase the system used when retrieving the cited content) | Grounding query, Query |
| Citation share (the site's share of all citations shown for that grounding query) | Citation share |
| Intent class of the grounding query | Intent |
| Topic cluster | Topic |
| Date or period | Date |

Where: Bing Webmaster Tools, the site's property, AI Performance. If the report offers a download, use it; otherwise copy the table from the screen. Grounding queries are a sample of citation activity, per Bing.

## Google Search Console: generative AI performance reports

What it covers: impressions of the site's URLs inside generative AI features in Search (such as AI Overviews and AI Mode) and in Discover (announced 2026-06-03 at https://developers.google.com/search/blog/2026/06/gen-ai-performance-reports; a note at the top of that post says the insights were rolled out to all websites worldwide as of 2026-08-31).

| Meaning | Likely column names |
|---|---|
| Page URL | Page, Top pages, URL |
| Impressions in generative AI features | Impressions |
| Country | Country |
| Device (Search only) | Device |
| Date | Date |

Where: Search Console, the property, the generative AI performance report for Search (or for Discover). The report shows impressions only, no clicks. If the user exports it and the file has one table per dimension, ask which table they sent; this is common for Search Console exports but not documented for this report.

## Google Analytics 4: AI Assistant channel

What it covers: sessions whose referrer matches Google's list of AI assistants. GA4 sets the medium to `ai-assistant` and the campaign to `(ai-assistant)` for them, and groups them in the default channel called AI Assistant. Google's channel description says it excludes Google's AI Overviews and AI Mode.

| Meaning | Likely column names |
|---|---|
| Channel | Session default channel group, Default channel group |
| Source | Session source, Source |
| Landing page | Landing page, Landing page + query string |
| Sessions | Sessions |
| Conversions | Key events, Conversions |

Where: GA4, Reports, Acquisition, Traffic acquisition, with the channel dimension; add landing page as a secondary dimension. No setup is needed for the default channel.

## Page value list (optional, from the user)

Any table with a page URL and one value column: conversions, pipeline, revenue, sign-ups, or the user's own score. The user names the value column; otherwise the skill uses conversions, then clicks, then sessions, and says which.

## URL normalization before joining

1. Lower-case the scheme and host; drop `www.` only if the user confirms both hosts serve the same site.
2. Treat `http` and `https` as the same page.
3. Remove the fragment (`#...`) and a trailing slash (except for the root `/`).
4. Remove tracking parameters: `utm_*`, `gclid`, `fbclid`, `msclkid`, `mc_cid`, `mc_eid`, `ref`.
5. Keep other query parameters; they may be different pages.

List URLs that did not join after normalization, with the likely reason.

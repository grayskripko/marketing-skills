# Data caveats

After the priority list, name only the caveats that apply to the user's files, in a few lines. Sources were read on 2026-09-29.

## Bing Webmaster Tools: AI Performance

- Citation share is the percentage of citations attributed to the site out of all citations shown for the same grounding query. Bing describes it as an observational metric: not a ranking, not a competitive scoreboard, not traffic share, and it does not show competitor domains. Source: Bing Webmaster blog, "New AI Visibility Insights in Bing Webmaster Tools: Intents, Topics, Citation Share, Compare" (2026-06-16).
- Citation counts show how often pages are referenced, not where they appear inside an answer or how important they are. Grounding queries are a sample. Source: Bing Webmaster blog, "Introducing AI Performance in Bing Webmaster Tools Public Preview" (2026-02-10).
- Intents and topics come from machine classification in preview; labels can be broad, especially for niche sites (same June 2026 post).
- The report covers Microsoft Copilot, AI summaries in Bing and some partner integrations, not every AI engine.
- Shares for grounding queries that contain the brand name, or that are navigational, are expected to be high; they are set aside before comparing pages (see `prioritization.md`).

## Google Search Console

- Appearances in AI Overviews and AI Mode are counted inside the Web search type of the standard Performance report, with no separate filter there. Source: Google Search Central, "AI features and your website" (last updated 2025-12-10).
- The generative AI performance reports show impressions in generative AI features, by page, country, device (Search only) and date; there are no clicks in them, and the same data also stays inside the overall Performance report. Source: Google Search Central blog, "Introducing Search Generative AI performance reports in Search Console", https://developers.google.com/search/blog/2026/06/gen-ai-performance-reports (published 2026-06-03). A note at the top of that post says that as of 2026-08-31 the insights were rolled out to all websites worldwide.
- A logging error affected impressions reported in the generative AI Search report from 2026-08-13 to 2026-08-17; Google reported the data restored on 2026-08-21. Re-export files pulled before that date. Source: Search Console Help, "Data anomalies in Search Console".
- Impressions in Search performance were not reported accurately from 2025-05-13 to 2026-04-27 because of a logging error; do not compare impressions across that boundary. Same source.

## Google Analytics 4

- The AI Assistant channel counts sessions from referrers on Google's list of AI assistants. Google's channel description says it excludes AI Overviews and AI Mode. Source: Analytics Help, "[GA4] Default channel group".
- Visits from AI answers that pass no referrer (for example, some app or copied-link visits) land in Direct, so the channel undercounts.

## General

- None of these reports shows a brand's mentions without a link. Mentions are measured only by the prompt panel.
- Compare equal-length periods with the same settings. Re-measure no earlier than 4 weeks after changes ship (heuristic).
- Never convert citations or impressions into traffic, revenue or ranking claims.

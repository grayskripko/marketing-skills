# Myths and unverified claims

The skills in this plugin do not report the items below as problems and do not recommend them as fixes. If the user raises one, answer in one or two plain sentences and name the source. Sources were read on 2026-09-29; the page dates are given so the user can check for updates.

## Claims contradicted by primary sources

| Claim | What the source shows, in short | Source |
|---|---|---|
| Google needs special files, markup or optimizations for AI Overviews and AI Mode | Google states there are no additional requirements or special optimizations; normal Search guidance applies, and the page must be indexed and eligible for a snippet. | Google Search Central, "AI features and your website", developers.google.com/search/docs/appearance/ai-features (last updated 2025-12-10) |
| Adding JSON-LD structured data gets a page cited more in AI answers | Ahrefs compared 1,885 pages that added JSON-LD between August 2025 and March 2026 with 4,000 matched control pages. AI Overview citations fell 4.6% relative to controls (small but statistically significant); the AI Mode (+2.4%) and ChatGPT (+2.2%) changes could not be told apart from zero. The study covered pages that were already heavily cited. Structured data stays useful for rich results and clear entity information. | ahrefs.com/blog/schema-ai-citations/ (published 2026-05-11) |
| Ranking in the top 10 means being cited in AI Overviews | In Ahrefs' 2026 analysis of 863K results pages, 37.9% of URLs cited in AI Overviews also appeared in the first 10 results. An earlier Ahrefs study (July 2025) found about 76% of cited pages in the original results page; the method differs, so treat the comparison as direction only. | ahrefs.com/blog/ai-overview-citations-top-10/ (published 2026-03-02) |
| One check shows how visible a brand is in AI answers | Ahrefs observed AI Overview content changing about every 2.15 days on average, with about 45.5% of cited sources new when an overview changed. Single checks are snapshots; measure per engine with repeated runs. | ahrefs.com/blog/ai-overview-change/ (published 2025-11-11) |
| Blocking Google-Extended removes a site from AI Overviews | Google-Extended is a separate token that controls use of content for training Gemini models and for grounding in some other Google systems. Access for Search, including its AI features, is governed by Googlebot rules, and what is shown is limited with nosnippet, data-nosnippet, max-snippet or noindex. | Google Search Central, AI features page (2025-12-10) and "Google's common crawlers" |
| Changing a page's date makes it look fresh | Google's guidance on people-first content lists changing dates without substantial changes as a practice to avoid. Visible dates should match real edits. | Google Search Central, "Creating helpful, reliable, people-first content" |
| FAQ markup brings FAQ rich results | FAQ rich results stopped appearing in Google Search from 2026-05-07. | Search Console Help, "Data anomalies in Search Console" |
| Hidden instructions to AI systems in a page help a brand get recommended | Hidden text placed to manipulate search systems is a spam-policy violation, and this plugin treats any AI-directed text as a risk. | Google Search Central, "Spam policies for Google web search" (hidden text and link abuse) |
| A self-ranking "best X" list is neutral content | Presenting a list the brand wrote about itself as independent is misleading to readers. Earning a fair place in independent lists is the honest route. | Reasoning, no statistic |

## Claims with no documented support

- **llms.txt gets a site cited.** None of the major AI answer engines documents using an llms.txt file to choose or cite sources. It is optional; its absence is never a finding.

## Unverified or limited evidence

- **AI assistants ignore JSON-LD when they read a page.** searchVIU tested one purpose-built page in October 2025 (published 2025-12-02) and found that the tested assistants used only visible HTML during a direct fetch. This is a single-page experiment about direct fetching only; systems that work from a search index may still use structured data. Mention it only with that limit.
- **Theories built on leaked internal search documents, patents or single-site experiments** (for example fixed freshness windows or numeric authority scores). Never use them as the reason for a finding. If asked, say they are not confirmed and describe what can actually be measured.
- **Correlations reported as causes.** Ahrefs found YouTube mentions correlate with brand visibility in AI answers (Spearman about 0.737 in its study of 75,000 brands, similar across ChatGPT, AI Mode and AI Overviews) and states that correlation is not causation (ahrefs.com/blog/ai-brand-visibility-correlations/, published 2025-12-12). Use such figures as context, never as a decision rule.

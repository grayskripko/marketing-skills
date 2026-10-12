# AI crawler purposes and controls

Reviewed 2026-10-12. Vendor-declared behaviour, not an independent compliance audit. Re-check the source before changing a live robots file.

| Token | Purpose | Effect and limits of blocking |
|---|---|---|
| `OAI-SearchBot` | ChatGPT search discovery | Disallow excludes the site from ChatGPT search answers; navigational links may remain. Changes may take about 24 hours. |
| `GPTBot` | Content potentially used for OpenAI model training | Disallow says content should not be used for that training. Independent of OAI-SearchBot search permission. |
| `ChatGPT-User` | Visits a user asks ChatGPT to make | robots.txt rules may not apply; it does not decide search inclusion. |
| `PerplexityBot` | Perplexity search discovery | Disallow stops its compliant search crawl; Perplexity recommends allowing it for search visibility. Not a training crawler. No promise of immediate removal of known URLs. |
| `Perplexity-User` | User-directed fetches | Generally ignores robots.txt. Not a training crawler. |
| `Claude-SearchBot` | Claude search indexing | Disallow prevents its search indexing and may reduce visibility in Claude search answers. |
| `ClaudeBot` | Potential training collection | Disallow excludes future material under Anthropic's policy; does not erase past training. |
| `Claude-User` | Retrieval a Claude user asks for | Disallow prevents retrieval for user queries under Anthropic's policy. |
| `Googlebot` | Google Search, including AI Overviews and AI Mode | Blocking it blocks Search too; there is no AI-only opt-out for Search. Supporting links in AI features need indexed, snippet-eligible pages; `nosnippet`, `data-nosnippet` and `max-snippet` apply. |
| `Google-Extended` | Gemini training and grounding in Gemini Apps and Vertex AI | Control token only (no separate user agent). Does not affect Google Search inclusion or ranking; blocking it can affect Gemini grounding. |
| `bingbot` | Bing indexing, which Copilot answers draw on | Blocks Bing crawling; removal from results needs a readable `noindex`, not only a robots block. |

## Sources

- OpenAI crawlers and IP lists (`searchbot.json`, `gptbot.json`, `chatgpt-user.json`): https://developers.openai.com/api/docs/bots (no update date shown; reviewed 2026-10-12)
- Perplexity crawlers and IP lists: https://docs.perplexity.ai/docs/resources/perplexity-crawlers (no update date shown; reviewed 2026-10-12)
- Anthropic crawler policy (dated 2026-04-07): https://privacy.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler ; IP list https://claude.com/crawling/bots.json
- Google common crawlers, Google-Extended scope (updated 2026-07-14): https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers
- Google AI features and your website (updated 2025-12-10): https://developers.google.com/search/docs/appearance/ai-features
- Verifying Google requests (updated 2026-03-20): https://developers.google.com/crawling/docs/crawlers-fetchers/verify-google-requests
- Robots Exclusion Protocol, RFC 9309 (September 2022): https://www.rfc-editor.org/rfc/rfc9309.html

## Example: allow AI search, limit training

Added to an existing file, keeping its `*` group, private-path exclusions and Sitemap lines (copy the needed `Disallow` lines into each new group):

```text
User-agent: OAI-SearchBot
Allow: /

User-agent: GPTBot
Disallow: /

User-agent: PerplexityBot
Allow: /

User-agent: Claude-SearchBot
Allow: /

User-agent: Claude-User
Allow: /

User-agent: ClaudeBot
Disallow: /

User-agent: Google-Extended
Disallow: /
```

`Allow: /` here is not advice to expose private paths. A robots rule cannot fix a CDN or firewall block; check the logs for that.

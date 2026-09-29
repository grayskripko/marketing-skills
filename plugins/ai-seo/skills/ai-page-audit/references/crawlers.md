# AI crawlers and controls

Agent names and purposes come from each vendor's own documentation, read on 2026-09-29. Vendors add and rename agents; check the linked pages before advising a change.

| Vendor | robots.txt token | Purpose | Effect of disallowing it | Source |
|---|---|---|---|---|
| OpenAI | OAI-SearchBot | Search: surfaces sites in ChatGPT's search features | The site is not shown in ChatGPT search answers (may still appear as a navigational link) | developers.openai.com/api/docs/bots |
| OpenAI | ChatGPT-User | User-triggered visits when a user asks something | OpenAI says robots.txt rules may not apply because the visit is user-initiated; it does not decide search inclusion | same |
| OpenAI | GPTBot | Crawling for training generative models | Content is marked as not to be used for training | same |
| Anthropic | Claude-SearchBot | Search: improves search result quality | Content is not indexed for search, which may reduce visibility in user search results | support.claude.com, "Does Anthropic crawl data from the web, and how can site owners block the crawler?" |
| Anthropic | Claude-User | User-triggered retrieval when a user asks a question | Content is not retrieved for user queries | same |
| Anthropic | ClaudeBot | Collecting content that may be used for training | Future content is excluded from training data | same |
| Perplexity | PerplexityBot | Search: surfaces and links sites in Perplexity answers; not used for training foundation models | The site is not surfaced in Perplexity search results | docs.perplexity.ai/guides/bots |
| Perplexity | Perplexity-User | User-triggered visits when a user asks a question | Perplexity says this fetcher generally ignores robots.txt because the user requested it | same |
| Google | Googlebot | Crawling for Google Search, including AI Overviews and AI Mode | The page cannot be crawled for Search at all | developers.google.com/search/docs/appearance/ai-features |
| Google | Google-Extended | A control token, not a separate crawler: use of content for training Gemini models and for grounding in some other Google systems | No effect on Search or its AI features | developers.google.com/search/docs/crawling-indexing/google-common-crawlers |
| Microsoft | bingbot | Crawling for Bing; Bing's AI Performance report covers Copilot and Bing AI summaries, and Bing says it respects robots.txt and other owner controls | The page cannot be crawled for Bing | Bing Webmaster blog, 2026-02-10 |

## How to judge check 1

- For being cited in answers that search the web, the search agents and user-triggered agents matter. Blocking a training-only agent (GPTBot, ClaudeBot, Google-Extended) does not by itself stop citation in search-based answers; it is a policy choice and may be intentional.
- To limit what Google shows from a page in Search, including AI features, Google documents `nosnippet`, `data-nosnippet`, `max-snippet` and `noindex`.
- Read robots.txt group matching carefully: a specific user-agent group replaces the `*` group for that agent.
- Never advise blocking or unblocking without saying what each change affects, and let the owner decide.

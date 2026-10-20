# Privacy policy: AI Search Visibility & Brand Mentions (GEO/AEO) (ai-seo)

Effective date: 2026-10-20.

This plugin is a set of instructions and reference documents for an AI assistant. It contains no code that runs, no server, no analytics and no tracking. The publisher receives nothing from your use of it.

| Topic | Answer |
|---|---|
| Categories of personal data collected | None. |
| Purposes of processing | None, because nothing is collected. |
| Recipients or third parties | None from this plugin. Pages you ask it to fetch, and any search you explicitly request, go through the assistant's own tools to the sites or search provider involved. |
| Retention | None. The plugin stores nothing of its own; the crawler skill writes llms.txt or robots.txt in your project only when you ask. |
| Your controls | None needed. You can remove the plugin at any time; nothing remains except llms.txt or robots.txt changes you asked it to make in your project. |

## What happens when you use it

- Network scope: this plugin fetches only URLs you type or paste, including URLs inside logs or exports you paste, plus the robots.txt file of those sites; and, only when you ask to verify a bot's IP or re-check a dated fact, the vendor documentation, IP-list or study pages the plugin names as sources (OpenAI, Anthropic, Perplexity, Google, Microsoft/Bing, Amazon, Apple, Meta, Mistral, Cloudflare, Wikipedia, llmstxt.org and the cited studies). It fetches public pages only, never logs in or submits forms, and skips paths a site's robots.txt disallows. Default and maximum: 10 page fetches and, only when you explicitly ask, 10 search queries per run; robots.txt does not count. Fewer are used when your supplied URLs or requested work need fewer, and the answer states the counts used. Larger supplied lists are handled in bounded batches; the ceiling stays 10. Every search query is listed. The plugin never queries AI answer engines, runs no code of its own and stores nothing of its own; the crawler skill writes llms.txt or robots.txt in your project only when you ask; if the assistant has a code or spreadsheet tool, it may use it to compute the tables you see.
- Any fetching or searching is done by the assistant's own tools under the assistant provider's privacy terms, not by this plugin.
- Brand and competitor names, logs, exports and answers you paste stay in your conversation with the assistant, under the assistant provider's privacy terms.
- Before sharing analytics exports, remove personal data such as user IDs or email addresses. If pasted material still names private people or shows their emails or user IDs, the skills do not repeat them: they refer to Person 1, Person 2 and ask you to remove such data before the next paste.

## Contact

Questions about this policy: open an issue at https://github.com/grayskripko/marketing-skills/issues

## Changes

If this policy changes, the new version will be published in this file with a new effective date.

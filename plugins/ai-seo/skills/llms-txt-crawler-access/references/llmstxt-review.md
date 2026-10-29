# llms.txt: format and what it does

Proposal: llmstxt.org, version 2. <!-- https://llmstxt.org/ modified 2026-08-10, first published 2024-09-03; changes https://llmstxt.org/changes.html --> A community proposal, not a crawler permission protocol and not an engine certification.

Format (v2):
- File at `/llms.txt`; an H1 with the site or project name is the only required element.
- Then optionally a blockquote summary, free paragraphs, and H2 sections holding Markdown link lists: `- [Title](URL): optional note`.
- A section named `Optional` marks links that can be skipped when context is short.
- v2 adds discovery through `<link rel="alternate" type="text/markdown">` and `rel="describedby"`, and a subpath file covers that subpath (most specific file wins).
Do not reject an H1-only file as invalid; report weak content separately from format errors. Check only links whose existence the user supplied or a permitted fetch confirmed; do not invent `.md` page URLs.

What it does for visibility: <!-- reviewed 2026-10-12 -->
- Google Search, including AI Overviews and AI Mode: ignores llms.txt; creating one neither helps nor harms rankings <!-- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide, updated 2026-07-10 -->.
- ChatGPT, Perplexity, Claude, Bing/Copilot: their crawler documentation does not say they read llms.txt to choose or cite sources. Not documented is not the same as never used.
- Vendors publish their own llms.txt as documentation indexes, and an assistant can read one when a user points it there. A logged fetch of `/llms.txt` shows a request, not that the file was used in an answer.
So: write one when the goal is helping AI tools and coding assistants navigate documentation; do not promise AI search visibility from it.

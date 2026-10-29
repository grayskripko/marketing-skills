# Engines as measurement targets

This file lists AI answer surfaces a team commonly measures. It describes what a user can observe on each and which settings change the answers. It does not rank engines. Check each vendor's current help pages before a run; interfaces change often.

| Surface | What the person running the panel can observe | Settings to record, because they change answers |
|---|---|---|
| ChatGPT (OpenAI) | The answer text; linked sources when it searches the web | Signed in or out, web search on or off, model or mode if selectable, country |
| Perplexity | The answer text with numbered sources | Signed in or out, mode (standard or research), country |
| Google AI Overviews | The overview above the results, with linked sources, on queries where one appears | Signed in or out, country, device, language |
| Google AI Mode | A conversational answer with linked sources | Signed in or out, country, device |
| Gemini (Google) | Answer text and any sources or related links actually shown; not every response includes links | Account state, model or mode, country, connected sources and observed search use |
| Claude (Anthropic) | Answer text and citations when web search is used | Account/plan, interface/model, country, search control if available, and whether search was actually used (the new Claude experience has no web-search toggle) |
| Microsoft Copilot | Answer text and source links when a web-grounded response shows them | Exact Copilot product/surface, account state, mode/model, country and observed web-search use |

## How to use this list

- Measure each surface separately. Never average different engines into one score.
- Keep settings fixed inside one engine across runs and periods. If settings change, start a new baseline.
- Record the run date. Answers can change within days (see `myths.md`, the entry on single checks).
- A surface that shows no sources can still be scored for mentions; citation rate is then "not available", not zero.

## Owner-side reporting, where it exists

- Google: Search Console includes AI Overviews and AI Mode appearances inside the Web search type of the Performance report, and since 2026 also offers generative AI performance reports with impressions.
- Microsoft: Bing Webmaster Tools has an AI Performance report with citations, cited pages and grounding queries across Copilot, Bing AI summaries and some partners.
- Analytics: Google Analytics 4 has a default channel called AI Assistant for visits referred by recognized AI assistants.

Details and caveats for these reports are handled by the export-analysis skill.

# Sponsorship Pitches

Check creator media-kit audience claims, write sponsorship pitches and draft replies to brand offers.
For podcast, newsletter and video creators using pasted audience summaries, brand notes, placement inventory and proposed terms. No account, API key or paid service is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a bundled program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers. This working folder also contains development evaluation text under `tests/`, `REVIEW.md`, and `BUILD-NOTES.md`; those records are not runtime instructions and should be excluded from a submitted release package.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not direct web search, URL or robots.txt retrieval, API calls, account connections, message sending, mailbox draft creation, publishing, settings changes, or contract signing. URLs identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead. Source notes describe prior publisher verification, not a request to retrieve those pages during your task.

The skills explicitly permit local counting and arithmetic using your assistant's existing tools. Depending on the host, this may execute a calculation in a code or spreadsheet tool; no calculation program is bundled. The skills name no particular tool, interpreter, package installation, API, or network destination. Execution and any temporary files are managed by your assistant provider. Reading explicitly supplied files is also performed by the assistant's existing tools. The requested emails, replies and media-kit summaries are returned as draft text; the skills do not instruct file writes or delivery.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments, and tool activity under its own terms. This disclosure concerns plugin-directed activity; it does not claim that the assistant provider operates without network access.

## Jobs

- **check-audience-claims** repairs audience and survey wording while preserving dates, definitions and uncertainty.
- **draft-sponsor-pitch** writes an email and matching placement summary or media-kit draft from supplied facts.
- **reply-to-brand-offer** compares an incoming offer with a rate card and drafts a reply without accepting unapproved additions.

Paste the relevant export rows with metric names and dates, the copy or brand email, available placements, currency and prices. Say which terms are agreed and which are proposals. Redact individual audience records and private contact details. Files explicitly supplied for the task can also be read where the host supports them; pasted text covers all three jobs.

Example: “Here are our episode download rows, a brand brief and two October placements. Write a short sponsorship email and a matching placement summary at the rate I give.”

Monthly totals stay monthly; downloads are not automatically unique listeners; voluntary survey percentages describe respondents; unknown cross-platform overlap stays unknown. The creator reviews the draft. Contract or publication questions can require jurisdiction-specific review.

## Access and privacy

Nothing is fetched, including pasted URLs. No sponsor discovery, account connection, sending, mailbox draft creation, publishing, communicating deal acceptance or contract signing is provided. Local counting and arithmetic may execute through the assistant's existing tools as described above. The package has no executable integration, service, storage or telemetry. The assistant provider's conversation processing and retention apply. See [PRIVACY.md](PRIVACY.md).

Install this folder through your host's supported plugin mechanism. It contains both host manifests and three skills; no additional setup is needed for pasted text. Local behavioral tests do not establish directory approval or automatic selection.

MIT license, Sergey Skripko, 2026. Support: https://github.com/grayskripko/marketing-skills/issues

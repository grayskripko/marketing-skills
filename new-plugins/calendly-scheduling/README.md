# Calendly Scheduling

Explain why Calendly times are unavailable and which setting to review.
For schedulers and service teams investigating missing appointment times. Needs pasted Troubleshoot codes, the affected date/time and time zone, and relevant event/calendar settings. Routing checks use pasted form answers, conditions and response exports. No account connection, keys or paid API is needed to analyze supplied text.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The diagnosis is offline; the recommended user checks are not. You perform any Calendly actions yourself in your browser: open Scheduling → Preview → Troubleshoot, review settings and bookings, test routing answers in Preview form, inspect Responses or Meetings, and request a CSV export. A requested export may arrive by email from Calendly. The slot skill also explains user edits to buffers, Free/busy exceptions (including Save changes), and host/distribution settings, followed by a same-slot recheck. The routing skill may recommend a published-form test if requested; submitting it can create a response record, and completing scheduling can book a meeting. These actions use Calendly and any calendars already connected to your account; the plugin does not perform them. An External URL is a possible routing destination to analyze, not an instruction for the assistant to open it.

The `.claude-plugin` and `.codex-plugin` folders contain platform metadata, not executable servers. Development records in `tests/`, `BUILD-NOTES.md`, and `REVIEW.md` are not runtime instructions and should be kept outside the submitted release folder.

| Skill | Give it | You get |
|---|---|---|
| calendly-slot-diagnosis | Codes and event/calendar settings | Cause, supporting evidence, exact setting to review and same-slot recheck |
| calendly-routing-diagnosis | Answers, conditions, destinations and response rows | Matching conditions, fallback explanation and destination setting to review |

## Get the right input

Open the affected event from Scheduling, select Preview, then Troubleshoot. Copy the reasons for the affected date and time. Include the event duration, availability, buffers, limits and event kind when relevant. Use neutral host labels rather than names or email addresses.

For an unexpected routing result, paste each condition's question, qualifier, answer, AND/OR grouping and destination, plus the fallback. Responses can be copied from Scheduling → Routing forms → the form → Responses, or exported with Export CSV. Preview submissions do not create response rows.

## Examples

- “BUFFER still shows after I removed the buffer. Here are the event settings and the existing booking's buffer.”
- “MEETING LIMIT appears on a team event. Which host setting should we review?”
- “These form answers went to the fallback message. Which condition failed?”

## Data and network

The skills read supplied text and files the user selects. The assistant makes no plugin-directed network requests; user-performed Calendly checks use the service as described above. Official knowledge is bundled in dated reference files. No calendar connection, booking, setting change, telemetry or plugin storage. [Privacy](PRIVACY.md).

## Sources and maintenance

Official help pages were read on 2026-10-11. Source dates, URLs and deciding facts are in each skill's references.

## Support and license

[Issues](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).

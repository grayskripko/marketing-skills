# Linear Triage

Diagnose Linear intake and snooze behavior from supplied templates, triage rules, team defaults and issue activity; produce a disposition review list.
For team leads and support or engineering intake owners. Needs pasted templates, ordered triage rules, team defaults and issue activity, or exports containing those details. No keys, account connection or setup is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. For these task workflows, URLs identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The two bundled source registers also say “Recheck near 2026-10-20.” This is a release-maintenance instruction to reopen these public documentation pages: https://linear.app/docs/triage, https://linear.app/docs/issue-property, https://linear.app/docs/issue-templates, https://linear.app/docs/triage-intelligence and https://linear.app/docs/inbox. Following that instruction uses a browser or the assistant’s existing web tool and makes requests to linear.app, exposing the requested URLs and ordinary connection metadata to that site and the tool provider. It does not require sending supplied issue data or connecting a Linear account. It is separate from the supplied-material task workflow; this package does not claim that maintenance is network-free.

Both platform manifest directories contain metadata, not executable runtimes. This working folder also retains text/JSON development evidence under `tests/`, plus `BUILD-NOTES.md`, `REVIEW.md` and `SHA256SUMS`; none is an executable helper. The clean submission described in the scan-hold packaging guidance should exclude development evidence and notes.

| Skill | User job | Result |
|---|---|---|
| diagnose-linear-intake | Explain why an issue entered, skipped or moved through Triage | Intake review list with the supported route, mismatch and next check |
| review-linear-snooze | Explain wake events and review pending dispositions | Disposition list with accept destination, wait condition or retained duplicate issue |

For intake, paste creation source, template scope/status, ordered rules and relevant team settings, including destination teams. For dispositions, paste issue evidence, team decision criteria and the actual acceptance default. For snooze, add chosen wake time, later activity, snapshot time/timezone and team Triage versus personal Inbox. A partial export can start the review; only deciding gaps need more detail.

Example requests: “Why did these tickets bypass Triage? Here are our templates and activity.” “These snoozed issues came back early. Give me a disposition list from this history.”

## Data and network

The task workflow reads only supplied material and returns recommendations. Public-source maintenance and provider processing are disclosed above. See [PRIVACY.md](PRIVACY.md).

## Contents

Two self-contained skills with dated source registers, MIT [LICENSE](LICENSE), and [BUILD-NOTES.md](BUILD-NOTES.md). Support: [repository issues](https://github.com/grayskripko/marketing-skills/issues).

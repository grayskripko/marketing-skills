# Classroom Rubrics

Repair a Google Classroom rubric or official Sheets export; preserve its template and validate scoring, criteria, performance levels and order.
For teachers and course designers. Needs pasted rubric text or a supplied Classroom export; no account, keys, install or paid API is needed for the text workflow.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

Rubric repair and import diagnosis work only from task text, attachments, and local files that you explicitly supply. The skills fetch nothing, request no credentials, and return corrected text, API drafts, or a recovery plan. They do not install software, call APIs, send messages, publish content, or change account settings. A supplied URL is treated as text: paste the relevant content instead. Classroom import, edit, save, and export steps are manual actions for you in Google's service; the assistant does not perform them or upload your rubric. API methods, permissions, and patch parameters are draft-review knowledge, not instructions to execute requests.

The existing local-tool allowance is limited to arithmetic on supplied values and an output file you explicitly request. Your assistant's existing calculation or code tool may run that arithmetic; no executable code is bundled and no package installation or network access is requested. Tool execution and temporary files are managed by your assistant provider. Output files use your assistant's existing file tools, not a bundled program.

There is a separate maintenance instruction in both source registers: recheck the official pages before the planned submission. That check reaches public documentation at support.google.com and developers.google.com, including the documented Request.Errors redirect to troubleshooting/common-errors. It makes network requests if performed; it is not part of supplied-rubric repair. The sites and retrieval provider receive the requested URL and ordinary connection metadata, not an instruction to transmit rubric content. GitHub author, repository, and support URLs identify project pages; the skills do not retrieve them or send support messages.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments, and tool activity under its own terms.

| Skill | Input | Deliverable |
|---|---|---|
| repair-classroom-rubric | Rubric text, export, or API JSON | Corrected rubric in the supplied layout, unresolved score choices, and totals |
| recover-rubric-import | Export history and import error | Recovery steps, preserved content, and edits to apply in Classroom |

Classroom's standard Sheets import requires an untouched export created in Classroom. For another class, import an untouched export into a titled ungraded destination, edit there, then export the destination if needed. Keep the original assignment intact unless it is the requested editing target. Pasted text can be repaired without setup; it is not converted into a fabricated import template.

Sources were checked on 2026-10-11. See each skill's references for field rules and the distinction between Classroom UI and API behavior.

Support: https://github.com/grayskripko/marketing-skills/issues
License: MIT; see [LICENSE](LICENSE).

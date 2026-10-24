# Survey Analysis

Turn supplied survey responses into descriptive analysis: checked question tables, counts and segments, a workbook linking answers to themes and a short findings report.

Inferential testing, weighting, population estimates, survey design and collection require separate additions.
For managers, organizers and teams reviewing survey results. Supply pasted responses or CSV/XLSX, question wording, rules for showing or skipping questions and any list of theme labels (codebook). No survey account or paid API is required. Not for questionnaire design or collecting responses.

## What this package runs and connects to

This package supplies Markdown skills and reference text, JSON platform metadata, a static SVG icon, a license, and build notes. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. Development harnesses and evaluation records are kept outside this plugin folder in `plans/overnight/development/survey-analysis/`.

These skills use task text, attachments, and local files you explicitly supply. All four skills permit your assistant's existing local tools to read files, calculate results, and create and reopen new output copies. Calculations, CSV/XLSX writing, and chart rendering may execute code in the assistant's tool environment. Requested charts are rendered and visually inspected. No runtime or workbook writer is bundled; the assistant relies on tools already available in its host. If a tool is unavailable, supply readable data or accept equivalent tables in the conversation rather than installing software for this workflow. Original inputs remain unchanged.

The skills do not direct the assistant to search the web, fetch URLs or robots.txt, call APIs, access survey accounts, send messages, publish results, or change account settings. Qualtrics and AAPOR URLs identify sources for bundled local notes; GitHub URLs identify repository, documentation, privacy, and support pages. They are not retrieval instructions or connection endpoints. Treat supplied URLs as text and paste the relevant content instead. One reference describes a user-led Qualtrics dictionary export: Survey tab → Tools → Import/Export → Export survey to Word, with Show Coded Values enabled. If needed, the user obtains that file through their own Qualtrics account and supplies it; that separate browser action contacts Qualtrics. The assistant does not access the account or download it.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, calculation inputs, and generated files under its own terms. Output files are created by your assistant's existing tools, not by a bundled program. This is supplied-data analysis with host execution and file writes, not a no-execution workflow.

## What you get

| Skill | Give it | You get |
|---|---|---|
| prepare-survey | responses, question wording and known rules for showing or skipping questions | prepared response table, question map and unresolved rows |
| summarize-questions | responses and question definitions | counts, percentages with the counts they are based on and requested segment tables |
| code-open-answers | open answers and any codebook | reviewable codebook, answers linked to themes and theme counts |
| write-readout | responses or checked tables and coding | short findings report with evidence and proposed next steps |

Examples: “Get this survey ready to analyze.” “Split results by attendee type.” “Group these comments and show the responses behind each theme.” “Write a short readout for the team.”

## How it works

Original files stay unchanged. Unanswered questions, questions skipped under the supplied rules and explicit not-applicable answers stay separate. Every calculated percentage shows the counts used and what it is a share of. Multiple-choice selections and overlapping themes are counted separately from people. Uncertain theme labels and answers that disagree remain visible for review.

This package provides instructions and reference notes. It does not process files by itself. The assistant needs file-reading and local calculation tools for full exports, and a workbook writer to create XLSX. File creation is checked by reopening the result. Requested charts also need rendering and visual inspection. Small pasted datasets can be handled as tables in the conversation without setup. If a tool is missing, supply readable data or use equivalent pasted tables; this workflow does not install software. It must describe what it actually produced and must not claim a workbook exists unless it created one. No native pivots, automatic refresh or survey-platform connection is promised.

## Privacy and limits

Use only authorized data, keep only what is needed and use IDs that do not identify people. Limit access to answers linked to themes; share only safe totals. Small groups and quotes may identify people, so unsafe detail is withheld or grouped more broadly. Outputs are descriptive drafts for human review. They do not prove causes or statistically significant differences, estimate results for the wider population or measure employee performance.

Assistant network scope: no plugin-directed retrieval, API calls or account access. The optional user-led Qualtrics export described above uses the user’s own account and browser. No telemetry. No credentials are needed. The package has no independent storage; the AI host handles supplied data, conversation history and generated files under its own terms. Generated copies stay in the host workspace until managed there. See [PRIVACY.md](PRIVACY.md).

## Support and license

Issues: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).

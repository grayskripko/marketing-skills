# Judge Calibration

Check whether your AI grader agrees with your reviewers and whether its recorded judgments stay consistent.
For teams already using an AI grader to review assistant answers or agent work.
Paste ratings, a rubric, configs or exported traces, or give the assistant the relevant files. No account, API key, install beyond the plugin, or paid evaluation service is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable connectors.

These skills work only from task text, attachments, and local files that you explicitly supply, plus bundled reference text. They do not instruct the assistant to install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The existing local-tool permission covers reading user-designated files and arithmetic on supplied values. The assistant may use its existing code or spreadsheet tool to run those calculations; no executable code is bundled. Tool execution and any temporary files are managed by your assistant provider. This is an offline analysis workflow, not a promise of no host code execution. It does not run your grader or install packages.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools at the destination you authorize, not by a bundled program.

## Jobs

- **Compare judge ratings:** join existing human and grader ratings by case and criterion; show disagreements, unmatched records and failed grading attempts.
- **Audit judge records:** check the rubric against supplied traces; distinguish missing judgments and failed tools from successful grading, and inspect existing repeated or reordered judgments.

Reports cite your case identifiers and trace fields. Numeric results show their inputs and denominator. Human ratings remain reviewer judgments; agreement does not establish correctness. No universal reliability score is supplied.

The skills recognize exported Claude Code, Claude Agent SDK, Codex and MCP records. Recognition of those formats is not a live connection. They do not run your grader, modify its config, change labels or submit reports. With no repeated or reordered records, the report identifies missing evidence rather than inventing observations. Rubric clarification suggestions stay tied to the ambiguity you supplied.

## Getting started

Ask “Where does this grader disagree with our reviewers?” with matching case IDs and the label meanings. Or ask “Why did this grader pass a failed tool?” with the rubric and relevant result events. For a large export, provide a redacted file and identify the relevant cases; the assistant may use its existing local tools for reading and arithmetic. No additional tools or services ship with this package.

## Data and sources

No network requests, telemetry or remote evaluation calls are made by these skills. The assistant provider processes supplied material under its own terms and retention settings. They read only pasted material and user-designated files through the assistant's existing tools. Source links in the [reference register](references/official-docs.md) document the embedded guidance; following those links is not part of the audit. [Privacy](PRIVACY.md) explains conversation processing.

This is a skills-only package for Claude Code and Codex. Uploaded or pasted exports can also be reviewed by an assistant that can load the instructions. Automatic selection and directory acceptance need checks in the destination host.

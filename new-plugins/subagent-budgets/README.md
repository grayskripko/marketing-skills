# Subagent Budgets

Show which delegated agents used your allowance, and draft a budget for the next task.
For developers and teams running delegated agent workflows. Give it pasted traces, usage exports, agent settings or files you identify. No account, API key or install is required for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The `.claude-plugin` and `.codex-plugin` directories contain platform metadata for their respective assistants; neither provides an executable runtime or server.

| Skill | Input | Output |
|---|---|---|
| subagent-usage-report | run records, usage or billing exports | reconciled task/worker usage, missing coverage and evidence of repeated work |
| subagent-budget-plan | chosen allowance and launcher or agent configuration | dispatch budget, stop conditions and a runtime-specific proposal |

Ask “Which worker made this run expensive?” or “Give this delegated task a budget and stop plan.” Recorded tokens, SDK cost estimates, actual billed charges and subscription allowances remain separate. A partial trace yields a partial report.

The package contains instructions only. It reads the material you supply and drafts proposals. It does not monitor accounts, launch agents, change settings, install hooks or stop live workers. A written budget does not enforce a billing ceiling. Runtime facts cover Claude Code, Codex, agent SDK usage and MCP cancellation; each skill links a dated source register.

## Data and network

Network fetches: none. No telemetry, account access or paid API calls. Only pasted content and files you identify are read. No launcher or configuration is changed. Redact credentials and personal data before supplying logs. The host assistant may retain conversations and files under its own settings; the package adds no storage service.

## Status and support

Prepared locally for the requested Monday submission. Publication, installed-host checks and directory review are separate. See BUILD-NOTES.md for validation and open items.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See LICENSE.

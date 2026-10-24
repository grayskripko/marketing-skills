# Context Triage

Find what is filling your agent’s context and remove the waste without losing decisions.
For developers and AI builders using Claude Code, Codex, MCP tools or agent SDKs. Needs pasted traces, configuration snippets or files you provide, plus the next task when preparing a pack. No account, API key or install beyond the host’s plugin support is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

These skills analyze only task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs identify documentation or support pages, not connection endpoints or retrieval instructions; supply the relevant content rather than a URL alone. Reports, continuation packs, and proposed patches are returned as text.

The advice can include user-run actions: `context-audit` suggests Claude Code `/context`, `/compact` and `/clear` after a preservation plan, and a follow-up context-report or outgoing-payload check in your runtime. `context-pack` explains `/compact` and `/clear`; its fictional parser-fix example preserves a next action to inspect a draft and run an unrun check. It also retains pending actions and references from your supplied task. These are recommendations or handoff text, not actions executed by this plugin. Clearing a session loses active continuity; runtime checks and resumed tasks have the execution and connection scope of your own environment. The package does not prescribe a network destination for those checks.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you separately request is created by your assistant's existing file tools, not by a bundled program.

- **context-audit:** ranks supported context contributors and proposes small changes with evidence and retention risks.
- **context-pack:** writes a task-specific continuation brief that keeps constraints, decisions, identifiers, blockers and source references.

Paste the relevant material in your request or attach files. Example: “This session compacts repeatedly. Here is its context report and MCP configuration; explain what I can trim.” For a pack, include the next task and any maximum length. Redact credentials before sharing. Partial traces are useful, but do not establish the whole session’s occupancy.

The skills contain dated, official knowledge about host controls, MCP result shapes and SDK session history. They distinguish visible context from cumulative usage and measured tokens from text size. They propose changes; they do not edit configuration, clear sessions, delete history or connect to servers.

The assistant analysis requests no additional network activity. User-run runtime checks and resumed tasks are separate, as described above. Host conversation processing and retention still apply; see [PRIVACY.md](PRIVACY.md).

This package supplies instructions and references, with no hooks, runtime scripts or MCP server. Host installation and marketplace acceptance remain separate from package checks. Packaging decisions and outstanding release checks are in [BUILD-NOTES.md](BUILD-NOTES.md).

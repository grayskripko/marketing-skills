# CLAUDE.md & AGENTS.md Instructions Cleanup

Fix conflicting CLAUDE.md and AGENTS.md instructions: map the active scopes, repair stale references and return a minimal patch that preserves approvals.
For developers maintaining repository and user instructions across coding agents.
Needs pasted files, traces, logs, configs, transcripts or identified local files, plus the launch directory and host when known. Pasted-input review needs no account, key, installation or paid API.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. User-identified local files and their supplied imports may be read using your assistant's existing file tools. The audit skill returns findings without editing files. When you explicitly request a repair, the repair skill edits only the identified instruction files using those tools; otherwise it returns a diff. Any output file you explicitly request is created by those tools, not by a bundled program.

- **agents-md-scope-audit** returns a verdict with the deciding file, line and load rule, plus a scope map when outcomes differ by launch or host.
- **claude-md-repair** returns a minimal supported patch, or applies it to identified instruction files when requested, preserving approvals and scoped exceptions.

Try: “Which AGENTS.md applies when I launch from services/payments?” Or: “Clean up these conflicting instructions and replace this old command using the scripts I pasted.” Or: “Does my Agent SDK setting load our CLAUDE.md?”

The bundled knowledge covers Claude Code's mixed CLAUDE.md/AGENTS.md selection, Codex override discovery, SDK setting sources, import resolution, conditional rules and retrieval boundaries. [Official source register](references/platform-rules.md) includes dated URLs.

For a Claude-only contradiction review, the native `/doctor prompt-audit` may already finish the job. This package focuses on ownership across instruction sources and hosts, with a reviewable patch. Plain shortening belongs to a text-reduction workflow; individual skill repair is a different job.

Command strings in examples and proposed patches are instruction-file content, not commands this workflow executes. The optional native `/doctor prompt-audit` mentioned above is a separate Claude Code feature, not invoked by these skills. Both platform manifests describe the same supplied-material workflow; `.codex-plugin/` is metadata for Codex, not a connector or server.

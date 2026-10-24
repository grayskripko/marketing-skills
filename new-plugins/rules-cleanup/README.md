# Rules Cleanup

Find conflicting or stale repository rules and prepare a small repair patch.
For developers maintaining Claude Code, Codex or Claude Agent SDK instructions.
Needs the files you paste or identify, a directory tree, launch directory and relevant configs or command definitions. No account, key, install or paid API is required for pasted-input review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply or identify, plus bundled reference text. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

Local file reads use your assistant's existing file tools. When you explicitly request a patch, those tools may edit only the identified instruction files; otherwise the skills return a diff. The repair skill may recommend a manual next check when execution evidence is missing. Any command execution for that separate check is outside this workflow and is not performed by these skills. Commands in inspected rules and example diffs are document content, not instructions for this plugin to execute.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

- **rule-scope-audit** maps which rules apply, distinguishes loading failures from contradictions, and links findings to supplied files.
- **rule-file-repair** replaces supported stale references and reconciles clear scope errors while preserving approvals and exceptions. Returns a diff, or applies changes to identified instruction files when requested.

Try: “Audit these CLAUDE.md and AGENTS.md files for this launch directory.” Or: “Replace this obsolete test command using the package scripts below; keep our deploy approval rule.”

The skills contain client-specific discovery rules, SDK loading checks and MCP annotation boundaries from official documentation. Reference registers include source URLs and actual read dates. Source dates describe documentation access, not verified compatibility with every installed version.

Network: none in these workflows. The assistant reads supplied text or identified local files; it does not fetch documentation, follow links, contact MCP servers or run repository commands. It creates no telemetry, accounts or background service. Applying a requested patch uses the assistant's existing file tools. Conversation handling follows your assistant provider's terms.

This is document diagnosis and repair. It does not install permission controls or guarantee that an agent obeys prose. Supplied command definitions can establish a replacement exists; successful execution needs separate evidence.

Local manifests are included for Claude Code and Codex. Publication, directory submission and approval are separate steps; see BUILD-NOTES.md for current checks and open questions.

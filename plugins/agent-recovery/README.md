# Agent Recovery

Plan recovery of an interrupted AI agent run from checkpoints and action receipts; identify what can resume and which effects need checking before retry.
For developers and operators whose AI agent stopped halfway or whose workers left uncertain actions.
Paste traces, logs, configs, transcripts, checkpoints, files and receipts, or provide named local files. No setup, keys, accounts or paid APIs are required beyond your existing assistant.

These skills return an action ledger, a continuation plan and a check of supplied recovery records. They do not restart the agent.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not runtime servers.

The assistant analyzes material you paste or explicitly supply, including authorized named local files, and reads the bundled source register. The skills do not direct the assistant to install runtimes, retrieve URLs, search the web, call connectors or service APIs, restart agents, cancel processes, send messages, publish content, change permissions, edit checkpoints, or replay actions. Source and support URLs are references, not retrieval instructions; supply the relevant content when evidence is missing. Named local files may be read through your assistant's existing file tools, and a deliverable may be saved only to a destination you request.

Recovery plans can ask you to obtain checkpoint/session exports, receipts, installed-version details or idempotency evidence through your existing host's inspection facilities. They can propose operator steps such as `claude --resume`, `codex resume <SESSION_ID>`, LangGraph `Command(resume=...)`, or OpenAI Agents SDK state restoration and `Runner.run(...)`. The skills do not execute those steps. If you carry out a plan in your runtime, that runtime may run code, contact its configured model providers or services, write files, or repeat external effects; its configuration and your approvals control those actions. This is not a claim that executing a recovery plan has no network activity.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Local reads and any output file you explicitly request use your assistant's existing tools, not a bundled program.

| Skill | What you give it | What you get |
|---|---|---|
| agent-state-reconstruct | Saved state, worker records, artifacts and receipts | Completed, pending and uncertain action ledger |
| agent-resume-plan | Ledger, runtime config and approval records | Ordered continuation plan with replay boundaries |
| agent-resume-check | Before-and-after artifacts and effect records | Verified, incomplete or unresolved outcome |

Ask: “This run stopped halfway. Did the timed-out action happen?” Or: “Plan how to resume this agent without sending twice.” Or: “Check whether recovery preserved the finished files.”

The instructions distinguish LangGraph node replay, Claude Code and Codex session selection, Claude Agent SDK session availability, OpenAI Agents SDK outer approval state and MCP cancellation races. Retrieval-based records retain exact request identity and context; indexing and final outcomes are checked separately. Current official sources and actual read dates are in [runtime sources](references/runtime-sources.md).

The deliverables use your existing artifact layout. Routine worker assignment belongs to agent-orchestration, shorter handoff summaries to token-saver, durable stored-fact corrections to memory repair, and deeper failure investigation to agent debugging.

To obtain missing runtime state, the agent can identify the exact session, checkpoint export or receipt fields needed from your pasted version/config. Use your existing host's export or read-only inspection facility and paste the result. Plans identify the supported resume path and its prerequisites; execution stays in your existing runtime. No framework installation or service connection is bundled.

Network scope: the skills fetch no web pages, run no searches and call no external connectors or service APIs. They read pasted material and authorized named local files. No telemetry or package-owned storage. See [PRIVACY.md](PRIVACY.md).

MIT. See [LICENSE](LICENSE).

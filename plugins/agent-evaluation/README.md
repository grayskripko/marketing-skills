# Agent Evaluation

Plan agent evaluation and verify agent output against supplied requirements, artifacts, action receipts and escalation records.
For application owners and engineers checking agent answers, saved work, tool actions and human escalation before accepting a task or release.
Paste requirements, traces, logs, configs, transcripts, receipts, original sources or selected files. No account, API key, paid service or additional installation is needed for this review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

Local tool use is allowed: requested output files are written at your chosen destination using your assistant's existing file tools. The acceptance-plan skill writes assertions in a supplied runner schema, or tool-neutral checks without one, and does not execute them. Runner setup and live execution in your own infrastructure are described as later prerequisites; these skills do not run agents, graders, imports or deployments.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation, attachments and tool data under its own terms. Local execution and any temporary files are managed by that provider; requested output files remain at your chosen destination under your control.

| Job | Skill | Result |
|---|---|---|
| Plan agent evaluation | `agent-acceptance-plan` | Requirements mapped to observable outcomes and the supplied runner contract |
| Prepare agent evals and regression tests | `agent-evals-export` | Redacted ready cases in the importer's format, or neutral JSONL; unresolved cases listed beside the file |
| Verify agent output | `agent-outcomes-check` | Findings tied to sources, actual artifacts, action receipts and escalation |
| Check agent results before release | `agent-release-report` | Readiness decision from supplied runs and grader records |

Try: “The agent says it submitted our request. Check this trace and receipt.” Or: “Can we ship this version? Here are our requirements and runner exports.”

A completion statement is checked against the requested outcome. Checks cover normal completion, incomplete input, tool failure and human escalation. Runtime completion, correct content, persisted artifacts and action completion are checked separately. Existing grader judgments are checked against the evidence they received and the owner's rubric.

The package works with supplied Claude Code, Codex, MCP, Claude Agent SDK, OpenAI Agents SDK and LangGraph records. It prepares checks for your existing runner and reviews its exports. It ships instructions and saved references; it does not collect traces, run agents, import cases into a service or deploy releases. Exact runner exports need the supplied importer schema or accepted example. Without one, it produces neutral JSONL with explicit expectations and provenance.

For later execution in your infrastructure, provide its runner version, schema, existing config and approved action scope. The assistant can prepare the corresponding capture contract and explain prerequisites without reading credential files. Live runs use that infrastructure's accounts, provider usage and side effects; this package's jobs stop at preparation and supplied-result review.

Retrieval-stage diagnosis belongs in RAG Evaluation. Checking a currently delegated team's combined result is a separate job. Individual skill repair and instruction rewriting are separate jobs.

## Data and network

No runtime network requests: no searches, URL fetches, robots.txt requests, dependency downloads, remote schema resolution, uploads or telemetry. Only pasted inputs and selected task files are read. Requested local exports are saved at the chosen destination. No plugin-managed database or retention service is supplied. The assistant host handles chats and file/tool data under its own settings. See [PRIVACY.md](PRIVACY.md).

Official format knowledge is embedded in every skill; dated supporting URLs are in the [reference register](references/official-docs.md). Skills also carry a few dated facts (OpenAI Evals retirement, Inspect scoring changes, judge reliability, infrastructure noise), each with its source and check date in a hidden comment.

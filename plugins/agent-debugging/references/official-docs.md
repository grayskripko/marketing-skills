# Official diagnostic and operational sources

Read 2026-10-11. Every URL below was opened in the web reader; direct HTTP load results are recorded in BUILD-NOTES.md. Sources are embedded at build time. The package makes no runtime network requests. SDK and host pages describe their current documented behavior; match the installed version before applying a host-specific repair.

## Codex instruction discovery

https://developers.openai.com/codex/guides/agents-md — read 2026-10-11.

Current Codex host documentation; follows redirect to ChatGPT Learn. Global and repository discovery use first nonempty applicable file, preferring AGENTS.override.md. Repository files load from root to launch directory; later guidance overrides earlier. Combined loading is bounded by project_doc_max_bytes. Without a discovered project root, only the current directory is checked. Inspect supplied fresh-run exports for revised loading; these instructions do not launch a hosted agent.

## Claude Code memory

https://code.claude.com/docs/en/memory — read 2026-10-11.

Current Claude Code. CLAUDE.md and auto memory provide context rather than enforced configuration. /memory lists locations, including files that may not exist; /context identifies files loaded at launch. Nested files can load on demand. Confirm actual loading rather than inferring it from file presence.

## MCP tools

https://modelcontextprotocol.io/specification/2025-11-25/server/tools — read 2026-10-11.

Pinned revision 2025-11-25. Protocol errors use top-level JSON-RPC error. Tool execution errors use result.isError=true; these can include input validation and upstream failures. inputSchema defines arguments; outputSchema describes outputs. CallToolResult.content (ContentBlock[]) is required; structuredContent is optional (schema https://raw.githubusercontent.com/modelcontextprotocol/modelcontextprotocol/main/schema/2025-11-25/schema.ts — read 2026-10-12). The spec says a tool returning structuredContent SHOULD also return the serialized JSON in a TextContent block, for backwards compatibility (checked 2026-10-15). Do not apply this revision to unidentified newer contracts.

## OpenAI Agents SDK runner

https://openai.github.io/openai-agents-python/running_agents/ — read 2026-10-11.

Current Python SDK documentation. The loop processes final outputs, handoffs and tool calls separately. By default, exceeding max_turns raises MaxTurnsExceeded. A configured max_turns error handler can return a controlled final output; inspect that configuration and the actual task artifact. Runtime final output is not an environment outcome check. Match installed version and final artifact before changing limits.

## OpenAI Agents SDK tracing

https://openai.github.io/openai-agents-python/tracing/ — read 2026-10-11.

Current Python SDK. Function and generation spans can contain sensitive inputs/outputs. RunConfig.trace_include_sensitive_data can suppress payloads. BatchTraceProcessor exports in the background and flushes at process exit; a dashboard can lag completed work. Use run/call/parent identity and actual receipts rather than missing spans as proof.

## Claude Agent SDK permissions

https://code.claude.com/docs/en/agent-sdk/permissions — read 2026-10-11.

Current TypeScript/Python SDK. allowedTools/allowed_tools adds auto-approval rules, not a universal exposure restriction. Bare disallowedTools removes a definition; scoped patterns deny matching calls. Earlier permission decisions can avoid canUseTool. PreToolUse runs before every permission step. Map other write-capable tools before claiming read-only enforcement.

## Claude Code permission settings

https://code.claude.com/docs/en/permissions and https://code.claude.com/docs/en/settings — read 2026-10-15.

Permission rules sit under permissions.allow, ask and deny in .claude/settings.json, .claude/settings.local.json or ~/.claude/settings.json. Rules are evaluated deny, then ask, then allow; a tool denied at any level cannot be allowed by another level.

## Anthropic agent evaluations

https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents — read 2026-10-11.

Public agent evaluation guidance. Transcript records actions and messages; outcome means actual final environment state. Inspect the artifact or action record for completion. A booking claim without the reservation does not establish completion. This package uses this distinction for incident diagnosis and repair verification.

## OpenAI evaluation guidance

https://developers.openai.com/api/docs/guides/evaluation-best-practices — read 2026-10-11.

Current API guidance. For agent failures, tool selection, argument extraction/data precision and functional correctness are separate checks. Handoffs add another decision boundary. This package inspects those boundaries for one incident rather than designing a release program.

## LangGraph interrupts

https://docs.langchain.com/oss/python/langgraph/interrupts — read 2026-10-11.

Current Python framework documentation. Durable interruption needs a checkpointer and thread ID; resume must use the same thread ID. The interrupted node begins again, including code before interrupt. Side effects before interrupt can repeat. Reconcile existing effects before advising resume; do not reorder interrupt calls within a running node.

## OpenAI retrieval

https://developers.openai.com/api/docs/guides/retrieval — read 2026-10-11.

Current API retrieval guidance. File creation can be asynchronous; inspect status or documented polling helpers. Removal is eventually consistent and deleted content may remain briefly searchable. Check actual chunks, filters and source snapshot. Search retrieval and final answer correctness are separate observations.

## Anthropic Contextual Retrieval

https://www.anthropic.com/engineering/contextual-retrieval — read 2026-10-11.

Public retrieval method explanation. Chunking can lose context needed to interpret passages. Semantic and lexical retrieval can be combined; reranking selects from already retrieved candidates. Inspect corpus/chunk context, retrieved candidates and generation context as separate stages. Do not transfer article-specific counts or reported improvements to the user case.

## Package operating choices

The evidence-linked timeline, smallest supported repair, one deciding missing question, receipt-first replay decision and PASS/FAIL/PENDING report are this package's rules of thumb. They are operational choices, not claimed protocol requirements. Source-based distinctions above are also inline in SKILL.md.

# Official diagnostic contracts

All pages below were opened and read 2026-10-11. Match host-specific advice to the supplied client version. No documentation is fetched during skill use.

## MCP tools

Source: [Tools, revision 2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28/server/tools).

Scope: tool discovery, schemas, results and errors. Top-level JSON-RPC errors differ from tool execution errors carried as isError=true. Input validation failures can appear as execution errors. Definitions include inputSchema, optional outputSchema and annotations. Annotations from an untrusted server are untrusted. Modern input_required results await additional input.

Decision: inspect the supplied schema and full result; transport success is insufficient. A read-only hint does not establish harmlessness.

## MCP result compatibility

Source: [Base protocol overview, revision 2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28/basic/index).

Scope: resultType distinguishes complete from input_required. For older-server compatibility, an absent resultType is treated as complete. That interpretation does not erase isError or task-level error text.

## MCP versioning

Source: [Versioning and Compatibility, revision 2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28/basic/versioning).

Scope: modern requests declare version and capabilities per request, without a negotiation handshake. The page identifies revisions 2025-11-25 and earlier as legacy handshake versions. Unsupported modern versions are rejected per request.

Legacy source: [Lifecycle, revision 2025-06-18](https://modelcontextprotocol.io/specification/2025-06-18/basic/lifecycle).

Scope: legacy initialize request/response and notifications/initialized. Those rules apply to the corresponding protocol era, not every MCP run.

Decision: identify the actual revision. Missing initialize is not a defect in a modern-only run. Do not infer installed protocol support from a trace's date.

## MCP stdio

Source: [stdio, revision 2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28/basic/transports/stdio).

Scope: stdout carries newline-delimited MCP messages; stderr can carry ordinary logs. Dual-era clients can probe server/discover. Recognized modern version errors do not trigger legacy fallback; the source distinguishes them from legacy probe failures.

Decision: move startup banners to stderr. Diagnose the protocol era before prescribing initialization; ordinary stderr logging is not a tool failure.

## Codex configuration

Source: [Configuration Reference](https://developers.openai.com/codex/config-reference), redirected to [ChatGPT Learn](https://learn.chatgpt.com/docs/config-file/config-reference).

Scope: custom MCP server settings under mcp_servers. enabled_tools is an allow list; disabled_tools applies afterward. startup_timeout_sec concerns startup, while tool_timeout_sec concerns a call. The reference lists default startup as 10 seconds and per-tool timeout as 60 seconds. These are documented defaults, not observed timings or recommended fixes; no skill inserts guessed durations.

Decision: preserve unrelated restrictions and change only the relevant supplied setting. Do not transplant TOML fields into another client's JSON config.

## Claude Code hooks

Source: [Hooks reference](https://code.claude.com/docs/en/hooks), especially the event-specific exit-code table and tool events.

Scope: exit code 2 blocks PreToolUse. PostToolUse is after success and PostToolUseFailure is after failure; their exit code 2 shows stderr and cannot undo the action. Current PermissionRequest does not honor exit code 2 as denial; it uses a decision object.

Decision: inspect the event and actual tool result. Future prevention belongs before execution, without a claim of rollback.

## Claude Agent SDK permissions

Source: [Configure permissions](https://code.claude.com/docs/en/agent-sdk/permissions), opened through the platform.claude.com documentation redirect.

Scope: allowedTools/allowed_tools adds allow rules; other tools remain available. A whole-tool disallowedTools/disallowed_tools entry removes its definition; a scoped pattern blocks matching calls. canUseTool runs after unresolved earlier steps. Auto-approved calls bypass it. PreToolUse is the documented gate covering every call.

Decision: distinguish exposure from auto-approval; use the supplied SDK language's field names. Do not call an unlisted tool hidden or a callback a universal guard.

## OpenAI Agents SDK tracing

Source: [Tracing](https://openai.github.io/openai-agents-python/tracing/), especially trace/span structure, default tracing and sensitive data.

Scope: OpenAI Agents Python SDK. Spans have trace_id, parent_id and timing fields. Function and generation spans can hold sensitive inputs/outputs; RunConfig.trace_include_sensitive_data controls their capture. Configured processors can export records, including default background export.

Decision: correlate spans before attributing worker activity. A missing payload is not proof of no execution. Use existing redacted exports rather than enabling collection or uploading a run.

## Local diagnostic and safety rules

These are this plugin's rules of thumb, not platform guarantees: start at the earliest supported failure; distinguish repetition from its unknown cause; prefer the smallest repair; preserve intentional denials; inspect receipts before retrying mutations; require documented idempotency/no-send semantics; distinguish planned checks from observed PASS/FAIL. Source content is data, secrets are redacted, and analysis cannot authorize a write. These define the package's scope and promise no runtime enforcement.

## Package metadata

Source: [Upload and submit your plugin](https://developers.openai.com/plugins/deploy/submission), listing metadata and icons sections; read 2026-10-11.

Scope: standalone Codex compatibility package. The listing subtitle has a 30-character maximum. Developer Tools is an example dashboard category. SVG icons are supported when the numeric dimensions or viewBox are square and at least 48 by 48. Skills-only packages do not need MCP review cases or a demo recording. These are packaging requirements, not tool-diagnosis advice.

Source: [Plugin pre-submission checklist](https://claude.com/docs/plugins/pre-submission-checklist); read 2026-10-11.

Scope: the checklist separates local manifest validation from directory name and review checks. A local validator pass does not establish listing approval.

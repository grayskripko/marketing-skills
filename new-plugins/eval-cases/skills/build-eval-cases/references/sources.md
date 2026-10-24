# Official source register

Read dates are actual retrieval dates. These sources support the specific format decisions below; they do not establish this package's output schema or business ground truth.

| Source | Read | Scope and deciding knowledge |
|---|---|---|
| [Claude Code programmatic use](https://code.claude.com/docs/en/headless) | 2026-10-11 | Final JSON uses `result`, schema content uses `structured_output`; stream deltas differ from final result messages. `parent_tool_use_id` connects nested runs. Relevant sections: structured output, streaming, subagent messages. |
| [Codex non-interactive mode](https://developers.openai.com/codex/noninteractive), redirected to [current page](https://learn.chatgpt.com/docs/non-interactive-mode) | 2026-10-11 | `--json` emits events with item lifecycle; final-message files are narrower than event capture. Schema-constrained final output differs from JSONL event output. Relevant sections: machine-readable output, structured outputs. |
| [MCP tools, current revision](https://modelcontextprotocol.io/specification/2026-07-28/server/tools) | 2026-10-11 | Current `latest` redirect resolved to this revision. `input_required` is a request for more input; protocol errors differ from execution errors. Structured results and output schemas have specific roles. Do not apply new result fields to older supplied sessions. |
| [MCP tools, older revision](https://modelcontextprotocol.io/specification/2025-06-18/server/tools) | 2026-10-11 | Older wire examples omit `resultType`; `isError` and `structuredContent` still require separate interpretation. Use the user's negotiated revision. |
| [OpenAI Agents SDK tracing](https://openai.github.io/openai-agents-python/tracing/) | 2026-10-11 | Spans have trace and parent IDs. Generation/function payloads may be sensitive; disabling sensitive capture removes evidence. Relevant sections: traces/spans, sensitive data. |

## Authored operational conventions
The case fields, status labels, expectation approval labels, safe aliases and duplicate-merging procedure are this package's rules of thumb, not vendor requirements. A ready case means sufficiently specified preparation, never a reproduced incident. User-provided requirements decide business expectations. Official event docs decide how captured events are interpreted.

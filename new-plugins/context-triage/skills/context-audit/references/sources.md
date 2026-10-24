# Official operational sources

Opened and read 2026-10-11. Dates are retrieval dates, not claims of publication or installed-version compatibility. Current pages may change. The dated MCP specification is a versioned source; match the negotiated protocol before recommending fields. Paraphrases below supply the facts embedded in the skills.

## Claude Code context

[Manage costs effectively](https://code.claude.com/docs/en/costs), read 2026-10-11. Sections “Manage context proactively” and “Reduce MCP server overhead” document `/context`, `/compact` with preservation instructions and `/clear` for a fresh task. Use the context report for occupancy rather than a cumulative usage total. The latter comparison is an authored diagnostic rule, not a promised platform metric conversion.

## Claude Code MCP definitions

[Connect Claude Code to tools via MCP](https://code.claude.com/docs/en/mcp), read 2026-10-11. “Control tool search” documents current default deferral, `ENABLE_TOOL_SEARCH=false` upfront loading, provider exceptions and `alwaysLoad: true` exemptions. Deferral does not shrink returned result text. This last distinction follows the control’s scope; confirm actual client payload when diagnosing a trace. Do not reuse remembered default thresholds from older versions.

## Codex history controls

[Configuration Reference](https://learn.chatgpt.com/docs/config-file/config-reference), read 2026-10-11 via the official redirect from https://developers.openai.com/codex/config-reference/. Entries `tool_output_token_limit` and `model_auto_compact_token_limit` respectively describe per-output storage budgeting and automatic compaction threshold, with model defaults when unset. Neither entry documents a billing cap. No numeric defaults or limits are prescribed here.

## MCP tool-result structure

[Tools specification, version 2025-06-18](https://modelcontextprotocol.io/specification/2025-06-18/server/tools), read 2026-10-11. “Resource Links,” “Embedded Resources” and “Structured Content” distinguish URI references, embedded content and structured results. Text serialization alongside structured data is recommended for compatibility; resource links need not occur in `resources/list`. Protocol result fields do not establish which representation a client sent to a model. Verify this against supplied outgoing requests.

## OpenAI Agents SDK sessions

[Sessions overview](https://openai.github.io/openai-agents-python/sessions/), read 2026-10-11. “Core session behavior” and “Control how history and new input merge” explain automatic history retrieval, persistence of new items and `RunConfig.session_input_callback`. The overview prohibits combining sessions with run-level continuation identifiers; the callback controls model input without resaving filtered old items as new input. Retaining call/result pairs rather than arbitrary item slices is an authored preservation precaution. No SDK installation or API call is required for analysis of pasted code.

## Authored operational heuristics

Rank unknown-size material by visible redundancy and task relevance without calling it a measured token ranking. Preserve permissions, pending actions and acceptance criteria. Prefer recoverable references to unchanged bulk material when the next recipient can retrieve it. Keep unresolved conflicts explicit. These are public diagnostic and summarization practices chosen for this package; they are not documented host guarantees.

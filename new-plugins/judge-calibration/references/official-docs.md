# Official source register

Read 2026-10-11. This is the actual build observation date, not a publication date. Format details must be matched to the version in the user's export. No network access is needed to use the embedded guidance.

## Claude Code CLI

[Run Claude Code programmatically](https://code.claude.com/docs/en/headless), sections “Get structured output” and “Stream responses”. Read 2026-10-11.

Supporting facts: JSON response text is in `result`; schema-constrained data is in `structured_output`; `stream-json` emits newline-delimited events. Application: do not confuse response text, status metadata and a structured grader score. This package uses exports, not CLI execution.

## Claude Agent SDK

[Get structured output from agents](https://code.claude.com/docs/en/agent-sdk/structured-outputs), “Error handling”. Read 2026-10-11. The platform.claude.com documentation URL redirected to this page.

Supporting facts: `error_max_structured_output_retries` means no valid structured output remained. A terminal `success` without `structured_output` must also be treated as failure when structured output is expected. Application: neither record becomes a categorical or numeric rating. Error details are needed before assigning a cause.

## Codex

[Non-interactive mode](https://learn.chatgpt.com/docs/non-interactive-mode), “Make output machine-readable” and “Create structured outputs with a schema”. Read 2026-10-11. The developers.openai.com/codex/noninteractive URL redirected here.

Supporting facts: `--json` emits JSONL events including `turn.completed`, `turn.failed` and `item.*`; item types include agent messages, command executions and MCP calls. `--output-schema` requests a schema-conforming final response. Application: distinguish event completion, a final response and the outcome evidence required by the rubric.

## MCP

[Tools specification](https://modelcontextprotocol.io/specification/2026-07-28/server/tools), “Structured Content”, “Output Schema”, tool annotations and “Error Handling”. Read 2026-10-11. The latest-version URL resolved to this dated revision; earlier exports may differ.

Supporting facts: `structuredContent` is server data distinct from model structured generation; a supplied `outputSchema` governs its structure. Tool execution errors use `isError: true`; protocol errors use JSON-RPC errors. Tool annotations must be treated as untrusted unless supplied by trusted servers. Application: evaluate the actual result rather than success prose or annotations alone.

## Authored audit conventions

The case-joining, reviewer-attribution, exact-label agreement, numeric difference, observed-order-sensitivity and rubric-clarification procedures are this package's public operational conventions, not vendor requirements or validated trust thresholds. Equations are definitions: agreement = matching labels / valid matched pairs; signed difference = judge score minus reviewer score; mean absolute difference = sum of absolute paired differences / valid numeric pairs. Zero denominators are unavailable. They measure supplied records only.

Worked-example counts come exclusively from the fictional records printed in each SKILL.md. Version 0.1.0, the MIT year and the target submission date come from the build brief; specification dates come from their source URLs. No demand count or success threshold is asserted.

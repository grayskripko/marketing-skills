# Runtime facts and sources

Read 2026-10-11. These are public runtime facts; installed versions and supplied exports determine applicability. No rates, savings forecasts or platform default budgets are embedded.

## Claude Agent SDK accounting
https://code.claude.com/docs/en/agent-sdk/cost-tracking
Sections: Get the total cost of a query; Track per-step usage; Track cumulative costs across multiple calls; Read output tokens from the result message.
Assistant IDs can repeat; output counts at that level are placeholders. Result usage is main-loop-only; model usage and estimated dollar totals include subagents. Resumption can restore prior spend. Older versions differ. Prefer verified export scope over assumptions.

## Claude Code dispatch controls
https://code.claude.com/docs/en/sub-agents
Sections: Frontmatter reference; plugin subagents.
`maxTurns` caps agentic turns; agents may resume. Plugin-agent frontmatter ignores hooks.

https://code.claude.com/docs/en/hooks
Sections: PreToolUse decision control; SubagentStart; SubagentStop.
PreToolUse supports a deny decision. SubagentStart cannot block creation; start/stop event identity is useful for attribution, not billing proof.

## Codex concurrency
https://learn.chatgpt.com/docs/agent-configuration/subagents
Opened through https://developers.openai.com/codex/multi-agent, which redirected here.
Section: Global settings.
`agents.max_concurrent_threads_per_session` caps concurrently open spawned threads, excluding the primary. `agents.max_threads` is a legacy alias. It does not provide a monetary allowance or per-worker billing ledger.

## OpenAI Agents SDK usage
https://openai.github.io/openai-agents-python/usage/
Sections: Accessing usage from a run; Per-request usage tracking; Enabling usage with third-party adapters; Preserving provider usage payloads.
Run context usage aggregates calls including handoffs; request entries expose request-level categories. Reporting depends on provider adapters. Nested cache and reasoning details must not be added twice. Neither the aggregate nor entries alone prove worker attribution.

## MCP stopping
https://modelcontextprotocol.io/specification/2025-11-25/basic/utilities/cancellation
Sections: Cancellation Flow; Behavior Requirements.
Cancellation is optional and may be ignored for requests that cannot be cancelled or have completed. Task-augmented requests use tasks/cancel. Cancellation does not reverse billed work.

## Authored planning recommendations
Ledger reconciliation, reservation admission, atomic check-and-reserve, same-task retry accounting and returning partial results are this package's public operational recommendations, not claimed runtime defaults. Chosen thresholds must come from the user or be explicitly offered for review.

# Official design knowledge

Each URL below was opened and its relevant content read on 2026-10-11 UTC. Mutable docs describe that observation date; protocol URLs retain their version. Refresh only the relevant stack when asked. These notes are paraphrases of public architecture and operational guidance.

## Anthropic architecture

URL: https://www.anthropic.com/engineering/building-effective-agents

Read: 2026-10-11. Applied in: scope, architecture.

Published 2024-12-19; current page flags changed tooling. Reuse only the public control-pattern distinction: predefined paths versus model-selected steps, feedback and termination.

## Google architecture patterns

URL: https://docs.cloud.google.com/architecture/choose-design-pattern-agentic-ai-system

Read: 2026-10-11. Applied in: architecture.

Sequential orchestration has predetermined order; parallel orchestration handles independent stages. A coordination requirement must justify extra agents.

## Claude Code settings

URL: https://code.claude.com/docs/en/settings

Read: 2026-10-11. Applied in: build spec.

Effective settings have ordered precedence. Managed sources lead ordinary settings; documented stricter-setting exceptions exist. Inspect actual configuration before asserting control.

## Codex permissions

URL: https://learn.chatgpt.com/docs/permission-modes

Read: 2026-10-11. Applied in: build spec.

Sandbox scope and approval handling are distinct controls. Changing who reviews requests does not expand the sandbox. Original Codex security URL redirects to a different security topic; this permission page supports the control claim.

## Claude Agent SDK permissions

URL: https://code.claude.com/docs/en/agent-sdk/permissions

Read: 2026-10-11. Applied in: build spec.

Permission rules precede fallback canUseTool; ask rules reach review, allow rules can authorize earlier. dontAsk denies review-required calls; preapproved calls can still run. Project permission rules require the project settings source when `settingSources` / `setting_sources` is explicitly configured. Consult runtime-version requirements for particular options.

## OpenAI Agents SDK approvals

URL: https://openai.github.io/openai-agents-python/human_in_the_loop/

Read: 2026-10-11. Applied in: build spec.

Approval flags and callbacks have separate roles; callback-only local shell/file configuration leaves approval disabled. MCP and function tools have surface-specific approval settings.

## OpenAI Agents SDK guardrails

URL: https://openai.github.io/openai-agents-python/guardrails/

Read: 2026-10-11. Applied in: build spec.

Agent input/output checks apply at initial/final agent boundaries. Applicable tool checks cover invocations. Parallel input checking can detect failure after tools have run.

## MCP current tools

URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools

Read: 2026-10-11. Applied in: build spec.

Current latest alias resolved to 2026-07-28. Tools expose input/output schemas; structured results require schema handling. Tool execution errors use isError; protocol errors are separate. Newer tools/call results distinguish completed work from input-required continuation. Annotations are untrusted absent a trusted source.

## MCP older tools

URL: https://modelcontextprotocol.io/specification/2025-11-25/server/tools

Read: 2026-10-11. Applied in: build spec.

Retained for existing client evidence: execution errors use isError and results may include structuredContent/outputSchema. Do not infer current-version fields in an older trace.

## MCP security

URL: https://modelcontextprotocol.io/docs/2025-11-25/tutorials/security/security_best_practices

Read: 2026-10-11. Applied in: build spec.

Versioned security guidance: reject audience-mismatched tokens and token passthrough; downstream authorization is a separate boundary. Only apply to a design using remote authorization.

## Anthropic evaluation

URL: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents

Read: 2026-10-11. Applied in: scope, build spec.

The transcript and environment outcome are distinct. Choose code, model or human checks for the property; action completion requires observable state.

## OpenAI evaluation

URL: https://developers.openai.com/api/docs/guides/evaluation-best-practices

Read: 2026-10-11. Applied in: build spec.

Include ordinary, edge and adversarial application cases. Match checks to where nondeterminism enters the selected architecture. Here this supports task acceptance design only.

## OpenAI retrieval

URL: https://developers.openai.com/api/docs/guides/retrieval

Read: 2026-10-11. Applied in: architecture, build spec.

File attribute filtering can narrow results before semantic search. Specify corpus identity/version/access scope; retrieval filtering does not replace service authorization.

## Anthropic retrieval

URL: https://www.anthropic.com/engineering/contextual-retrieval

Read: 2026-10-11. Applied in: architecture, build spec.

Published 2024-09-19. Exact identifiers can need lexical BM25 alongside semantic retrieval. Chunk context preserves document meaning. Historical benchmark improvements are not forecasts for the user.

## LangGraph interrupts

URL: https://docs.langchain.com/oss/python/langgraph/interrupts

Read: 2026-10-11. Applied in: build spec.

Resumption re-executes the interrupted node. Effects before interrupt risk replay. Separate approval and effects, and use replay-safe writes.

## LangGraph persistence

URL: https://docs.langchain.com/oss/python/langgraph/persistence

Read: 2026-10-11. Applied in: build spec.

Checkpointers capture thread state; stores serve cross-thread information. Delayed review needs suitable durable persistence and stable thread identity.

## LlamaIndex evaluation

URL: https://developers.llamaindex.ai/python/framework/module_guides/evaluating/

Read: 2026-10-11. Applied in: build spec.

Retrieval relevance and generated-answer support are different properties. Keep the retrieved source evidence available for acceptance checks.

## Authored working conventions

The process-map columns, decision table and brief coverage prompts are optional working aids; the requested answer shape controls presentation. Keep checks beside the relevant decision or interface, and do not add unspecified operational policies to exact-rule routing. The choice to keep one process per design is a package convention. They are not SDK or protocol mandates. Unknown settings remain proposals. Apply source rules only at the documented stack and version.

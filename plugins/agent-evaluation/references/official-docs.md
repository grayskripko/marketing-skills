# Official reference register

All URLs below were opened and their relevant content read on 2026-10-11. These are dated format snapshots. Use the supplied producer version and negotiated MCP revision when interpreting a record. The embedded checks do not depend on runtime fetching.

| Source and verified URL | Concrete knowledge used | Skill coverage |
|---|---|---|
| [Anthropic: Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents), read 2026-10-11 | Transcript claims differ from final environment state; code, model and human graders serve different checks. | Plan, export, outcomes, release |
| [Claude Code: programmatic use](https://code.claude.com/docs/en/headless), read 2026-10-11 | JSON `result` differs from `structured_output`; stream capture is partial until the result; documented stream command uses verbose output. | All four |
| [Claude Agent SDK: Python reference](https://code.claude.com/docs/en/agent-sdk/python), read 2026-10-11 | `ResultMessage.is_error` must be inspected even with success subtype; structured-output retry exhaustion is an error. Original platform.claude.com URL redirected here. | All four |
| [Codex: non-interactive mode](https://learn.chatgpt.com/docs/non-interactive-mode), read 2026-10-11 | JSONL event output differs from schema-constrained final output and the last-message file. Item IDs/types and terminal error events support execution checks. developers.openai.com/codex/noninteractive/ redirected here. | All four |
| [MCP tools specification, revision 2025-11-25](https://modelcontextprotocol.io/specification/2025-11-25/server/tools), read 2026-10-11 | JSON-RPC error and result `isError` are different; declared output schema governs `structuredContent`; annotations require trusted provenance. | All four |
| [OpenAI Agents SDK: tracing](https://openai.github.io/openai-agents-python/tracing/), read 2026-10-11 | Generation/function spans may carry sensitive payloads. Disabling `trace_include_sensitive_data` omits them rather than proving empty calls. | All four |
| [OpenAI Agents SDK: running agents](https://openai.github.io/openai-agents-python/running_agents/), read 2026-10-11 | `MaxTurnsExceeded` is an exception; handoffs/tools may occur before a final run result. | Plan, outcomes, release |
| [OpenAI: evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices), read 2026-10-11 | Tool selection, argument precision and handoff accuracy require separate application checks. Use explicit criteria for grader-record interpretation. | Plan, release |
| [OpenAI: optimizing LLM accuracy](https://developers.openai.com/api/docs/guides/optimizing-llm-accuracy), read 2026-10-11 | Wrong retrieved context and wrong response behavior are separate failure locations. This package checks source support; it does not infer retrieval cause without passages. | Outcomes |
| [LangSmith: evaluate a RAG application](https://docs.langchain.com/langsmith/evaluate-rag-tutorial), read 2026-10-11 | Correctness, groundedness, relevance and retrieval relevance compare different objects. A supported passage alone is not task correctness. | Outcomes |
| [LlamaIndex: evaluating](https://developers.llamaindex.ai/python/framework/module_guides/evaluating/), read 2026-10-11 | Retrieval can be evaluated independently of the response. Route stage diagnosis to the specialist rather than guessing from final text. | Outcomes |
| [LangGraph: interrupts](https://docs.langchain.com/oss/python/langgraph/interrupts), read 2026-10-11 | Resume restarts the interrupted node; pre-interrupt effects can repeat. Pending input is not completed approval. | All four |
| [LangGraph: persistence](https://docs.langchain.com/oss/python/langgraph/persistence), read 2026-10-11 | Checkpointers preserve thread state; stores preserve durable cross-thread data. Retain actual thread/checkpoint linkage when available. | Plan, outcomes, release |
| [JSON Schema: object](https://json-schema.org/understanding-json-schema/reference/object), read 2026-10-11 | Declared properties are not automatically required; null differs from absence; extra properties need an explicit policy. | Export |
| [DeepEval: evaluation introduction](https://deepeval.com/docs/evaluation-introduction), read 2026-10-11 | End-to-end, trajectory and component checks are distinct; execution through its real framework is different from preparing records. docs.confident-ai.com redirected here. | Runner boundary |
| [Claude Code: plugin manifest reference](https://code.claude.com/docs/en/plugins-reference), read 2026-10-11 | Manifest/resources are package metadata; loading is a separate host check. | Packaging |

## Authored operational conventions

These are this package's rules of thumb, not vendor requirements: the neutral case fields and ready/review statuses; joining requirements to safe evidence locators; retaining unresolved cases in a review collection; exporting provenance in a separate sidecar when the importer forbids metadata; and proposing a release hold for unresolved required outcomes. A supplied owner policy governs the actual readiness decision; producer runtime diagnostics do not add acceptance conditions. A schema-compatible preview may retain unresolved expectations as empty strings only when the complete supplied contract permits them, with review status and conflicts kept separately. No universal success threshold is invented.

## Competitors considered

Opened 2026-10-11: [DeepEval](https://deepeval.com/docs/evaluation-introduction), [MLflow skills](https://github.com/mlflow/skills), [verification-before-completion](https://www.skills.sh/obra/superpowers/verification-before-completion), and [Iris](https://glama.ai/mcp/servers/iris-eval/mcp-server).

DeepEval provides execution infrastructure; MLflow skills work with its tracking workflows; verification-before-completion requires verification before a completion claim; Iris provides trace/checking infrastructure. The useful difference here is a cross-host requirement-to-outcome report from the user's existing records, with action receipts, escalation and unresolved cases carried through the same acceptance decision. Prefer the existing native workflow when it already finishes that job. No measured superiority or replacement of their infrastructure is claimed.

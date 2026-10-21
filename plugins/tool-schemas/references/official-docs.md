# Official documentation and public references

Read 2026-10-11 UTC. Each URL below was opened during this build. These notes paraphrase public documentation. Rules about output order, minimal edits, redaction and authorization are package operating choices; they are not claims about a protocol requirement. Check the supplied host/version before applying a version-specific rule. Use only the sections needed for the requested repair or conclusion; these references do not require a report template or a broader verification job.

## MCP tools

- URL: https://modelcontextprotocol.io/specification/2025-11-25/server/tools
- Read: 2026-10-11
- Scope: Pinned 2025-11-25
- Applied knowledge: Schema and error boundaries; application to handler/consumer repairs. structuredContent objects match declared outputSchema; text serialization aids compatibility. isError identifies execution failures; JSON-RPC handles unknown tools and malformed requests.
- Loaded: HTTP 200; 690513 bytes. Resolved URL: https://modelcontextprotocol.io/specification/2025-11-25/server/tools

## Anthropic tool design

- URL: https://www.anthropic.com/engineering/writing-tools-for-agents
- Read: 2026-10-11
- Scope: Public engineering guidance, published 2025-09-11
- Applied knowledge: Tool boundaries, clear namespaces and meaningful context support usable interfaces. Applied to definitions and task-specific return fields, rather than broad prompt changes.
- Loaded: HTTP 200; 197025 bytes. Resolved URL: https://www.anthropic.com/engineering/writing-tools-for-agents

## OpenAI function calling

- URL: https://developers.openai.com/api/docs/guides/function-calling
- Read: 2026-10-11
- Scope: Responses and Chat Completions; strict:true
- Applied knowledge: Strict objects disallow extra properties and require every declared field. Nullable types represent optional values. Preserve the API-specific wrapper and handler semantics.
- Loaded: HTTP 200; 1472142 bytes. Resolved URL: https://developers.openai.com/api/docs/guides/function-calling

## Codex MCP

- URL: https://developers.openai.com/codex/mcp/
- Read: 2026-10-11
- Scope: Current hosted CLI documentation
- Applied knowledge: disabled_tools follows enabled_tools. Host filtering is distinct from interface semantics; preserve denials when patching an owned definition.
- Loaded: HTTP 200; 479834 bytes. Resolved URL: https://learn.chatgpt.com/docs/extend/mcp?surface=cli

## Claude Code MCP

- URL: https://code.claude.com/docs/en/mcp
- Read: 2026-10-11
- Scope: Current hosted Claude Code documentation
- Applied knowledge: MCP tool search can defer loading definitions. Inspect actual available/loaded definitions before interpreting a wrong-tool incident.
- Loaded: HTTP 200; 1534919 bytes. Resolved URL: https://code.claude.com/docs/en/mcp

## Claude Agent SDK custom tools

- URL: https://code.claude.com/docs/en/agent-sdk/custom-tools
- Read: 2026-10-11
- Scope: Current Python/TypeScript SDK docs
- Applied knowledge: tool()/@tool plus createSdkMcpServer/create_sdk_mcp_server defines registered tools. Zod or full JSON Schema carries bounds/optional fields. Defaults belong in handlers; controlled failures carry content plus isError (TypeScript) or "is_error" (Python). Python @tool forwards only content and is_error. Rechecked 2026-10-15, including SDK source https://github.com/anthropics/claude-agent-sdk-python/blob/main/src/claude_agent_sdk/__init__.py.
- Loaded: HTTP 200; 1078266 bytes. Resolved URL: https://code.claude.com/docs/en/agent-sdk/custom-tools

## Claude Agent SDK permissions

- URL: https://code.claude.com/docs/en/agent-sdk/permissions
- Read: 2026-10-11
- Scope: Current hosted permission rules
- Applied knowledge: allowedTools grants approval rather than an exclusive definition inventory. Preserve permission configuration while editing tool semantics.
- Loaded: HTTP 200; 585801 bytes. Resolved URL: https://code.claude.com/docs/en/agent-sdk/permissions

## OpenAI Agents SDK tools

- URL: https://openai.github.io/openai-agents-python/tools/
- Read: 2026-10-11
- Scope: Current Python SDK documentation
- Applied knowledge: Model-facing function tools use failure_error_function for error responses; None re-raises. Schema-backed program-owned calls disable the default free-form formatter: handler exceptions propagate unless a custom formatter returns schema-conforming JSON. Inspect the call path, output schema and custom error handler. Independently rechecked this distinction on 2026-10-11 at the same URL, under Programmatic Tool Calling and Handling errors in function tools.
- Loaded: HTTP 200; 252855 bytes. Resolved URL: https://openai.github.io/openai-agents-python/tools/

## LangChain tools

- URL: https://docs.langchain.com/oss/python/langchain/tools
- Read: 2026-10-11
- Scope: Current Python tools documentation
- Applied knowledge: ToolRuntime is injected at execution and excluded from the model-facing schema. Preserve trusted context in the runtime rather than exposing it as arguments. Examples read runtime.context by attribute with a dataclass context_schema (rechecked 2026-10-15).
- Loaded: HTTP 200; 1753022 bytes. Resolved URL: https://docs.langchain.com/oss/python/langchain/tools

## JSON Schema objects

- URL: https://json-schema.org/understanding-json-schema/reference/object
- Read: 2026-10-11
- Scope: General object semantics; respect supplied dialect
- Applied knowledge: properties alone does not require a property. Null and absence differ; additionalProperties governs undeclared fields.
- Loaded: HTTP 200; 709836 bytes. Resolved URL: https://json-schema.org/understanding-json-schema/reference/object

## OpenAI evaluation guidance

- URL: https://developers.openai.com/api/docs/guides/evaluation-best-practices
- Read: 2026-10-11
- Scope: Public task/agent evaluation guidance
- Applied knowledge: Tool choice, arguments and final functional outcome are distinct checks. Applied here to observable calls and user results only. Evidence requirements follow the particular claim: a selection claim for one question does not require unrelated agent-level empty/failure cases.
- Loaded: HTTP 200; 434038 bytes. Resolved URL: https://developers.openai.com/api/docs/guides/evaluation-best-practices

## Anthropic evaluation guidance

- URL: https://platform.claude.com/docs/en/test-and-evaluate/develop-tests
- Read: 2026-10-11
- Scope: Current public evaluation documentation
- Applied knowledge: Use task-specific expectations and relevant edge cases. Applied to interface success, empty and failure paths.
- Loaded: HTTP 200; 3277421 bytes. Resolved URL: https://platform.claude.com/docs/en/test-and-evaluate/develop-tests

## OpenAI retrieval

- URL: https://developers.openai.com/api/docs/guides/retrieval
- Read: 2026-10-11
- Scope: Current vector-store search documentation
- Applied knowledge: Search returns source identifiers, passage content and scores. Preserve provenance and supporting text in a tool response; do not turn score into a claim of truth.
- Loaded: HTTP 200; 1046374 bytes. Resolved URL: https://developers.openai.com/api/docs/guides/retrieval

## Anthropic grounding guidance

- URL: https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-hallucinations
- Read: 2026-10-11
- Scope: Current public grounding guidance
- Applied knowledge: Ground answers in supplied documents, quotes and citations. Applied to retrieval tool result evidence; corpus repair remains a separate job.
- Loaded: HTTP 200; 284286 bytes. Resolved URL: https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-hallucinations

## MCP Inspector

- URL: https://github.com/modelcontextprotocol/inspector
- Read: 2026-10-11
- Scope: Official public repository
- Applied knowledge: Existing call/schema inspection surface. Use actual results from the selected installed inspection surface for requested checks; distinguish inspection evidence from the proposed repair.
- Loaded: HTTP 200; 380618 bytes. Resolved URL: https://github.com/modelcontextprotocol/inspector

## AG2 tool builder

- URL: https://github.com/ag2ai/ag2-claude-plugins
- Read: 2026-10-11
- Scope: Public plugin marketplace repository
- Applied knowledge: Existing framework-specific tool building. Preserve the supplied framework and repair the existing interface for the requested task.
- Loaded: HTTP 200; 296822 bytes. Resolved URL: https://github.com/ag2ai/ag2-claude-plugins

## MCP tools current revision

- URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools
- Read: 2026-10-11
- Scope: Pinned 2026-07-28
- Applied knowledge: Required request _meta accompanies wire requests. Completed responses use resultType:complete; input_required continues a request rather than completing it. SDK adapters and examples must match the supplied revision. For an adapter repair, preserve continuation state and input prompts; distinguish completion of a status lookup from documented completion of the business action.
- Loaded: HTTP 200; 890167 bytes. Resolved URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools

## tool-design existing skill

- URL: https://raw.githubusercontent.com/muratcankoylan/Agent-Skills-for-Context-Engineering/main/skills/tool-design/SKILL.md
- Read: 2026-10-11
- Scope: Public skill source, current main branch
- Applied knowledge: Existing guidance addresses interface ambiguity and errors. Apply it where it resolves the supplied failure; derive edits and checks from the requested task.
- Loaded: HTTP 200; 20089 bytes. Resolved URL: https://raw.githubusercontent.com/muratcankoylan/Agent-Skills-for-Context-Engineering/main/skills/tool-design/SKILL.md

## Anthropic agent evaluation

- URL: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents
- Read: 2026-10-11
- Scope: Public agent evaluation guidance
- Applied knowledge: Execution transcripts and actual environment outcomes are separate evidence. Check real tool effects and user-facing results, not merely a successful return.
- Loaded: HTTP 200; 268207 bytes. Resolved URL: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents

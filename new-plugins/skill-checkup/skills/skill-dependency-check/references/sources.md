# Official source register

Read date for every source below: 2026-10-11, the build session date. Dates denote retrieval, not document publication. Facts are scoped to the named platform and documentation revision; inspect user-supplied versions before applying them to older installations.

| Key | Official source and URL | Deciding knowledge embedded in the skill |
|---|---|---|
| C | [Claude Code skills](https://code.claude.com/docs/en/skills) | Separate automatic and user invocation controls; plugin namespace and discovery locations; visibility overrides are not for plugin skills; dynamic shell injection is host-specific. |
| O | [Codex skills](https://developers.openai.com/codex/skills/), redirected to [Build skills](https://learn.chatgpt.com/docs/build-skills) | Repository `.agents/skills` discovery; explicit invocation remains available when implicit invocation policy is false. |
| A | [Claude Agent SDK skills](https://code.claude.com/docs/en/agent-sdk/skills) | Explicit empty setting sources exclude filesystem skill loading; working directory and current skills allowlist affect discovery. |
| M | [MCP tools specification](https://modelcontextprotocol.io/specification/2025-06-18/server/tools) | Tool declaration and input schema identify the call contract; JSON-RPC errors differ from tool-result errors. The date in the URL identifies the inspected specification revision. |
| S | [OpenAI Agents SDK MCP](https://openai.github.io/openai-agents-python/mcp/) | Tool-list cache may become stale; the documented instance cache invalidation method refreshes discovery. |
| P | [OpenAI plugin packaging](https://developers.openai.com/plugins/build/plugins) | Codex compatibility manifest remains documented; skill and asset paths resolve from plugin root. Root portable manifests are another supported format, not included in this requested dual-manifest package. |

## Authored operational rules

Small proposed patches, no execution or network, supplied-artifact-only scope, incomplete-inventory handling and case-first answers are this plugin's operational rules, not platform requirements. Never interpret an error alone as proof that a remote write did not occur. No claim of host installation, automatic selection or successful command execution follows from a static review.

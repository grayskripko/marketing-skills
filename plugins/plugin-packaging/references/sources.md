# Packaging sources

Read and URL availability verified 2026-10-11. Official documentation rules are scoped to the named format. The diagnostic workflow, small-patch preference, inventory completeness labels and receipt stages are this package’s operational conventions. They are not claims that all hosts share a schema.

| ID | Official page | Embedded knowledge |
|---|---|---|
| C1 | https://code.claude.com/docs/en/plugins-reference — read 2026-10-11 | Manifest location; component paths relative to the plugin root; existence and containment; root-skill `.` exception from v2.1.221; remote MCP HTTPS exception; marketplace strictness and restricted skill scans; custom skills scans add to the default; unknown top-level keys versus strict objects; dependency forms and own-marketplace bare-name resolution; `claude plugin validate`; `bin/` restriction on claude.ai/Cowork. |
| C4 | https://code.claude.com/docs/en/plugin-dependencies — read 2026-10-11 | Root marketplace cross-marketplace installation allowlist; installed and enabled same-scope alternative; qualification alone is insufficient. |
| C3 | https://code.claude.com/docs/en/plugins — read 2026-10-11 | Local development loading with `--plugin-dir` requires no marketplace; enabled hooks and MCP servers can execute during a host session. Inspect components before loading. |
| C2 | https://code.claude.com/docs/en/skills — read 2026-10-11 | Skill directories and front matter; namespacing; manual versus automatic invocation controls; descriptions are metadata, full body loads on invocation. |
| O1 | https://developers.openai.com/plugins/build/plugins — read 2026-10-11 | Codex compatibility scaffold remains supported with `.codex-plugin/plugin.json` and `skills: "./skills/"`; portable format uses root manifest and fixed component locations; `extensions.com.openai` replaces the compatibility overlay rather than merging it. |
| A1 | https://code.claude.com/docs/en/agent-sdk/skills — read 2026-10-11 | Filesystem discovery, current default user/project sources, explicit source overrides, cwd and allowlist; explicit tools list must include Skill; system init skills array lists user-invocable skills only, independently of the allowlist; captured Skill and Read events. |
| M1 | https://modelcontextprotocol.io/specification/2025-11-25/server/tools — read 2026-10-11 | Protocol errors differ from execution errors returned with `isError: true`; discovery schemas and call results are separate artifacts. |
| S1 | https://openai.github.io/openai-agents-python/mcp/ — read 2026-10-11 | OpenAI Agents SDK tool-list caching and instance-level `invalidate_tools_cache()`; cached discovery is not completion evidence. |

C1 version details: `icon`, `documentationUrl`, `supportUrl`, `privacyPolicyUrl` and `termsOfServiceUrl` validate without warnings starting with Claude Code v2.1.281 (not `category` or `tags`); some extra component-path validation needs v2.1.283. Do not interpret an older validator’s warning without the actual host version. A manifest’s supported current syntax cannot establish that an older colleague’s runtime accepts it.

O1 verification replaces the broad Codex plugins page, which redirected to https://learn.chatgpt.com/docs/plugins. The retained packaging URL loads the actual manifest documentation. A1’s older platform.claude.com URL redirects to the retained code.claude.com URL. Only the URLs retained above are operational source links.

Fix verification 2026-10-11: reopened C1, C2 and A1. Newly corrected rules are supported by C1’s Path rules, Marketplace entries and the manifest, and Standard layout sections, and A1’s Confirm skills loaded section. These links are source references, not bundled copies of the official documents.

Answer-first edit verification 2026-10-11: checked C4’s cross-marketplace section and A1’s session tools, settings sources and named dispatch guidance. For SDK configuration repairs, present the requested option changes together and distinguish tool availability from pre-approval; retain invocation controls and evidence boundaries.

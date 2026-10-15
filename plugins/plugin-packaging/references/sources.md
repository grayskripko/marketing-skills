# Packaging sources

Official pages behind the host rules the skills state. Rules were rechecked against these pages on 2026-10-15, except M1 (read 2026-10-11). The diagnostic workflow, small-patch preference and receipt stages are this package's own conventions, not host rules.

| ID | Official page | Rules taken from it |
|---|---|---|
| C1 | https://code.claude.com/docs/en/plugins-reference | Manifest location; component paths relative to the plugin root, `./`, existence and containment; `skills: "."` (failed validation before v2.1.221); `skills` adds to the default scan; unknown top-level keys stripped with a validate warning; directory listing fields only in `plugin.json`; reserved plugin names; marketplace `strict` and root-source skill selection; `bin/` not installed by claude.ai or Cowork. |
| C2 | https://code.claude.com/docs/en/plugins/marketplace-reference | Relative plugin sources resolve from the marketplace root; `url` marketplaces fetch only `marketplace.json`; `category` and `tags` are entry fields. |
| C3 | https://code.claude.com/docs/en/plugin-dependencies | Bare and qualified dependency names; root-marketplace `allowCrossMarketplaceDependenciesOn`; already installed and enabled dependency at the same scope is exempt. |
| C4 | https://code.claude.com/docs/en/skills | `disable-model-invocation` and `user-invocable` controls. |
| A1 | https://code.claude.com/docs/en/agent-sdk/skills | Init `skills` array lists user-invocable skills only; `user-invocable: false` skills load but are absent; `/<name>` dispatch does not depend on the `skills` option. |
| A2 | https://code.claude.com/docs/en/agent-sdk/claude-code-features | `settingSources`: `project` = `<cwd>/.claude/settings.json`, `local` = `.claude/settings.local.json`; empty list loads none. |
| M1 | https://modelcontextprotocol.io/specification/2025-11-25/server/tools | Protocol errors differ from tool execution errors returned with `isError: true`. |
| O1 | https://developers.openai.com/plugins/build/plugins | Codex compatibility layout `.codex-plugin/plugin.json`, paths relative to the plugin root starting with `./`, `skills: "./skills/"`. |

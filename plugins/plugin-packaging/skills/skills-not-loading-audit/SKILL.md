---
name: skills-not-loading-audit
description: "A question about why the user's own skills-only Claude plugin fails to install, has skills not loading or cannot find its files, even a quick one before the manifest is pasted. Find why a skills-only Claude plugin works locally but fails to install, load skills or find its resources for colleagues. Use when the user reports “plugin not loading,” “missing skills,” or “the companion is installed but cannot be found” and supplies a plugin manifest, package inventory, marketplace declarations, configs or logs. Locate broken references and unresolved plugin dependencies against the named host’s package rules. Return the exact failing path or declaration and a small repair list. Not for writing a new plugin, changing a skill’s behavior, or diagnosing one valid skill’s task selection."
---

# Audit an existing plugin package

Find the defect that stops the package loading, its skills being discovered, or its files being found on a colleague's machine, and give the edits that fix it. Use plugin-manifest-repair when the user authorizes local edits, plugin-install-check for runtime evidence.

If nothing has been supplied yet, answer the question in general terms, name the manifest, file list, log or transcript that would settle it for this package, and ask for it.

## What to check

1. Inventory scope. If only a subset was supplied, unlisted files are "not supplied", not missing. The author's checkout and the installed tree are different; a file outside the marketplace source directory or behind a symlink does not ship.
2. Manifest paths and every link in each SKILL.md, resolved from the file that contains it, compared with the inventory character for character (case matters on Linux).
3. Marketplace entry against the manifest, and dependencies (rules below). Keep separate: wrong marketplace, not in the allowlist, installed but disabled, dependency cycle, missing external program, and a tool call that ran and failed.
4. Executable parts (hooks, MCP servers, `bin/`): report them; do not run them.

## Package rules

- Claude Code manifest: `.claude-plugin/plugin.json`; everything else at the plugin root. Component paths are relative to the plugin root, start with `./`, must exist and stay inside it. `skills` adds to the default `skills/` scan.
- Unknown top-level manifest keys are stripped and the plugin still loads; `claude plugin validate` warns. A warning is not a load failure.
- Marketplace entry with a `plugin.json` present: default `strict: true` appends the entry's `skills` to the manifest; `strict: false` with any entry component field is a conflict and the plugin fails to load. An entry whose source is the marketplace root and that lists `skills` subdirectories loads only those and skips the default scan, so `--plugin-dir` locally can find skills the marketplace install does not.
- Relative marketplace sources start with `./` and resolve from the marketplace root (the folder holding `.claude-plugin/`). A marketplace added by direct `url` fetches only `marketplace.json`, so relative sources cannot resolve.
- Dependencies: a bare name resolves in the plugin's own marketplace; `name@marketplace` names another. Installing from another marketplace also needs that marketplace in `allowCrossMarketplaceDependenciesOn` of the root marketplace's `marketplace.json`, unless the user already has the dependency installed and enabled at the same scope. Show the allowlist as an added field, keeping existing entries you were not shown.
- A plugin dependency does not install an external program it calls.
- claude.ai and Cowork do not install a plugin that has a top-level `bin/`.
- MCP: a result with `isError: true` is a failed tool call even though JSON-RPC returned a result.
- Codex: the compatibility layout is `.codex-plugin/plugin.json` with paths relative to the plugin root, e.g. `"skills": "./skills/"`. Discuss the root `plugin.json` portable layout only if the user is migrating to it.

<!-- Sources, checked 2026-10-15: https://code.claude.com/docs/en/plugins-reference (paths, unknown keys, strict, root-source skills, bin/) ; https://code.claude.com/docs/en/plugins/marketplace-reference (relative sources, url sources) ; https://code.claude.com/docs/en/plugin-dependencies (allowlist, installed-and-enabled exception) ; https://modelcontextprotocol.io/specification/2025-11-25/server/tools (isError; read 2026-10-11) ; https://developers.openai.com/plugins/build/plugins (Codex compatibility layout) -->

## Answer

- Lead with the diagnosis and give every edit the request needs, each the smallest one, as exact file text or a field change at an exact path.
- When the records cannot settle a choice (which edge of a dependency cycle to drop, relink or rename), still give one concrete edit, say it is the user's or the owner's call, and do not invent a reason for it.
- State a platform rule only when it decides this fix. If the rule is not visible in the user's records (a version boundary, a host behaviour), name the doc page it comes from; if you cannot, say you cannot tell and name the check that would.
- Keep a requested length or format. Never invent missing file contents, marketplace names or versions.

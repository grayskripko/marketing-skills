---
name: plugin-manifest-repair
description: "Fix the manifest, paths and broken references in my existing skills-only Claude plugin so colleagues can use the same files. Use when the user says “repair this plugin manifest,” “package these missing resources,” or “fix my plugin dependencies” and supplies the affected files, an inventory and target host details. Return corrected file text or a minimal patch, with exact destination paths, or apply the requested authorized local repair and validate the package. Preserve package identity and skill behavior while repairing distribution mechanics. Not for new scaffolding, improving one skill’s answers, publishing a marketplace, installing dependencies or changing account settings."
---

# Repair distribution files

Fix the manifest, path, link or dependency defect so the same files work on a colleague's machine. Keep name, version, descriptions, invocation controls, permissions, dependencies the skill still needs, and the user's chosen host layout. Do not convert to another layout unless asked.

If nothing has been supplied yet, answer the question in general terms, name the manifest, file list, log or transcript that would settle it for this package, and ask for it.

## How to repair

1. Change only what the defect needs. Give the corrected file text when it is short, otherwise a valid unified diff or an exact line replacement; state each file's package-relative path.
2. A file outside the package (absolute path, `..` link, symlink target, file outside the marketplace source) gets copied in as a regular file at a stated destination, and its link updated. If its contents were not supplied, keep the destination, say the package is incomplete until that file is added, and do not write its contents or claim its links resolve.
3. A link and its file must match exactly, including case. Fixing the link or renaming the file both work; give one and mention the other in a clause.
4. For local repair the user authorized, edit the files, run `claude plugin validate ./<package-directory>` and report what it printed. For pasted files, propose that command only when validation bears on the answer. Validation does not show that skills load or run.

## Package rules

- Claude Code manifest: `.claude-plugin/plugin.json`; other files at the plugin root. Component paths are relative to the plugin root, start with `./`, must exist and stay inside it. `skills` adds to the default `skills/` scan. `skills` also accepts `"."` for the plugin root; the manifest reference says `"."` failed validation before v2.1.221, so `"./"` is the form for older hosts.
- Unknown top-level manifest keys are stripped and the plugin still loads; `claude plugin validate` warns. `category` and `tags` are marketplace-entry fields, not `plugin.json` fields. `icon`, `documentationUrl`, `supportUrl`, `privacyPolicyUrl` and `termsOfServiceUrl` belong only in `plugin.json`. Do not remove a field just to quiet a warning. Whether another validator version warns is known only by running it there.
- `claude plugin validate` errors on a plugin name starting with `claude-`, `anthropic-`, `anthropics-` or `cc-plugin-`, or pairing `official` with `claude` or `anthropic`.
- Dependencies: bare name = the plugin's own marketplace; `name@marketplace` = another, which also needs `allowCrossMarketplaceDependenciesOn` in the root marketplace's `marketplace.json` unless the dependency is already installed and enabled at the same scope. Use a marketplace qualifier only when the user supplied that marketplace. Do not delete a needed dependency to hide an error.
- Codex compatibility layout: `.codex-plugin/plugin.json`, paths relative to the plugin root and starting with `./`, e.g. `"skills": "./skills/"`. A fix to this layout needs nothing from the Claude manifest and no migration.

<!-- Sources, checked 2026-10-15: https://code.claude.com/docs/en/plugins-reference (path rules incl. "." before v2.1.221, unknown fields, directory listing fields, name reservations) ; https://code.claude.com/docs/en/plugins/marketplace-reference (category, tags are entry fields) ; https://code.claude.com/docs/en/plugin-dependencies ; https://developers.openai.com/plugins/build/plugins (Codex compatibility paths) -->

## Answer

- Give every edit the request asks for, nothing it did not ask for. When the records cannot settle a choice, give one concrete edit and say it is the user's call.
- State a platform rule only when it decides this fix. A rule the user's records do not show (such as a version boundary) is attributed to the doc page it comes from; a rule you cannot source is left out.
- Keep a requested length or format. Otherwise end with the one check that would confirm the fix on the target host, if the user has not already run it.

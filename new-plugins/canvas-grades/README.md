# Canvas Grades

Review a Canvas gradebook export and proposed upload; preserve IDs and produce a grade-change diff with rejected or unintended assignment changes.
For instructors and course administrators reviewing grade imports.
Needs an original export, proposed CSV and intended corrections; a fresh export and preview or history text support result reconciliation. No account, key, install or paid API is required for pasted data.

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories are platform metadata, not servers. Development notes and evaluation records are also present in this working folder.

Both skills analyze pasted CSV or files you explicitly supply, instruct the assistant to use a CSV parser for quoted commas and newlines, and may create a separate corrected local file only when requested. Parsing and file creation use the assistant's existing tools; no parser program or installer is bundled. This is not a strict no-execution workflow. The instructor performs exports and imports in Canvas; the skills do not access Canvas accounts, call the Canvas API, send messages, publish assignments, or change grades or account settings.

Ordinary reviews fetch nothing. If a deciding rule needs refreshing, both skills permit the assistant's existing web tool to retrieve only these four official documentation URLs and their redirects:

- https://community.instructure.com/en/kb/articles/660862-how-do-i-import-grades-in-the-gradebook
- https://community.instructure.com/en/kb/articles/660866-how-do-i-export-grades-in-the-gradebook
- https://community.instructure.com/en/kb/articles/660864-how-do-i-view-the-history-of-all-grading-changes-in-the-gradebook
- https://developerdocs.instructure.com/services/canvas/resources/gradebook_history

These retrievals make network requests and disclose the requested URL and ordinary connection metadata to the destination sites, redirect destinations, and the assistant's tool provider. Student data, CSV cells, IDs, private context, supplied error text, and credentials must never be included in requests. The fourth URL is documentation, not an API endpoint to call. The references also direct rule refresh before submission and when preview evidence conflicts. Missing rule evidence can be left unresolved. Repository and support links identify documentation or support; they do not direct account connections or message delivery.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, tool activity, and temporary files under its own terms. Requested corrected files use the assistant's existing file tools and the user's chosen local destination.

## Skills

- `review-canvas-upload`: produce a proposed-change diff, flag rejected or unintended edits, and prepare a corrected local copy when requested.
- `reconcile-canvas-import`: compare original, proposed and actual grades and separate observed changes from confirmed rejection evidence.

Paste full CSV headers and rows, or provide files. Keep student and assignment IDs intact. Include course and export times, points possible, grade types, grading-period settings and exact preview messages where relevant. Samples support only the supplied rows.

Source rules were checked on 2026-10-11. See either skill’s references/canvas-rules.md for dated URLs and the override-column documentation conflict.

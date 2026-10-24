# Salesforce Imports

Why did my Salesforce import fail, and should I insert, update, or upsert these records?

For Salesforce admins and operations teams repairing imports. Needs pasted error text, CSV exports, field settings, or screenshots or their descriptions. Analysis needs no account, keys, installs, or paid API. Running the recommended import yourself requires a Salesforce account and the appropriate object and import permissions.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

Analysis uses task text, attachments, and local files you explicitly supply. The skills do not direct code execution, software installation, Salesforce API calls, account connections, message delivery, or import execution. Any local output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

This package has an optional network workflow: only when you explicitly request a documentation refresh may the assistant retrieve the listed public official documentation URLs in the skill references using its existing browser/web tool. Destinations are `help.salesforce.com`, `developer.salesforce.com`, and `trailhead.salesforce.com`. Those sites and the assistant's retrieval infrastructure receive the requested public URL and ordinary connection metadata. Private row values, record IDs, credentials, and org URLs must not be included in requests or searches. The supplied-material analysis workflow does not require these requests; paste the relevant documentation if retrieval is unavailable. Repository and support links identify documentation or support locations, not account connectors.

The skills also describe actions you perform in Salesforce: sign in through Salesforce's interface, inspect settings and records, obtain exports and result logs, adjust mappings or Data Loader options, and run a representative test or import after the stated checks. Those user actions can read or change Salesforce records; the assistant prepares advice and requested files and does not perform them.

The publisher receives no task data through this plugin and operates no collection, telemetry, or storage service for it. Your assistant provider processes and may retain your conversation, attachments, and tool activity under its own terms.

- **Diagnose import errors:** get a row-level cause, concrete repair, and retry or hold.
- **Choose import matching:** select Data Import Wizard or Data Loader guidance, insert/update/upsert, object-specific match keys and External IDs, and target/parent relationship mappings that respect whether new records are allowed.
- **Review import results:** compare supplied success/error logs with an admin-visible post-import export, check intended field changes and parent relationships, hold missing or ambiguous outcomes, and prepare retries containing only confirmed failed rows.

Start with the object, importer, selected operation and matching field, then a few redacted rows and exact errors. Partial input still gets a useful conditional answer. A screenshot description is treated as your report, not as independently inspected account state.

The assistant can walk you through Setup → Data Import Wizard, operation selection, field mapping, and result review, or point you to Salesforce's Data Loader instructions. You enter credentials only in Salesforce's own sign-in flow. These skills prepare recommendations and files; they do not connect to an org or execute imports. Pasted exports remain the no-setup path.

Platform knowledge was verified on 2026-10-11. Org settings, edition, permissions, storage and automation still determine the actual outcome.

See [privacy](PRIVACY.md) and the skill reference files for source dates and scope. MIT license.

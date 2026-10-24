# Jira Automation

Create, edit and diagnose Jira Cloud automation rules from supplied requirements, configuration and audit evidence.
For people maintaining Jira Cloud automation. Needs pasted steps, a rule export, audit-log text, or your description of screenshots. Analysis needs no Jira account, keys, installs, or paid API.

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference notes, JSON platform metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect a Jira account. Build notes, reviews and text-only test records are development material, not a runtime.

This is not a strictly offline workflow. Both skills may use your assistant's existing web tool to fetch relevant public documentation from `support.atlassian.com` and `developer.atlassian.com`, following official documentation redirects only within those hosts. They direct verification of unfamiliar syntax or changed deciding facts. Those requests disclose the requested documentation URL and ordinary connection metadata to Atlassian and the assistant's tool provider; supplied rule exports, logs and private endpoints are not uploaded to those sites. Private Jira sites, URLs embedded in supplied material and arbitrary user links are not fetched. GitHub metadata and support links identify the publisher and support pages; they are not skill retrieval destinations.

The skills analyze material you supply and return diagnoses, builder steps, JSON action fragments and test plans. They do not direct code execution, software installation, API calls, account connections or assistant-performed Jira changes, file writes, publishing or message delivery. They can guide a global administrator to export flows (which downloads a file), and guide you through saving rules, creating and enabling a logging-only diagnostic copy, inspecting its audit and disabling it again. Actual field edits or notifications require your applicable authorization in Jira. Drafts may describe email, comments, item creation or authenticated web requests; these are proposed Jira actions, not requests executed by the assistant. You apply and test them in your own Jira account.

The publisher operates no task-data collection, telemetry or storage service. Your assistant provider processes and may retain conversations, supplied files and web-tool activity under its own terms. Redact personal data, credentials and private endpoints before sharing material.

- **Diagnose Automation Failure:** explains a failed save, failed run, or incomplete result using the supplied evidence.
- **Rewrite Automation Rule:** creates new rule drafts and edits existing rules, covering triggers, conditions, branches, actions, smart values, actor permissions and audit-log tests while preserving the intended result.

Include the exact error, intended outcome, trigger, conditions and actions. If known, include plan, ordinary or advanced flow, scope, actor permissions and one failing item's relevant fields. Redact names, account IDs, private URLs, webhook addresses and secrets. A partial screenshot description can yield a provisional explanation; an exact component count needs the relevant export structure.

For an export, an agent can guide a global administrator through Jira settings → System → Automation flows → More actions → Export flows. This exports all global and project flows: extract and redact only the relevant rule before sharing. Pasted steps remain a no-setup option.

The output is a diagnosis or a buildable draft, not an import-ready export or an executed change. Rules stay in your Jira instance until you choose to apply them. For a diagnostic test, create a disabled copy, replace every effect-producing action with logging, and constrain its trigger to a known test item. Enable only that diagnostic copy for the authorized test, inspect its audit details, then disable it. Test actual edits or notifications under your applicable authorization.

See [PRIVACY.md](PRIVACY.md) for execution, connection and retention scope.

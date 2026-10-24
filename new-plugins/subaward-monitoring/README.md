# Subaward Monitoring

Convert US federal subrecipient reports, award terms and audit findings into a 2 CFR 200.332 monitoring checklist with evidence, owners and corrective actions.
For US federal pass-through grant managers reviewing subrecipients.
Needs pasted award terms, reports and findings, or user-selected readable exports. No account, keys or installation beyond loading the plugin.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon, with development notes and evaluation records. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

The supplied-text/export review needs no network, but these skills also direct public-source retrieval when a deciding rule needs refreshing or a historical version is needed. Your assistant's existing web tool may read the source-register URLs on `www.ecfr.gov` (CFR sections), `www.govinfo.gov` (dated CFR PDFs), and `www.fac.gov` (FAC guidance), or an official agency URL you supply for award implementation, including redirects. These are real network requests: the contacted sites, redirect destinations and tool provider receive the requested URL and ordinary connection metadata. Report text, identifiers and private context must not be put in queries or uploaded to those sites. If refresh fails, the skills identify the exact unresolved decision after the useful deliverable.

The skills do not direct code execution, software installation, authenticated API calls, account access, message delivery, publication or account-setting changes. Monitoring means a written checklist or follow-up tracker, not a background listener. Notifications, repayments, award amendments, management decisions and FAC submissions are review tasks or drafts for responsible people, not actions performed by this plugin. A spreadsheet correction is returned as advice; local files are read only when selected by you, and an output file is created only when explicitly requested through your assistant's existing file tools.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. GitHub source, documentation and support links identify package information; they are not workflow retrieval endpoints.

## Skills

- **monitoring-checklist:** Build a review table from subaward terms, risk information and financial/performance reports.
- **audit-follow-up:** Turn audit findings and corrective-action records into a responsibility and follow-up table, including management-decision timing.

Each table links evidence to its document and location, separates unknown evidence from a documented problem, and labels proposed owners and dates. The source pack includes current subaward field rules, award-specific versus cross-cutting findings, fiscal-year audit thresholds and the FAC acceptance clock.

## Inputs

Paste excerpts with document names, dates and page/section labels, or select text, Markdown, CSV or other exports readable by your assistant. Include amendments, fiscal-year dates, entity type, entity-wide Federal expenditures and the FAC acceptance date when relevant. An audit summary alone may omit the corrective-action plan and prior findings schedule.

[Privacy](PRIVACY.md) · [License](LICENSE)

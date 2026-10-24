# Help Articles

Check and fix your help articles and saved replies against approved policies, with exact replacements and source references.

For support leads and help-content owners. Supply current approved policies or release notes, article and saved-reply exports, and optional ticket text with unnecessary private details removed. Include stable IDs, effective dates, and plan, language or location setting, or version details where they affect the answer.

No accounts, connector setup or paid APIs are required. Paste text for the no-setup path. Your AI app must be able to read supplied files or images; paste readable text if it cannot. AI model usage and access to your helpdesk's exports may cost money.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The `.claude-plugin` and `.codex-plugin` directories contain platform metadata for the same skills; neither provides a runtime or server. Supplied attachments may be read with your assistant's existing file or image readers; if an input is unreadable, paste its text. No OCR software or calculation program is installed or run by these instructions.

## Skills

| Skill | Give it | You get |
|---|---|---|
| audit-support-content | Approved sources plus articles and replies | Conflicting wording, exact source locations and proposed replacements |
| update-articles-and-macros | Approved changes and the passages to update | Replacement blocks with separate notes on sources and where and when each change applies |
| find-ticket-driven-content-gaps | Ticket excerpts with unnecessary private details removed, existing content and approved facts | Gaps linked to tickets, supported additions and questions for unverified fixes |

## Examples

- “Compare our cancellation policy with these articles and saved replies. Find missing exceptions and give replacement text.”
- “Apply these approved release changes to the attached help page and macros.”
- “People keep getting stuck on this guide. Use these ticket excerpts to show which steps need clarification.”

The audit skill finds problems across a library. The update skill applies known changes to specific passages. The gap skill starts from tickets. A request can need more than one; do not repeat the same findings in each output.

## Review and limits

Use supplied approved facts without an additional approval step. Follow your stated review requirements. Conflicting approved policies and unverified claims need an owner decision before those claims can be used. Different plans, regions and product versions are compared separately. Ticket workarounds are proposals until someone confirms where and when they apply.

Public copy is separate from ticket evidence and internal instructions. Review notes appear in the same conversation or requested file. Keeping them apart makes public copy easier to copy; it does not restrict access to the notes. Actions in saved replies (macros) are reviewed only when you supply them and your approved rules. Reply text alone does not show what a macro changes in the account. You can get ready-to-paste drafts. For a vendor import file, supply a verified description of the required file format.

This review links content changes to their sources. It does not certify compliance with policies, sort general support tickets or analyze customer satisfaction (CSAT). It does not publish, send, change accounts or monitor a live inbox.

## Data and network

Network scope: none. No URL, robots.txt, web search, helpdesk endpoint or other service is fetched. No telemetry. The instructions use only material you supply for the task. There is no executable service, connector or background process.

Redact names, contact details, credentials and private case details before sharing; stable ticket IDs can still be sensitive. The plugin creates no separate storage. Your AI host handles conversation, uploaded-file and output retention under its own terms. If you request a local output file, that file remains until you delete it. See [PRIVACY.md](PRIVACY.md).

## When inputs are incomplete

Paste text if a file or scan cannot be read. Supply the approved version and effective date if policies conflict. With no approved fix, you can still get a gap list and a marked draft for review.

## Support and license

Report issues through the repository's issue tracker: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).

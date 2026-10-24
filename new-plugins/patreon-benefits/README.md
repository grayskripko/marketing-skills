# Patreon Benefits

Work out who should receive this month's Patreon benefits and explain missing rewards from pasted member exports.
For creators and media teams managing monthly reward delivery. Needs the benefit month, tier terms and pasted rows or a user-selected export; month eligibility and delivery records resolve payment and duplicate-delivery questions. No keys, installation of connectors or live account access are needed.

| Skill | Input | Deliverable |
|---|---|---|
| [patreon-benefit-list](skills/patreon-benefit-list/SKILL.md) | Benefit month, member export, tier terms, delivery records | Ready, awaiting renewal, delivered and unresolved rows with scoped totals |
| [patreon-benefit-exceptions](skills/patreon-benefit-exceptions/SKILL.md) | Affected rows, statuses, month/access date and benefit terms | Member-by-member explanation and correction checklist |

## Prepare an export

In Patreon on desktop, open Creator studio → Audience → Relationship Manager → Benefit Eligibility Status. Select current or previous month and the relevant tier, then export the viewed list. Include the month, capture date and filters when sharing it. For older periods use the saved period export or payment history. The general Relationship Manager CSV inherits its active filters; it may not cover everyone owed a benefit.

Paste rows directly or select a local file for your assistant to read. Keep stable row IDs and replace full addresses with present/missing unless an address deliverable is needed. Add the actual benefit terms and completed-delivery rows. Gifted access needs separate inspection because the Benefits delivery ledger omits gift-only accounts.

## Examples

- “Make June's archive-access list for Marigold Sound from this tier export and June eligibility view.”
- “Juniper Films has gifted members missing from Benefits. Explain who still gets our screening link.”

## Data and network

Network requests: none. The skills read supplied text and user-selected files, using embedded official reference knowledge. They ship no executable code, MCP servers or connectors. They produce tables and proposed actions in the conversation. They do not send messages, deliver benefits, update completion, change tiers or process payments. No telemetry or plugin-operated storage. See [PRIVACY.md](PRIVACY.md).

## Sources and support

[Official knowledge register](skills/patreon-benefit-list/references/patreon-rules.md), verified October 11, 2026. Each entry records the displayed update date, actual read date and rule scope.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT — see [LICENSE](LICENSE).

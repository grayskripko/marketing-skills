# Support Targets

Explain why Zendesk tickets got an SLA target, which targets breached, and why SLA percentages differ from ticket counts.

For support operations teams reviewing Zendesk SLA reports from comment-based ticket workflows. Live-chat and messaging reply-event reconciliation is outside this package’s scope. Supply pasted policy text, ticket events, metric-instance rows and schedules, or readable CSV/JSON exports. No account connection, keys, installation of a connector or paid API is needed.

## Skills

- **sla-policy-match** — explain which ordered policy and priority target applied at each relevant ticket update, including schedule and advanced-setting history.
- **sla-breach-ledger** — reconstruct measured instances, clock segments and breaches; explain report filters, exclusions and the denominator.

For a full reconciliation, check policy history first, then build the instance ledger using those findings.

## Inputs that decide the result

Include policy order and All/Any conditions; system Priority values and changes; target units and business/calendar basis; policy change dates; schedule timezone, weekly hours, holidays and assignment history; advanced settings; comment visibility and actor/requester roles; metric events and report filters. Redacted ticket IDs are enough. Partial inputs yield a partial ledger with the exact missing evidence beside the affected rows.

## Data and network

The skills read only supplied text and task-relevant local files. They fetch no URLs, call no APIs and send no ticket data. Bundled dated official-source references supply the platform rules. They write no account changes and retain no data themselves. See [PRIVACY.md](PRIVACY.md).

## Example requests

- “Why did our VIP ticket match the general policy?”
- “Our ticket count differs from the next-reply denominator. Explain these rows.”
- “Does this internal note satisfy the target under these historical settings?”

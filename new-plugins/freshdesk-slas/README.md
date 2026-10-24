# Freshdesk SLAs

Convert Freshdesk SLA days to hours and explain ticket due times using your policies, working hours, holidays and ticket history. Include account rollout evidence when available; conversion proposals remain separate from deployed settings and historical ticket results.
For support administrators reviewing Freshdesk policies and ticket deadlines. Needs pasted policy targets and conditions, ordered policies, group schedules with time zones and holidays, ticket event times, and account rollout evidence when available. Missing rollout evidence yields conditional results. No keys, additional accounts or installs are needed for the pasted-text path.

## Skills

- **convert-sla-targets**: a worksheet of original targets, proposed hours, calendar-specific policy splits, preserved conditions and unresolved decisions.
- **reconcile-sla-deadlines**: recorded versus reconstructed due times, counted working intervals and evidence for differences.

Paste text or provide CSV/JSON exports as local files. Include product (Freshdesk or Freshdesk Omni), plan, signup cohort, configuration dates and the account's migration notice or observed rollout evidence. For tickets, include priority, group, channel/source for Omni, applied policy, created time, response events, status changes and any due-time edits. Use ticket labels instead of customer names.

The package contains instructions and embedded references. Network fetches: none during skill use. It has no connector, account mutation or background service. Calculations use supplied calendar and timeline evidence. Read the dated [source register](references/freshdesk-sources.md) for platform behavior and cohort differences.

For conversion, ticket histories are optional. For reconciliation, supply the applicable targets and ticket history. Use either skill separately or request both outputs.

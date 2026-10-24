# Statuspage rule register

Scope: Atlassian Statuspage Cloud incident drafting. All four sources loaded and were independently re-read for this rework on 2026-10-11. No article publication or update date was displayed; verification date is not a publication date. They describe the current pages at build time, not future policy.

| Official source | Decision-changing knowledge | Read date |
|---|---|---|
| [Create an incident](https://support.atlassian.com/statuspage/docs/create-an-incident/) | Four states distinguish unknown cause, confirmed cause with repair underway, believed successful repair awaiting symptom clearance, and eliminated cause with full performance. Fields: representative name, state, message, affected components and notification choice. Maximum 100 open incidents. At least one affected component is required for the notification option. | 2026-10-11 |
| [Top-level status and incident impact calculations](https://support.atlassian.com/statuspage/docs/top-level-status-and-incident-impact-calculations/) | Component statuses: Operational, Under Maintenance, Degraded Performance, Partial Outage, Major Outage. Page headline derives from all page components; incident impact derives from affected components, and can be overridden. Neither is the incident lifecycle state. | 2026-10-11 |
| [Notification event triggers](https://support.atlassian.com/statuspage/docs/notification-event-triggers/) | Send-notification choice overrides triggers. Real-time creation/resolution: Email, SMS, Webhook, Slack. Other real-time updates: Email, Webhook, Slack, no SMS. Component changes: Webhook and Slack only. Trigger eligibility does not certify delivery. | 2026-10-11 |
| [Add HTML tags in incident messages](https://support.atlassian.com/statuspage/docs/add-html-tags-in-incident-messages/) | Documented tags: a (href), b, big, em, i, small, tt, br, h1–h6, hr, img (src). Plain text avoids promising unsupported Markdown rendering. | 2026-10-11 |

## Applied evidence policy

Package rule of thumb: require supplied observations covering the affected scope before recommending full recovery. Atlassian supplies state meanings, not a fixed wait duration, prescribed probe count or particular recovery test. Preserve a user's separately supplied observation policy without attributing it to Atlassian. Choosing plain text and omitting external images are package drafting choices.

## When impact or the page headline is requested

Use only the complete relevant component set and any supplied override. Incident impact uses ordered conditions: all Operational → None; all Major Outage → Critical; all Partial Outage → Major; any Major Outage → Major; any Partial Outage → Minor; any Degraded Performance → Minor; otherwise any Under Maintenance → Maintenance. Conditions are applied in order. An absent/empty affected set is insufficient to apply this table.

For a single-component page, headline follows that component: Operational → All Systems Operational; Under Maintenance → Service Under Maintenance; Degraded Performance → Partially Degraded Service; Partial Outage → Partial System Outage; Major Outage → Major System Outage. For a page with no components, Atlassian documents All Systems Operational unless an incident is active; the article does not give the active-incident exception's exact headline calculation. Ask for active-incident context rather than infer an all-clear.

For two or more components, apply the first matching condition to the full page inventory: all Operational → All Systems Operational; all Major Outage → Major System Outage; all Partial Outage → Partial System Outage; any Major Outage → Partial System Outage; any Partial Outage → Minor Service Outage; all Degraded Performance → Degraded System Service; any Degraded Performance → Partially Degraded Service; otherwise any Under Maintenance → System Under Maintenance. The official multi-component rule says System Under Maintenance, while its single-component rule and headline list say Service Under Maintenance. Preserve that documented difference when explaining the rule; for exact display copy in a maintenance-only mixed case, ask for the supplied page display rather than silently harmonize it. Do not fetch the source at runtime.


## Decision examples

These are fictional component inventories, not customer observations. Apply the ordered impact conditions before considering maintenance:

| This incident's affected components | Calculated incident impact |
|---|---|
| API Partial Outage only | Major |
| API Partial Outage; Dashboard Operational | Minor |
| API Major Outage; Dashboard Operational | Major |
| Reports Degraded Performance; Exports Under Maintenance | Minor |
| Reports Operational; Exports Under Maintenance | Maintenance |
| Search Operational; Login belongs to a separate incident | None for Search |

A supplied impact override remains an override even when the component calculation gives a different default. Impact None does not certify cause elimination; Resolved still depends on the incident-state evidence. At 100 open incidents, creation is blocked by the documented limit; an existing incident's next update is a different operation.

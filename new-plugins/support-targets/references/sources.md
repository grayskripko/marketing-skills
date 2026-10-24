# Zendesk SLA source register

Read and verified accessible: **2026-10-11**. Planned submission: **2026-10-22**. These are public official documents read for this build, not a future-date verification. Publication/edit dates were not exposed in the web-reader content; earlier queue dates are not represented as independently reverified. Platform scope: Zendesk Support customer SLAs; group SLA separation where relevant. Reference summaries are paraphrases.

| Source | URL | Deciding material embedded |
|---|---|---|
| Using SLA policies | https://support.zendesk.com/hc/en-us/articles/5604663490458-Using-SLA-policies | Reporting section: instance rather than ticket aggregation; repeated next-reply and periodic-update outcomes. Views section: countdown is calendar time. |
| About SLA policies and how they work | https://support.zendesk.com/hc/en-us/articles/5600997516058-About-SLA-policies-and-how-they-work | Application section: default Priority, post-trigger first-match order, target changes, solving, merging and breach recorded at update rather than backdated. Group/customer policies can coexist. |
| Customizing your SLAs with advanced settings | https://support.zendesk.com/hc/en-us/articles/7412192349466-Customizing-your-SLAs-with-advanced-settings | Per-policy additive start/fulfillment options, requester and actor eligibility, next-reply dependencies, subsequent-update effect, historical comparison changes. |
| Defining SLA policies | https://support.zendesk.com/hc/en-us/articles/4408829459866-Defining-SLA-policies | Seven-metric definitions and reopening section. Minimum configured target: 15 seconds. Status-based resolution clocks differ from comment-based reply/update clocks. |
| Setting your schedule with business hours and holidays | https://support.zendesk.com/hc/en-us/articles/4408842938522-Setting-your-schedule-with-business-hours-and-holidays | Schedule timezone and ticket assignment; holidays excluded from business time. Default schedule is first in multi-schedule list; triggers can assign alternatives. UI intervals minimum 1 hour, 15-minute adjustments, midnight split; holidays are whole days. These UI limits do not define API flexibility. |
| Ticket Metric Events API | https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_metric_events/ | JSON fields, target minutes, business/calendar status, instance identity, deleted-event handling. Incremental cursor pages contain at most 100 records; ticket endpoint groups by metric/instance rather than globally chronological order. Missing pages can hide earlier application history. |
| Ticket metric event types reference | https://developer.zendesk.com/documentation/ticketing/reference-guides/ticket-metric-event-types-reference/ | Activation can resume; fulfillment does not prove achievement. Application events identify measurement/changes. Event timestamp alone does not establish elapsed clock. |
| Explore recipe: Reviewing SLA performance | https://support.zendesk.com/hc/en-us/articles/4408835960602-Explore-recipe-Reviewing-SLA-performance | Uses Support – SLAs dataset, SLA Tickets metric and SLA metric filter. Its ticket-based chart is not interchangeable with an instance-achievement denominator. |

## Source conflicts that change decisions

The overview enumerates six customer metrics; the defining-policy article enumerates seven and includes **Pausable update**. Use the detailed metric definition for that clock and preserve the supplied report metric label.

The defining-policy article's standard agent-created public-comment example says no first-reply achievement is recorded. The advanced-settings article adds public-creation activation for end-user requesters. The defining-policy article's light-agent internal-note example also differs from the advanced page's selectable options. Historical boxes, actor roles and actual application/activation events decide the case; missing evidence leaves that activation unresolved.

The event-types reference describes breach records as generated before breach and says `deleted` is always false. The API schema separately instructs consumers to ignore `deleted=true`. Preserve this conflict: honor explicit deletion flags in supplied records, compare breach time with as-of time, and do not infer coverage or realized breaches from future-dated rows.

## Reconciliation conventions

These are analysis conventions, not Zendesk product guarantees: deduplicate by event ID while flagging conflicts; keep raw instance identity plus policy transitions; label reconstructed deadlines separately; show a defined reconciled subset when report filters are absent; mark unknown historical settings rather than applying current defaults. No invented mapping of native reply-time measures to SLA achievements.

Before submission, reopen these exact URLs and check for changed definitions or options; update the actual read date and any affected instructions. No end-user answer needs this maintenance date.

## Fix verification — read 2026-10-11

Reopened the defining-policy, advanced-settings, policy-application and reporting pages above. Deciding sections: Pausable update (initial public comment must be submitted in New/Open/On-hold; same-event Pending does not establish the initial clock), First reply activation/fulfillment (creating self-requester cannot fulfill), Next reply activation/fulfillment (light-agent prerequisites and nonrequester fulfillment). These rules are now inline in the ledger. The final All/Any uncertainty rule is Boolean reconstruction, not an additional platform guarantee.

[Turning on reply time SLAs for live chat](https://support.zendesk.com/hc/en-us/articles/6670155267994-Turning-on-reply-time-SLAs-for-live-chat), read 2026-10-11: live-chat reply measurement has a channel-specific enabling setting; the defining-policy page distinguishes it from public-comment behavior. This revision explicitly excludes live-chat and messaging reply-event reconciliation rather than expanding comment eligibility without channel evidence.

The pausable same-event paragraph ends with ambiguous application wording. Do not infer a historical activation from that sentence alone; use the qualifying start boundary and supplied application/activation records.

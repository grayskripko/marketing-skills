# Official Intercom SLA knowledge register

All six articles loaded through live read-only web retrieval on 2026-10-11. These are Intercom Help sources, not SDK assumptions. Exact dates below are visible article labels, not inferred from crawl dates. Relative labels remain relative. Use these dates for upkeep, not in routine user answers. Reopen the sources near the intended 2026-10-21 submission.

## S1 — Application, replacement and target lifecycle

URL: https://www.intercom.com/help/en/articles/6546152-set-slas-for-conversations-and-tickets
Title: Set SLAs for conversations and tickets. Article date: 2026-07-30. Read 2026-10-11. Loaded current article text.

Relevant sections: Phone SLAs (Speed of Answer); How to remove an SLA; How to configure SLA targets; How to pause an SLA; Overriding SLAs when converting conversations to tickets; FAQs.

- Only one active SLA per conversation; another workflow can replace it. A linked back-office ticket may have its own parallel SLA.
- The relevant last customer interaction supplies response start time, which may precede workflow application. A later customer message does not replace the selected trigger message automatically.
- A different SLA restarts response timers from the applicable recent customer message. Reapplying the same SLA retains elapsed time. If a teammate already replied, first reply does not start and next reply waits for the next customer response.
- Replacement resumes TTC; ticket replacement resumes TTR. Conversion introduces ticket TTR while continuing closure timing from original conversation history.
- Chat conversations support FRT/NRT/TTC; customer tickets also support TTR. Back-office/tracker tickets support TTC/TTR, without customer-response targets.
- Close and resolve are distinct. Reopening resumes the relevant clock. Closing a linked conversation does not resolve its ticket.
- Enabled snooze and waiting pauses combine: neither state may remain when resuming. Custom states use the waiting category. Teammate replies while waiting leave the pause until customer reply.
- Pausing/deleting the workflow stops new applications; existing matched conversations keep their SLA. Edits affect new conversations. Removing existing targets and editing archived SLAs are not supported in this version.
- Manual Remove SLA is supported from the conversation menu. This differs from removing an existing target from an SLA definition, which remains unsupported. Phone Speed of Answer runs from call connection to teammate answer; this package separates that channel from chat/ticket clocks.
- Fixed means missed then completed, including completion after replacement.

## S2 — Clock arithmetic, holidays and pause overlap

URL: https://www.intercom.com/help/en/articles/9263617-slas-and-office-hours
Title: SLAs and office hours. Article date: 2026-07-30. Read 2026-10-11. Loaded current article text.

Relevant sections: Examples → final schedule-change paragraph; Impact of office hours on SLAs; Default office hours settings; Holiday Office Hours; How SLA pauses affect breach calculations.

Only active, in-office time counts. Out-of-hours messages defer eligible time; unfinished work carries into the next working period. Holiday hours override default availability. A 24-hour duration consumes three eight-hour working days. Pause/out-of-hours overlap is excluded once, not subtracted twice. Keep an observed breach time separate from reconstruction when settings or event coverage differ.

Adding a previously excluded day leaves existing due times intact unless the SLA is reapplied or overridden. New tickets use the updated availability immediately. Preserve stored due times and use historical schedules for old targets; current availability alone cannot establish their breach.

Source inconsistency: the pause section says pauses do not extend the breach deadline, then says reported breach time adjusts for pauses. Interpret the counting rule rather than adding a pause duration blindly to a displayed deadline. Scenario 3 says Monday 15:00–17:00 contains one remaining hour; it contains two. Its four-hour target with Tuesday closed would reach Wednesday 11:00 under those stated hours, not 12:00. Do not copy this arithmetic error. Scenario 1's rounded inbox display is not an exact deadline.

## S3 — Dataset fields and metric definitions

URL: https://www.intercom.com/help/en/articles/7022438-reporting-metrics-attributes
Title: Reporting metrics & attributes. Visible update label: “Updated over a week ago”; no exact publication/update date established. Read 2026-10-11. Loaded current article text.

Relevant section: SLA dataset → Metrics and Attributes.

SLAs applied counts SLAs, not objects; hit/miss metrics are target counts. Most use SLA started at; SLAs missed also has an SLA missed at variant. Action ID identifies the related conversation action; SLA name, metric type, state and Conversation ID support reconciliation. Fixed remains missed despite eventual completion. SLA attributed to means assigned at evaluation; current assignment and anyone who replied are separate fields. Custom hit rate counts hit targets out of applied targets; the SLA report wording describes conversations meeting SLA. Preserve the actual chart configuration when comparing these definitions.

## S4 — Report template, repeat replies and filters

Canonical URL: https://www.intercom.com/help/en/articles/2672572-slas-reporting
Opened legacy URL: https://www.intercom.com/help/en/articles/2672572-slas-report
Title: SLAs reporting. Article date: 2026-05-27. Read 2026-10-11. Legacy URL redirects to canonical article; both resolve to current text.

Relevant sections: Phone SLAs in the report; Understand chart data; Get a high-level overview; Useful SLAs report filters.

The chart information panel exposes period, report filters, metric and metric-level filters. Conversation miss rate counts objects with breaches; conversations/tickets with SLA counts objects with at least one target. First response can hit/miss once per conversation; next response can include several hits and misses. SLA performance does not support company-attribute filtering. Custom reports use SLA metrics/attributes on Expert.

Phone Speed of Answer appears alongside chat/ticket metrics after the phone workflow applies an SLA. Segregate phone rows before computing the supported chat/ticket population.

Definition discrepancy: template article describes hit rate as hit SLAs / applied SLAs; the metrics article distinguishes template conversation wording from custom target wording. Require the chart's exact metric rather than selecting a denominator from its title.

## S5 — Reporting schedules do not control SLA clocks

URL: https://www.intercom.com/help/en/articles/8425113-how-to-use-office-hours-in-reporting
Title: How to use office hours in reporting. Visible update label: “Updated over 2 weeks ago”; no exact date established. Read 2026-10-11. Loaded current article text.

Relevant sections: Teammate schedules; Troubleshooting.

Per-teammate schedules affect reporting metrics only, not SLA timers. Headline conversation FRT retains workspace-default hours. Within-office duration variants can exclude replies with no eligible duration and export blanks; blanks are not automatically zeros. Count metrics have no Within office hours duration checkbox. Avoid applying ordinary response-time rules to SLA target clocks.

## S6 — Grain of the supplied rows

URL: https://www.intercom.com/help/en/articles/8825260-reporting-datasets
Title: Reporting datasets. Article date: 2026-07-22. Read 2026-10-11. Loaded current article text.

Relevant section: Available reporting datasets.

SLA dataset object is conversation/ticket action. Conversations and tickets datasets describe overall objects; conversation actions describe individual actions. A current object state is not an SLA event chronology. A final export cannot prove every prior applied target without suitable action records.

## Authored reconciliation conventions

The composite reconciliation key, union-of-intervals procedure, conditional outputs for missing settings and evidence-first ledger format are authored methods, not documented export primary-key guarantees. Calculate union intervals before summing. Distinct object rates require an explicit population mapping, particularly for linked tickets. Do not infer unknown outcomes from replacement or reclassify pending rows as hits.

## Fix verification — 2026-10-11

All six canonical sources reopened on this date. Application removal, phone scope, office-hours schedule changes and SLA field definitions were checked against their named sections. The historical schedule rule governs stored due times; generic business-time arithmetic alone does not decide that case.

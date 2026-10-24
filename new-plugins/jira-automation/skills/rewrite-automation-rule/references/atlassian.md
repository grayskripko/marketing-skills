# Jira Cloud automation reference notes

All pages below loaded successfully and were read 2026-10-11. These are current observations for Jira Cloud, not Jira Data Center. Documentation uses both rule/component and flow/step terminology. Recheck deciding constraints before submission or when the site's UI differs. Paraphrases below are not copied manuals.

## Limits
[Automation service limits](https://support.atlassian.com/cloud-automation/docs/automation-service-limits/)

Ordinary flow 65 steps, advanced flow 500, each flow group 65. Scheduled JQL retrieves at most 999 work items; Lookup uses only the first 100. Associated-item ceiling is 5,000 per execution; reaching it disables the flow. Rapid trigger chains stop at loop detection 10. Processing allowance is 60 minutes per 12 hours. Site concurrency is Free 5, Standard 10, Premium 20, Enterprise 30; highest plan wins across apps. One scheduled flow cannot overlap itself. `THROTTLED` and retrieval/processing details distinguish limits. Reducing schedule frequency, bounding retrieval, and splitting components address different causes; splitting does not remove aggregate load. The processing allowance is per flow; distributing work can help individual flows stay within it, but requires the relevant window history and preserves total work.

## Hidden structure
[Maximum number of 65 components](https://support.atlassian.com/jira/kb/automation-rule-message-youve-reached-the-maximum-number-of-65-components-allowed-per-rule/)

Cloud-only; page updated 2025-09-26, read 2026-10-11. The trigger is excluded. Its illustrated If block has six exported objects: outer container, condition block, three conditions and one action. The editor hides some structure. Inspect structural arrays, including child and condition nodes. Do not count every dictionary, deduplicate distinct nodes by ID, or remove container nodes to force an export under the cap. The page recommends multiple rules. Its 65-component discussion concerns ordinary structure; use the service page for the advanced-flow distinction. Structural traversal is an estimated method derived from the example, not a complete exported-schema specification. For an in-limit complete excerpt rejected by Save, preserve the draft, compare the rejected configuration, reproduce the discrepancy and escalate if it persists; do not invent an ID defect or remove required checks.

## Advanced flow eligibility and semantics
[Advanced automation steps](https://support.atlassian.com/cloud-automation/docs/advanced-automation-components/)

Premium and Enterprise only. Adding an advanced step wraps steps in a flow group. Branch with conditions selects only the first matching path in order, with up to three branches and optional fallback. Thus replacing independent conditions can change which actions execute. Advanced nesting allows two levels; loops cannot nest within loops. Do not confuse this with ordinary related-work-item branch restrictions.

## Audit evidence
[What is an automation audit log?](https://support.atlassian.com/cloud-automation/docs/what-is-the-automation-audit-log/)

Total time combines run time and processing time. Processing time is not displayed: calculate Total time minus the sum of expanded step run times, using matching units. Obtain timestamps and the relevant 12-hour execution history before attributing aggregate load. Total time differs from wall-clock elapsed time; do not add waits again if the calculated value already includes them. Waiting on web requests and delays contributes processing time. Parallel branch processing is added across branches: three branches at one minute each contribute 3 × 1 = 3 minutes despite one minute of elapsed time. Audit records are retained 90 days; missing older entries do not prove no execution.

## Branch context and ordering
[Branch automation flows](https://support.atlassian.com/cloud-automation/docs/branch-automation-rules-to-perform-actions-on-related-issues/)

`issue` refers to each related item within a branch; `triggerIssue` refers to the trigger item. Multi-item branches execute concurrently and cannot be used as an ordered pipeline. Their changes and variables cannot be assumed available to another branch or the main path. Ordinary branches cannot nest or use If/else. Use All created work items to target items created earlier; an unbranched comment after Create comments on the trigger item. Related-item branches across projects require multi-project/global scope and appropriate plan eligibility. Do not broaden a source-project rule merely to create a target-project item; check the actor’s target Browse/Create permissions and required fields.

## Field edits
[Advanced field editing using JSON](https://support.atlassian.com/cloud-automation/docs/advanced-field-editing-using-json/)

Prefer Choose fields to set when supported. Additional fields require a JSON object with `fields` or `update`. A field cannot appear in both. `fields` acts like set; `update` can add/remove multivalued entries. Duplicate custom field names need IDs. Valid JSON is distinct from runtime smart-value evaluation; check actor permissions and edit/create field metadata. Re-fetch can address stale work-item data, but cannot synchronize parallel branches.

## Export and import setup
[Import and export Jira automation flows](https://support.atlassian.com/cloud-automation/docs/import-and-export-jira-automation-rules/)

Global administrator required. System → Automation flows → More actions → Export flows downloads all global/project rules. Import file limit 5 MB; imported flows start disabled. IDs for fields, statuses and work-item types can need remapping across sites. Draft builder steps are safer than fabricating a runnable export from incomplete evidence.

## Design judgment

For actual diagnostic testing, the recommended diagnostic-copy procedure is: start disabled; replace all effect-producing actions with logs; constrain the trigger to the selected case; enable only that copy for the authorized test; inspect the audit and disable it again. Logged intent does not prove a removed action would succeed.
Partitioning by disjoint scope, adding explicit completion conditions, and checking duplicate notifications are design recommendations, not Atlassian guarantees. Preserve coverage and ordering when applying them. Exact proposed component totals depend on the actual exported structure and Jira validation.

For draft-only answers, supply the requested configuration and relevant expected outcomes; use the diagnostic procedure when execution testing is in scope. For one aggregate from bounded disjoint Lookup partitions, use sequential main-path lookups, capture each result before the next lookup, then assemble one final output. [Create variable](https://support.atlassian.com/cloud-automation/docs/jira-automation-actions/#Create-variable) stores rendered strings, so capture counts and rendered keys rather than treating a saved variable as an issue list.

For strict child-success then parent-confirmation ordering, capture `{{createdIssue.key}}` on the main path and keep the parent key as `{{triggerIssue.key}}`. Draft an explicit completion gate; a main-path action after a branch is insufficient. A synchronous [Send web request](https://support.atlassian.com/cloud-automation/docs/jira-automation-actions/#Send-web-request) design requires approved authentication and a verified success-response condition before confirmation. Missing authentication remains a prerequisite, not assumed actor access; do not execute it or request credentials.

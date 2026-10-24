# Independent reader review — 2026-10-11

Reviewed both complete skills, both reference files, both manifests, README, Privacy and Build Notes. Did not read test answer outputs. Overall: package clearly supports supplied-evidence analysis, has credible task separation, and avoids falsely promising account access. Two substantive wording fixes and one small clarity fix are recommended. The additional cohort and application-field guidance was reread before finalizing.

## Quote → reader problem → fix

1. **Medium — report reconciliation agent.** Quote: “A shared report link expires after 24 hours.” Reader problem: the linked [Troubleshoot a report](https://support.greenhouse.io/hc/en-us/articles/13710986142107-Troubleshoot-a-report) specifically says *emailed report URLs* are valid for 24 hours. Broadening this to every shared link could falsely diagnose an access problem. Fix: “An emailed report URL expires after 24 hours; an error within that window can indicate missing permissions.” Make the scope equally precise in the report reference table.

2. **Medium — recruiting operations reader / arithmetic instructions.** Quote, in both skills: “Do not mention … how arithmetic was performed.” Later: “For every derived number show formula and inputs.” Reader problem: conflicting instructions can suppress the denominators users need to audit a rate or produce excessive calculation exposition. Fix: remove “or how arithmetic was performed” from the suppression rule; retain compact formula/input reporting and suppress implementation/tool details instead.

3. **Resolved during review — report reconciliation agent.** The final addition now explicitly states that Candidate Quality by Source follows an application-date cohort and Number of Hires counts activity events. Its reference cites the official cohort/activity comparison. This resolves the initially missing explicit explanation of the common date-field mismatch. The added Application details / Source & referrer location is also supported by its linked official source.

4. **Low — agent reading attribution reference.** Quote: “This date replaces the older STYLE example date.” Reader problem: unexplained build-process terminology adds no evidence value and suggests an inaccessible dependency. Fix: remove that sentence; retain retrieval date, publisher date and scope.

## Reader outcomes

- **Agent selecting for missing sources:** PASS. Audit description directly covers missing sources and token disappearance; hosted, embedded and API mechanisms are distinct. The job token is distinguished from source token. Supplied mappings are required before labels are inferred.
- **Agent reconciling quality and hires:** PASS with fixes above. Explicitly separates reported progression quality from independently calculated hire rate and blocks unmatched cohort arithmetic. Current-year default is properly constrained by actual export date/filter evidence.
- **Recruiting operations user:** PASS with arithmetic wording fix. Table-first result shape, exception ledger and precise next check are useful. Missing values and observed evidence remain distinct from proposed corrections. No inferred account writes.
- **Directory visitor seeking prerequisites:** PASS. README states Greenhouse context, pasted text/CSV/XLSX inputs, no account/keys/setup, partial-input handling and sanitization. Manifests match the two analysis jobs and advertise Read/Interactive capabilities. Privacy matches local evidence analysis and limited documentation refresh.
- **Adjacent user wanting candidate sourcing:** PASS. Audit explicitly excludes generating applicants and quality skill excludes individual evaluation. No sourcing search or outreach capability is promised, although the broad product name makes explicit skill boundaries important.

## Factual and arithmetic verification

Expectations formed before checking: source-token transport must match board type; quality must describe progression rather than hire probability; default/permission/link claims must match the linked source's precise scope; worked formulas must reproduce the inputs.

- **PASS:** [Tracking a candidate's source](https://support.greenhouse.io/hc/en-us/articles/216902526-Tracking-a-candidate-s-source) supports final hosted URL / application-page token propagation and API `mapped_url_token`. [Job Board API](https://docs.greenhouse.io/job-board.html#submit-an-application) marks `mapped_url_token` optional and describes the incoming `gh_src` value. Missing attribution alone does not establish failed submission.
- **PASS:** [Tracking links overview](https://support.greenhouse.io/hc/en-us/articles/216904366-Tracking-links-overview) requires an existing unique source before link creation. [Add custom source](https://support.greenhouse.io/hc/en-us/articles/200721664-Add-custom-source) requires a sourcing strategy. The package appropriately avoids settling the apparent source-page strategy-editing conflict.
- **PASS:** [Candidate quality by source](https://support.greenhouse.io/hc/en-us/articles/203940929-Candidate-quality-by-source-report) supports pipeline distance, first-stage rejection 0%, reaching offer 100%, current-year Date applied default, stage/milestone controls and visualization narrowing. It does not supply an exact reconstruction formula for mixed pipelines; the package does not invent one.
- **PASS except wording scope:** Troubleshooting source supports migrated-candidate default exclusion, permission-limited job/candidate visibility and emailed URL expiry. “Shared” needs narrowing as finding 1 states.
- **PASS:** Worked rates 2/20 × 100 = 10% and 4/40 × 100 = 10%; hire count ratio 4/2 = 2. Undefined 0/0, explicit denominator grain, duplicate application preservation, and no unsupported quality averaging are appropriate arithmetic conventions, not undocumented Greenhouse behavior claims.
- **PASS:** Untrusted rows/URLs/payloads remain data; no secrets or record writes requested; tracking links are parsed without visiting them. Documentation refresh restrictions and host-retention statement are consistent across README, Privacy and skills.

## Five casual routing probes

| User phrase | Expected selection |
|---|---|
| “Our Greenhouse paid ads became Unknown. Can you check these links and rows?” | audit-source-attribution |
| “The token stays in our custom form's address bar, but Greenhouse has no source.” | audit-source-attribution; inspect submitted mapped_url_token evidence |
| “Is referral quality 70% saying seven out of ten get hired?” | interpret-source-quality |
| “These source totals disagree with hires, and some source blanks started after a careers redirect change.” | interpret-source-quality plus audit-source-attribution for the token-path evidence |
| “Find me twenty engineering candidates to approach on LinkedIn.” | Neither; adjacent candidate sourcing/outreach is outside this package |

Review artifact only; plugin files were not edited.

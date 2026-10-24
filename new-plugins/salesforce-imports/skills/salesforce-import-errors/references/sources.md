# Error source register

Read 2026-10-11. All sources opened successfully with article text. Publication dates below were displayed on the articles, not inferred from search snippets. Undated developer pages had no displayed publisher update date. These observations describe current public rules, not a verified org configuration.

| Official source and URL | Supporting detail and scope |
|---|---|
| [Use one of these records?](https://help.salesforce.com/s/articleView?id=Dataloader-Error-Message-Use-one-of-these-records&language=en_US&type=1) — published 2026-04-02 | Data Loader Insert can be blocked by an active duplicate/matching rule. Review rules in Setup and compare existing records with an administrator's visibility. |
| [Common Data Loader errors](https://help.salesforce.com/s/articleView?id=000384437&language=en_US&type=1) — published 2026-05-25 | Unique-field conflicts differ from duplicate detection. Cross-reference failures include visibility, deleted/missing IDs and record-type access; owner/lookup IDs must have the right type. Headers and number separators can cause format errors. The Update null mapping error is attributed to the enabled external-key Update setting looking for an External ID in CSV mapping; Salesforce prescribes unchecking it. This article does not specify complete version/API-mode support. |
| [Core API data types](https://developer.salesforce.com/docs/platform/api/guide/sforce-api-calls-concepts-core-data-objects.html) | `DUPLICATES_DETECTED` is duplicate detection; `DUPLICATE_EXTERNAL_ID` means multiple existing upsert matches; `DUPLICATE_VALUE` violates field uniqueness. |
| [Data Loader operations](https://help.salesforce.com/s/articleView?id=inserting_updating_or_deleting_data.htm&language=en_US&type=5) | Separate success/error CSVs; processing failure can coexist with successful rows. |
| [Missing update ID](https://help.salesforce.com/s/articleView?id=Id-not-specified-in-an-update-call&language=en_US&type=1) | Inspect absent or unmapped IDs and the operation's matching setup. Published 2023-07-24; older article still loads, interpreted alongside current operation docs. |
| [Configure Data Loader](https://help.salesforce.com/s/articleView?id=sf.configuring_the_data_loader.htm&language=en_US&type=5) — read 2026-10-11 | API modes are distinct; rendered settings table does not list the external-key Update option. Do not infer universal support, a complete mapping-only remedy, or version-specific impossibility of remapping. If the key is already mapped, distinguish the documented uncheck-and-ID fallback from the unconfirmed cause of that job’s error. |

## Editorial safeguards

Holding ambiguous identities, excluding known successes from retry files, avoiding rule bypass and separating observed error meaning from suspected causes are editorial rules of thumb. They are not Salesforce guarantees. A screenshot description or partial export cannot establish complete org state. Unknown errors require exact messages and relevant field settings, not invented defaults.

For unknown timeout outcomes, hold until authoritative job results or equivalent record evidence establishes whether the intended write committed. Use an admin-visible export when needed; check intended identity and field effects, and investigate hidden/multiple matches and unique-field conflicts when they affect retry safety. Current record presence alone does not attribute a write to the job. Preserve the requested upsert key for repaired failures unless reconciliation establishes a reason to change it.

# Independent reader review 2

Readers considered: an agent selecting a missing-source audit; an agent reconciling application and candidate report grain; a recruitment lead acting on results; a directory visitor deciding whether to install; an adjacent user trying to find candidates rather than audit their sources.

Expectation before review: each reader can choose the appropriate skill, preserve application/person distinctions, distinguish observed attribution from intended attribution, and act on a concise output without interpreting contradictory instructions. The adjacent candidate-sourcing reader should recognize the package is outside their task from its entry description.

Read: README, PRIVACY, both plugin manifests, both complete skills and both references. Did not read candidate answers or review 1. No package changes. The reader-alignment skill was read before the parent's clarification that independent reviewers should not load it; no other review's findings were used.

## Findings

1. **Contradictory arithmetic presentation rules**

Quote (both skills, Answer and data rules): “Do not mention ... how arithmetic was performed.” Then: “For every derived number show formula and inputs”.

Reader/task problem: the agent reporting computed hire rates cannot obey both. A short end-user answer may suppress needed denominators or become a calculation tutorial depending on which sentence it prioritizes. The worked report example itself displays calculations.

Fix: replace the first sentence with “Do not narrate internal workflow. Show the inputs and denominator beside derived rates.” Keep the later zero-denominator rule. This removes the contradiction without weakening verification.

Source: the two quoted instructions and the interpret-source-quality worked example are direct package evidence; no platform fact is needed.

2. **An attribution coverage metric lacks a definition**

Quote (audit-source-attribution, step 4): “If asked for rates, use attributed unique applications / all unique applications in the supplied cohort × 100, and keep unresolved attribution separate.”

Reader/task problem: a recruitment lead auditing Unknown applications can count a known entry token as “attributed”, even though the same skill says tokens do not establish persisted attribution. It is unclear whether “Unknown” is a nonblank recorded source that counts, or an unresolved application that does not. Those interpretations change the headline coverage rate.

Fix: “For recorded-source coverage, count distinct applications with an identified recorded source / all distinct applications in the supplied cohort × 100. Exclude blank and Unknown values from the numerator. Separately report applications with a mapped entry token but unresolved recorded attribution; do not count intended attribution as persisted attribution.” If another attribution-rate meaning is requested, label that numerator explicitly.

Source: attribution skill Deciding rules and Analysis conventions explicitly separate token evidence from persisted source. Greenhouse documents the transport requirement, not a package-defined coverage statistic: [Tracking a candidate’s source](https://support.greenhouse.io/hc/en-us/articles/216902526-Tracking-a-candidate-s-source). This finding concerns a missing analysis definition, not a claim that Greenhouse uses the proposed metric.

3. **Grain compatibility needs an explicit outcome check**

Quote (interpret-source-quality, step 3): “Calculate hire rate only from compatible counts: hires / candidates in that source's stated cohort × 100 (or hires / applications if that is the explicitly requested unit).”

Reader/task problem: an agent using an application-level denominator supplied by a user may treat the absence of an explicit request for an “application unit” as a reason to seek candidate counts. Conversely, the phrase “compatible counts” does not explain what to check if hires are application events while the denominator is distinct people across multiple jobs. Multiple applications by one person are specifically anticipated elsewhere in the package.

Fix: “Use the explicitly labeled cohort denominator supplied in the data: hires / distinct applications for application-level counts, or distinct hired candidates / distinct candidates for person-level counts. Verify both numerator and denominator use the same source assignment and population; if hire grain is unspecified or incompatible, report counts and leave the rate unresolved.”

Source: audit skill step 1 distinguishes application IDs from candidate IDs; quality skill step 1 requires preserving column meanings. [Candidate quality by source report](https://support.greenhouse.io/hc/en-us/articles/203940929-Candidate-quality-by-source-report) labels candidates by stage and total hires, but does not establish that an independently deduplicated person-level CSV denominator matches those hires. The fix is an analysis-grain rule, not an assertion about the report's undocumented internal aggregation.

4. **The adjacent candidate-sourcing reader lacks an explicit entrypoint exclusion**

Quote (README opening and manifest description): “Audit Greenhouse source attribution and report interpretation ...” The package is titled “Recruiting Sources”.

Reader/task problem: a directory visitor searching for places to find engineering candidates may interpret the broad title as candidate sourcing. The skill descriptions exclude generating applicants, but those exclusions appear after installation/selection, not in the package entrypoint. The opening does communicate the analytic scope, so this is a small routing improvement rather than a misleading functionality claim.

Fix: add one short sentence to README and the long description: “For auditing existing Greenhouse data; does not find or contact candidates.” Keep the title and existing input requirements. No extra workflow section is needed.

Source: the manifests advertise Interactive/Read capabilities, PRIVACY says no account access or connectors, and both skill descriptions exclude applicant generation/outreach. This is a selection clarity finding, not a factual correction.

## Material that needs no change

Token transport rules clearly distinguish hosted/embedded forms from API payloads. Unknown date filters are not silently filled from today's default. Sources and strategy totals are kept separate; quality is distinguished from hire rate and post-hire merit. Privacy and network boundaries consistently forbid sending candidate data or opening supplied tracking links. These are reader-relevant controls rather than filler.

# Greenhouse offer report sources

Verified/read 2026-10-11. Scope: Greenhouse Recruiting essential reports. Pages below loaded as official public support articles. Recheck before submission around 2026-10-20 and when applying rules to a changed report. These dates belong in evidence files, not routine user answers.

- [Offer activity report](https://support.greenhouse.io/hc/en-us/articles/204635925-Offer-activity-report), updated 2026-03-02. Per-job counts; acceptance = accepted/(accepted+rejected). Extended means sent through Greenhouse; outstanding means sent and unresolved. Defaults: authorized open jobs, current-year Activity date. Hiring team role uses job assignments, not candidate-profile recruiters/coordinators.
- [Offer details report](https://support.greenhouse.io/hc/en-us/articles/203940589-Offer-details-report), updated 2026-03-02. Includes pending approvals and distinct creation/sent/resolved dates. Application ID, requisition and opening are available. Filters include Offer created, offer history and migrated candidates. Authorized jobs only. Private-hired policy requires Can create and view private candidates / prospects to see accepted details (Site Admin permission or Job Admin stripe).
- [Which report should I use?](https://support.greenhouse.io/hc/en-us/articles/8837686136987-Which-report-should-I-use), updated 2026-01-30. Details uses offer-created date; Activity is labeled Offer date. It does not specify a per-column event-date mapping. Do not infer one.
- [Offer approval overview](https://support.greenhouse.io/hc/en-us/articles/360035625832-Offer-approval-overview), updated 2026-03-02. With approval enabled, newly created offers need approval before extension. Final approval enables sending; approval itself does not establish sending.

Both report articles list Core, Plus and Pro. Their report-access requirements differ:

- Activity: Site Admin can see private notes and salary info, manage offers, and approve jobs/offers. Job Admin can view/edit offers and approve/request approval on offers.
- Details: Site Admin can see private notes and salary info, manage offers, **request approvals**, and approve jobs/offers. Job Admin can view/edit offers and approve/request on offers.

The Details private-hired condition above adds Can create and view private candidates / prospects. Match the exporting user's authorized jobs and offer access before claiming completeness.

## Authored reconciliation methods

The following are analysis rules, not documented Greenhouse implementation: pool counts rather than average rates; label a zero denominator undefined; preserve raw rows; use stable offer/version identity when available; don't collapse solely by name or Application ID; reconstruct historical outstanding only with sent/resolution/version evidence and an explicit cutoff. Missing resolution alone is insufficient if status contradicts it. A complete detail cohort can differ from period activity without either report being wrong.

The official articles name history/migration controls but do not document full history row semantics, status vocabulary, timezone/boundary rules or error codes. Request relevant settings or dated records for a deciding ambiguity. Never attach an invented platform error meaning.

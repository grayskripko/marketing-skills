# GDPR Requests

Handle an EU GDPR subject access request: match supplied email and CRM records, review redactions, calculate the response deadline and draft the reply.
For EU controllers handling customer or staff access requests. Supply the request, receipt evidence, controller country, readable exports and search logs. No accounts, keys or paid APIs are required.

| Skill | Output |
|---|---|
| gdpr-record-map | Request-to-record map and specific missing searches |
| gdpr-disclosure-review | Field-level release/redaction proposals and faithful text extracts |
| gdpr-response-draft | Receipt-based deadline and response, extension or refusal draft |

Paste text or provide readable local CSV, JSON, email text or extracted document text. Include stable record pointers, verified aliases, repository coverage and actual disclosure decisions where available. Use pseudonyms for unrelated people and omit unnecessary identifiers. A request for the whole package can combine the three jobs.

The bundled dated references cover EDPB scope, identity, copies and conditional suspension; Article 15 response fields; targeted third-party review; and CJEU recipient/copy decisions. ICO material is kept as UK comparison, separate from EU calculations. An export alone does not establish that every system was searched. File redaction and attachment preparation require their own verification.

Network scope: none. Skills read only supplied text/files and bundled references. They do not search the web, fetch URLs, access email/CRM accounts or send a response. Official source links are citations for human inspection. Updated official text can be pasted for a changed rule or national restriction.

[Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Build evidence](BUILD-NOTES.md)

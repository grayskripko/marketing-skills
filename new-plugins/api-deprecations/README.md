# API Deprecations

Check API deprecation notices and retirement dates against response headers and supplied policy, or draft a retirement notice and migration guide from approved endpoint changes.
For API owners, developer relations teams and technical writers preparing lifecycle notices.
Needs pasted text or local exports of endpoint docs, headers and approved policy. No accounts, keys, installs or paid APIs are required.

| Skill | Input | Output |
|---|---|---|
| check-api-deprecation | Notice, response headers with request context, old/new endpoint docs and notice policy | Scope/date conflicts, policy timing and corrected passages |
| write-api-retirement | Approved affected resources, lifecycle dates and replacement details | Retirement notice and migration copy |

Ask “Do these retirement dates and headers agree?” or “Rewrite this deprecation announcement using the approved endpoint mapping.” Include method, path, version, environment, exceptions, timezone and when notice was actually published. Missing approved facts get a short marker in an otherwise useful draft.

The bundled references distinguish RFC 9745 structured Deprecation dates from RFC 8594 HTTP-date Sunset values. They include link-context rules, date syntax and a dated GitHub REST policy example. A provider's documented behavior is kept separate from protocol compliance. A calculated earliest permitted retirement date remains a proposal until approved.

## Data and network

Network scope: none. The skills read text in the conversation and local exports you select. Bundled official-source URLs are citations, not fetched pages. There are no connectors, endpoint calls, telemetry, background monitoring or account actions. The assistant may calculate dates and word counts locally with its available tools. Redact authorization headers, cookies, signed URLs, customer identifiers and internal hosts; keep the method, public path and lifecycle headers needed for the task.

## Files

[Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Build notes](BUILD-NOTES.md)

## Support

https://github.com/grayskripko/marketing-skills/issues

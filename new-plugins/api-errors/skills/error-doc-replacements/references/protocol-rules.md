# Official protocol source register

Verified/read 2026-10-11. Publication dates below are distinct from this read date. Each HTML source and its current IETF record loaded. These notes paraphrase deciding rules; they do not reproduce source examples. Current RFC records list the cited documents as standards-track documents rather than obsolete replacements. RFC 9457 explicitly replaces RFC 7807. Recheck records and applicable errata before the planned 2026-10-24 submission; future changes are not claimed as verified today.

## Problem Details — RFC 9457, published July 2023

- Text: https://www.rfc-editor.org/rfc/rfc9457.html
- Current record: https://datatracker.ietf.org/doc/rfc9457/
- RFC Editor record: https://www.rfc-editor.org/info/rfc9457
- Scope: HTTP problem representations, not every custom error format.
- §§3–3.1.5: JSON object and media type; base members are optional; wrong-typed values are ignored. Type is identity with about:blank default. Status is advisory but generators must match the HTTP code. Title is stable except localization; detail is occurrence-specific; instance identifies the occurrence. Relative references need a base.
- §§3.2, 4, 4.2.1, 5: unknown extensions are ignored; extension schema belongs to the problem definition. New definitions document type/title/status. about:blank carries status semantics. Avoid exposing internals. Type/instance references do not authorize fetching.
- Decisions: do not require all five fields; preserve identities and extension schemas; surface line/body mismatches without guessing their cause.

## HTTP semantics — RFC 9110, published June 2022

- Text: https://www.rfc-editor.org/rfc/rfc9110.html
- Current record: https://datatracker.ietf.org/doc/rfc9110/
- RFC Editor record: https://www.rfc-editor.org/info/rfc9110
- Scope: HTTP methods, headers and status semantics, not provider quotas.
- §9.2.2: automatic retries of non-idempotent requests require known idempotent semantics or evidence the original was not applied.
- §10.2.3: Retry-After is an HTTP-date or nonnegative integer seconds.
- §§15.5.2–15.5.6: 401 needs an authentication challenge; 403 is refusal; 404 can conceal existence; 405 needs Allow.
- §§15.5.10, 15.5.13, 15.5.16, 15.5.21: 409 is state conflict; 412 is failed precondition; 415 is unsupported format; 422 is unprocessable instructions in understood, syntactically valid content.
- §§15.6.1, 15.6.3–15.6.5: distinguish unexpected server condition, invalid gateway response, temporary unavailability, and upstream timeout. Retry-After on 503 is optional.
- Decisions: required headers are not invented method lists; retry timing is not replay safety.

## Additional status codes — RFC 6585, published April 2012

- Text: https://www.rfc-editor.org/rfc/rfc6585.html
- Current record: https://datatracker.ietf.org/doc/rfc6585/
- RFC Editor record: https://www.rfc-editor.org/info/rfc6585
- Scope: 428, 429, 431, 511; deployment of these statuses is optional.
- §3: 428 requires a conditional request; distinguish it from an already failed precondition.
- §4: 429 means too many requests; Retry-After is optional; identity, counting scope and quota are not standardized.
- §5: 431 means request headers are too large; shrinking them may permit resubmission.
- §6: 511 is network authentication, intended for intercepting proxies, not normal origin authentication.
- §§3–6: these responses must not be stored by caches.
- Decisions: never manufacture quota, rate-reset behavior or a mandatory Retry-After rule from 429 alone.

## OAuth Bearer errors — RFC 6750, published October 2012

- Text: https://www.rfc-editor.org/rfc/rfc6750.html
- Current record: https://datatracker.ietf.org/doc/rfc6750/
- RFC Editor record: https://www.rfc-editor.org/info/rfc6750
- Scope: protected-resource Bearer authentication; not token endpoint error responses. Apply §§3–3.1 here, not the document's historical TLS deployment advice.
- §3: use WWW-Authenticate for the protected-resource challenge; preserve required scope names only when supplied.
- §3.1: invalid_request normally maps to 400, invalid_token to 401, insufficient_scope to 403. No authentication information should not produce an invented error code. A client may obtain a new token and retry an invalid-token request; this does not define a provider refresh flow.
- Decisions: token rejection and insufficient scope need different recovery text; do not invent a refresh endpoint or specific token lifetime.

## IANA HTTP status registry — live registry

- URL: https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml
- Canonical redirect loaded: https://www.iana.org/assignments/http-status-codes
- Scope: registered names and specification pointers; verified 2026-10-11, no inferred publication date.
- Decision: use registered status names, including 422 Unprocessable Content. Registry names do not define product-specific error meanings, retry policy or billing consequences.

## Editorial decisions

The per-error documentation template, separation of observation/contract/proposal, and exact old/new replacement layout are this package's rules of thumb, not RFC requirements. A stricter supplied API contract may require fields or headers that an RFC leaves optional. Do not erase that distinction.

## Current updates and errata — checked 2026-10-11

- RFC 6750 is updated by RFC 8996 (March 2021), https://www.rfc-editor.org/rfc/rfc8996.html, and RFC 9700 (January 2025), https://www.rfc-editor.org/rfc/rfc9700.html. Both loaded. RFC 8996 retires TLS 1.0/1.1; this package does not repeat RFC 6750's historical TLS deployment advice. RFC 9700 §4.3.2 prohibits passing access tokens in URI query parameters: do not replace authentication-error text with a query-token workaround. These updates do not replace the protected-resource error meanings in RFC 6750 §3.1.
- RFC 9457 errata: https://www.rfc-editor.org/errata/rfc9457 (redirects to errata.rfc-editor.org). EID 7731 is Held for Document Update, making extension acceptance explicit in Appendix A; EID 8858 is Reported, concerning the schema title. Neither changes the core member rules. A reported proposal is not an adopted requirement.
- RFC 9110 errata: https://www.rfc-editor.org/errata/rfc9110. Read when the supplied case involves details beyond the selected sections; reported/rejected proposals do not silently replace normative text.
- RFC 6585 errata: https://www.rfc-editor.org/errata/rfc6585. EID 8181 is Reported, submitted 2024-11-19; it proposes changing the Updates reference from RFC 2616 to RFC 9110. It does not change the selected status-code rules. This reported proposal is not an adopted requirement.
- RFC 6750 errata: https://www.rfc-editor.org/errata/rfc6750. Reported token-response media-type and terminology proposals do not change this package's protected-resource error scope.

For source refresh, RFC Editor's errata subdomain is the same official publisher. Robots checks and public-only requests still apply.

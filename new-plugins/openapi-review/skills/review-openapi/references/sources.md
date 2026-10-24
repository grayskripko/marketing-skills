# OpenAPI field rules and diagnostic sources

Verified by opening each URL on 2026-10-11. Every retained source returned HTTP 200. The OpenAPI latest publication URL resolved to 3.2.1 on this date. Pin the contract's major/minor version; patch revisions clarify that feature set. Refresh the register when preparing a new release. These are source-backed technical rules; output grouping and minimal-patch preferences are editorial choices.

## OpenAPI 3.2.1

URL: https://spec.openapis.org/oas/v3.2.1.html
Latest check: https://spec.openapis.org/oas/latest.html
Published 2026-09-10; read 2026-10-11. Scope: OpenAPI 3.2 descriptions.

Deciding passages and locations:

- [OpenAPI Object](https://spec.openapis.org/oas/v3.2.1.html#openapi-object): root needs `openapi`, `info`, and one of `components`, `paths`, `webhooks`.
- [Parameter Object](https://spec.openapis.org/oas/v3.2.1.html#parameter-object): required path parameters; schema/content exclusivity; one content media type; querystring/content requirement and query/querystring exclusion.
- [Path Item Object](https://spec.openapis.org/oas/v3.2.1.html#path-item-object): additionalOperations excludes methods with fixed fields; inherited parameter identity/override rules.
- [Operation](https://spec.openapis.org/oas/v3.2.1.html#operation-object), [Response](https://spec.openapis.org/oas/v3.2.1.html#response-object): operationId is unique when present; responses and response description are optional. [Responses](https://spec.openapis.org/oas/v3.2.1.html#responses-object) requires entries when present; status keys are strings.
- [Media Type](https://spec.openapis.org/oas/v3.2.1.html#media-type-object): itemSchema applies per streaming item; whole-content schema may coexist.
- [Example](https://spec.openapis.org/oas/v3.2.1.html#example-object): dataValue excludes value; serializedValue excludes value/externalValue.
- [Discriminator](https://spec.openapis.org/oas/v3.2.1.html#discriminator-object): optional property requires defaultMapping.
- [Security Requirement](https://spec.openapis.org/oas/v3.2.1.html#security-requirement-object): URI scheme references permitted; component names take precedence.
- [Objects and Fields](https://spec.openapis.org/oas/v3.2.1.html#objects-and-fields): normative text takes precedence over informational JSON Schema.

## OpenAPI 3.1.2

URL: https://spec.openapis.org/oas/v3.1.2.html
Published 2025-09-19; read 2026-10-11. Scope: OpenAPI 3.1 descriptions; not 3.2 feature permission.

- [Root](https://spec.openapis.org/oas/v3.1.2.html#openapi-object): openapi/info required; paths optional. [OpenAPI Description](https://spec.openapis.org/oas/v3.1.2.html#openapi-description) requires at least one paths/components/webhooks field in the complete description. [Info](https://spec.openapis.org/oas/v3.1.2.html#info-object): title/version required.
- [Operation](https://spec.openapis.org/oas/v3.1.2.html#operation-object): operationId unique, case-sensitive and optional; responses optional. [Response](https://spec.openapis.org/oas/v3.1.2.html#response-object): description required.
- [Reference](https://spec.openapis.org/oas/v3.1.2.html#reference-object): summary/description siblings permitted; other properties ignored. [Schema](https://spec.openapis.org/oas/v3.1.2.html#schema-object): 2020-12 dialect, boolean schemas, arbitrary keywords; $ref schema siblings differ from Reference Objects. Root-schema $schema overrides the document dialect. Nullable is not a standard keyword enabling null.
- [Security](https://spec.openapis.org/oas/v3.1.2.html#security-requirement-object): alternatives versus cumulative schemes; anonymous empty entry; non-OAuth arrays may contain role names. [Operation](https://spec.openapis.org/oas/v3.1.2.html#operation-object): empty security array overrides inheritance.
- [Paths](https://spec.openapis.org/oas/v3.1.2.html#paths-object): template-name-only differences are identical paths; empty Path Items may omit parameters.

## OpenAPI 3.0.4

URL: https://spec.openapis.org/oas/v3.0.4.html
Published 2024-10-24; read 2026-10-11. Scope: OpenAPI 3.0 descriptions, including contracts declaring 3.0.3.

- [Root](https://spec.openapis.org/oas/v3.0.4.html#openapi-object), [Operation](https://spec.openapis.org/oas/v3.0.4.html#operation-object), [Response](https://spec.openapis.org/oas/v3.0.4.html#response-object): paths, operation responses and response description required respectively.
- [Schema](https://spec.openapis.org/oas/v3.0.4.html#schema-object): type is a string, not an array; array schemas require items. Nullable needs type in the same object; other constraints still apply. Const is not supported; enum with one value can preserve a constant constraint. Required readOnly/writeOnly properties apply to response/request respectively, and both flags cannot be true together.
- [Reference](https://spec.openapis.org/oas/v3.0.4.html#reference-object): siblings ignored.
- [Security](https://spec.openapis.org/oas/v3.0.4.html#security-requirement-object): non-OAuth/OpenID arrays must be empty.

## JSON Schema 2020-12 Core

URL: https://json-schema.org/draft/2020-12/json-schema-core
Document dated 2022-06-16; read 2026-10-11. Scope: 2020-12 Schema Objects and supplied standalone schemas using that dialect. The official draft identifier remains 2020-12; later document editing dates do not change the dialect name.

- Section 8.2.1 `$id` establishes schema resource identity/base URI. Section 8.2.3 `$ref` applies referenced schemas and does not prohibit adjacent keywords. `$dynamicRef` has dynamic resolution semantics; a cycle alone does not prove invalidity.
- Section 10.2.1: allOf applies every branch, anyOf needs at least one, oneOf exactly one. Section 10.3.2: additionalProperties is not a global property merge across allOf. Do not close schemas merely because a linter prefers it.
- Section 8.1.1: `$schema` identifies dialect at a resource root. Custom dialects require their supplied vocabulary and supported semantics.

## JSON Schema 2020-12 Validation

URL: https://json-schema.org/draft/2020-12/json-schema-validation
Document dated 2022-06-16; read 2026-10-11. Scope: 2020-12 assertions/annotations.

- Section 6.1.1: type permits a string or unique string array; null is a type. Sections 6.1.2–3: enum/const constrain values independently of type.
- Sections 6.2 and 6.5.3: minimum is inclusive; required checks presence rather than nullability.
- Section 7: format is annotation by default; assertion depends on vocabulary/tool support.
- Sections 9.2–4: default is annotation; it does not insert a missing value. ReadOnly/writeOnly are annotations interpreted in the consuming request/response context. Examples are annotations, not extra constraints.

## Redocly CLI current rule documentation

URLs opened/read 2026-10-11:

- https://redocly.com/docs/cli/rules/oas/no-unresolved-refs — HTTP 200, current table includes 3.2. The rule checks resolution of $ref. A misspelled target differs from a target file absent from the review input. Severity is configurable (`off`, `warn`, `error`), so a printed severity does not establish normative strength.
- https://redocly.com/docs/cli/rules/oas/operation-summary — HTTP 200, current table includes 3.2. The rule requires an operation summary; OpenAPI itself does not. Explain it as configured lint policy when that rule is supplied.

Redirect probes from shorter paths reached these canonical URLs. A legacy struct page redirected to CLI v1 and listed only through 3.1; it is excluded from current support claims. No tool-version support is inferred for a user's validator from these pages.

## Diagnostic interpretation

These are source-grounded interpretations, not a universal message catalog. Parse errors precede field checks. Unresolved-ref messages require the source base and target. “Expected string, got array” can mean a genuine 3.0 type error or older-tool handling of a valid 3.1/3.2 type array. “Missing description” is a 3.0/3.1 response rule, but not a 3.2 response rule. “OneOf failed” needs the instance and branch results; do not choose a repair from the message alone. An unprovided tool version/configuration stays unknown.

## Parameter serialization defaults

Read 2026-10-11: [3.2 Style Values](https://spec.openapis.org/oas/v3.2.1.html#style-values), [3.1 Style Values](https://spec.openapis.org/oas/v3.1.2.html#style-values), [3.0 Style Values](https://spec.openapis.org/oas/v3.0.4.html#style-values). For schema-based parameters, style defaults are form for query/cookie and simple for path/header. Explode defaults to true for form; 3.2 also gives the new cookie style a true default. Other styles default to false, but default values do not make undefined combinations defined. Content-based parameters use media-type serialization instead. Nested array/object deepObject serialization is not defined.

## Cookie constraint correction

Read 2026-10-11: [3.2 Parameter Object, schema serialization](https://spec.openapis.org/oas/v3.2.1.html#parameter-object), section 4.12.2.2, explicitly prohibits `explode: false` for `in: cookie` with both `form` and `cookie` styles. This is a prohibition, not merely the true default. Diagnose the `/explode` value. A boolean replacement preserves supplied repeated-cookie behavior; comma-separated server behavior needs a wire-format decision. Content-based parameters use media-type serialization. Scope this deciding OpenAPI rule to 3.2 rather than retrospectively imposing it on older contracts.

## Sequential content and serialized examples

Read 2026-10-12: [OpenAPI 3.2.1 Sequential Media Types](https://spec.openapis.org/oas/v3.2.1.html#sequential-media-types), sections 4.14.3.1–4.14.3.1.1: sequential content maps to an ordered array; `schema` applies to that complete array, while `itemSchema` applies to each item. A media-type `dataValue` represents the parsed sequence even for one item; a string schema does not describe its serialized NDJSON body. Both schema fields may coexist, but their constraints must fit these distinct instances.

Read 2026-10-12: [NDJSON specification 1.0.0, Serialization](https://github.com/ndjson/ndjson-spec#31-serialization), dated 2014-10-19: each JSON text is followed by LF (0x0A), optionally preceded by CR (0x0D). When exact serialized bytes must be preserved, report missing framing without silently changing those bytes.

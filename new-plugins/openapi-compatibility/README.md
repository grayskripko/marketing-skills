# OpenAPI Compatibility

Turn paired OpenAPI exports or an exported diff into a consumer-impact matrix and migration checklist.
For API owners and consumer teams preparing an upgrade. Needs old/new exports or a directional diff; consumer notes make exposure more specific. No account, key, installation or paid API is required.

## Skills

- **compare-api-versions**: identify changed request acceptance, response guarantees and client interfaces, with source locations and affected consumer behavior.
- **plan-api-migration**: turn those changes into ordered consumer actions, acceptance checks and release dependencies.

Paste YAML/JSON, attach readable exports, or provide an exported change report. Label the baseline and target. Include the OpenAPI version, any diff-tool version and overrides, and known consumers. Partial exports produce findings scoped to the supplied parts.

Ask: “Will old clients still work with these two exports?” or “What must our mobile team change before this API rollout?” Single-spec validation, SDK generation, release-note drafting and deployment belong to other workflows.

The package embeds dated official rules for directional changes, defaults, nullability, security alternatives and deprecation classifications.

## Data and network

Runtime network fetches: none. Analysis uses supplied text/files and bundled references. Remote `$ref` targets must be supplied as exports. No connectors, live API calls, telemetry, uploads or external storage. The assistant may read supplied local files and use local tools for parsing. See [PRIVACY.md](PRIVACY.md).

Version 0.1.0. MIT license. [Support](https://github.com/grayskripko/marketing-skills/issues).

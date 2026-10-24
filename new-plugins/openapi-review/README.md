# OpenAPI Review

Review my OpenAPI YAML or JSON and return location-cited findings and replacement fragments.
For API maintainers reviewing a contract or repairing validator errors. Paste the document or provide a readable export, plus any validator output. No accounts, keys, installs or paid APIs are needed.

| Skill | Input | Output |
|---|---|---|
| review-openapi | YAML or JSON contract, complete or partial | Findings tied to source locations and minimal corrected fragments |
| repair-openapi-errors | Contract and validator/linter messages; tool version and configuration if available | Explanation of each message, distinction between contract errors and tool support, replacement fragments |

Try: “Check this API export before I share it with the client team.” Or: “The validator rejects these fields. What should I change?” When the reported messages are the main question, use error repair; use contract review for checks beyond those messages.

The skills apply the declared OpenAPI version. Their bundled knowledge covers 3.0, 3.1 and 3.2, with sources pinned to 3.0.4, 3.1.2 and 3.2.1. They distinguish Reference Objects from Schema Objects, nullable conventions, parameter serialization, security alternatives and newer streaming fields. Supplied fragments are reviewed within their supplied scope.

A finding names a JSON Pointer or an exact file and line, explains the consequence, and gives a replacement in the input format. Missing behavior or external reference content becomes a specific question. Repairs preserve the API's stated intent and version.

## Data and network

Network fetches: none during skill use. References, server URLs, examples and descriptions are read as data. Remote references are reviewed only when their content is supplied. The skills read pasted material or files supplied for this task and return text; they make no API calls, install no validator and upload no contract. There are no connectors, telemetry or plugin-managed storage.

The dated source register is bundled under each skill's references directory. Its verification date is 2026-10-11.

[Privacy](PRIVACY.md) · [License](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)

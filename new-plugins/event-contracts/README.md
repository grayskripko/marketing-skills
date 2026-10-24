# Event Contracts

Check GA4 event names, tracking plans and sample payloads; return field corrections and an engineering handoff.
For analysts, engineers, and administrators preparing tracking changes. Paste a register, example payloads, and a Custom definitions export or quota counts. No account, keys, installs, or paid API are needed.

| Skill | Give it | Receive |
|---|---|---|
| event-preflight | Register, payloads, web/app and collection method; optional validation reply | Field correction table, corrected examples, engineering handoff |
| custom-definition-plan | Parameter register, Standard/360 tier, existing definitions by scope | Create/reuse/defer plan, quota arithmetic, administrator handoff |

A register can be a table, CSV, JSON, or plain text. Include event name, trigger, owner, parameter name, type, scope, and reporting need where available. For payload checks, include representative values and identify tag/SDK or Measurement Protocol collection. Missing property settings remain marked in the result.

Examples: “Check these Android event names and SDK error rows.” “We have 48 event definitions; which of these five fields can we register?” “Fix this payload and give engineering the exact before/after fields.”

## Data and network

Reads pasted material and local exports you select. Fetches only the public Google documentation URLs listed in each skill's references/sources.md on support.google.com, developers.google.com, and firebase.google.com to refresh deciding rules. Documentation redirects may be followed within those domains. User payloads, identifiers, and exports are never included in requests. It calls no Analytics collection endpoint, account API, or connector. No telemetry or plugin storage. Local counting tools can check JSON, lengths, and quota arithmetic.

Sources were checked on 2026-10-11. Refresh deciding rules when they affect a current implementation. The package contains instructions, reference notes, and an SVG icon.

MIT; see LICENSE. Support: https://github.com/grayskripko/marketing-skills/issues

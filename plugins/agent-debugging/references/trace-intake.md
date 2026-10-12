# Trace intake reused from tool-autopsy

Operational procedure adapted from tool-trace-diagnose and tool-replay-plan. Match requests and responses according to the identifiers and correlation semantics in the supplied export. Use run, server, worker and parent-span context where available to distinguish concurrent calls; these fields are not a mandatory all-fields-match contract. A nearby foreign result suggests possible misassociation, not proof that the agent consumed it. Do not join unrelated calls by display name or manufacture a sequential chain from concurrent timestamps. Keep original timestamps or line references. Label excerpts as excerpts. Use this procedure internally; return only the deciding events inline unless the user needs a timeline.

Compare definition, arguments, returned result and next action. Separate wrong tool choice, unavailable tool, invalid arguments, denial, transport failure, tool-reported failure and old/truncated results. An identical repeat alone does not explain its reason. A changed page or new evidence can justify another call.

Before reproduction inspect existing receipts. A timeout after dispatch leaves the effect uncertain. Start with deterministic and read-only checks, then documented no-send operations; an authorized write needs a known target and an outcome check. A plan is not a performed replay.

These are package operating choices, not protocol requirements. The core procedures are also present in each relevant SKILL.md.

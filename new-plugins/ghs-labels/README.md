# GHS Labels

Check a GHS chemical label against its SDS and approved hazard classification under the US OSHA Hazard Communication Standard (29 CFR 1910.1200). For chemical regulatory specialists and packaging reviewers at formulators, distributors and laboratory suppliers. Paste the label text or artwork, the approved classification and SDS sections 1 and 2; add container size and whether it ships. No account, API key, install or connection is needed.

## What it does

| Skill | Result |
|---|---|
| ghs-label-review | Element-by-element checklist of a label proof against the classification and SDS, with precedence errors and annotated corrections |
| ghs-label-elements | Draft label block (pictograms, signal word, hazard and precautionary statements, supplier block) from an approved classification |
| hazcom-label-route | The labeling path for a container: shipped, small container with outer package, bulk, workplace/secondary, or another federal law |

Try: "Check this label proof against our SDS section 2", "Which pictograms go on a label for flammable liquid 2 and acute toxicity inhalation 3?", "What label does a 2 mL ampoule in a kit need?", "Can we use NFPA diamonds on our in-house bottles?"

The skills carry OSHA's Appendix C label-element table, the signal-word and pictogram precedence rules, small-container limits (100 mL and 3 mL, with the feasibility condition), bulk, DOT-overlap and update rules, and the 2024 rule's compliance dates. Dated official sources are in [references/osha-hazcom-labels.md](references/osha-hazcom-labels.md).

## Limits

The approved classification is an input: the skills never classify a chemical, add or drop a hazard, or decide a classification from ingredient percentages. Missing classifications or unreadable artwork produce a list of what is missing, not a pass. Results support, but do not replace, the sign-off of the qualified regulatory or safety reviewer who approves the label for print and release; printed legibility is checked on a physical proof. Scope is US federal OSHA HazCom. DOT hazmat marking, EU CLP, pesticide, consumer-product and drug labels follow other rules and are named as out of scope when they come up.

## What this package runs and connects to

A skills-only package: Markdown instructions and reference text, JSON metadata, a license and a static SVG icon. No scripts, dependencies, hooks, MCP servers or background processes. Network scope during use: none. The skills fetch no URLs, run no searches and send no data anywhere; source links in the references are for human reading. The publisher receives no task data and runs no telemetry. Your assistant provider processes the conversation under its own settings.

[Sources](references/osha-hazcom-labels.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)

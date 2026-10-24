# DOE Designs

Build a design of experiments (DOE) run matrix from your factors, approved levels, responses, run budget and batch limits. For formulation chemists, materials scientists and process-development researchers planning bench experiments. Paste or export your factor list with the operating bounds your scientist has approved; no account, API key, software or installation is needed.

| Skill | Result |
|---|---|
| screening-design | Full or fractional factorial, Plackett-Burman or definitive screening run table with blocks, run order, centre points and aliases |
| response-surface-design | Central composite, Box-Behnken or mixture design with every star point and blend checked against approved bounds |
| design-alias-check | What an existing run sheet can estimate, what is aliased or confounded with blocks, and runs outside approved bounds |

Try "Set up a DOE for these 6 factors in 16 runs across two lots", "Central composite or Box-Behnken inside these limits?", "Design a coating formulation where resin, solvent and pigment add to 100%" or "What is confounded in this run sheet?".

## What it does and does not do

The skills use the conventions of the NIST/SEMATECH e-Handbook of Statistical Methods (chapter 5) and name the section a design choice rests on. Every actual setting is computed from your approved bounds; a factor without approved bounds gets coded levels only. No run is placed outside those bounds. When the run budget cannot estimate the effects you want, the answer says so instead of offering an under-sized design.

Use it to plan bench experiments before collecting results: choose a design, prepare a run sheet, or check aliases and model estimability.

## What this package runs and connects to

Skills-only: Markdown instructions and references, JSON platform metadata, an MIT license and a static SVG icon. No scripts, dependencies, hooks, MCP servers, connectors or background processes. The skills make no network requests: no web search, no URL fetching, no uploads, no telemetry. They work from text and files you supply. If your assistant can run code, it may use its own local tools to compute a random run order with a recorded seed; nothing is sent elsewhere by this package.

The publisher receives no task data. Your assistant provider processes the conversation under its own settings.

[Sources](references/sources.md) · [Design tables](references/design-tables.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)

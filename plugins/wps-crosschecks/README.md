# WPS Crosschecks

Check welding procedure specifications (WPS), procedure qualification records (PQR) and their lab test reports against each other under ASME Section IX, and check that every joint on a weld map points to a current WPS that covers it. For welding engineers, welding inspectors and QA document reviewers at pressure-equipment fabricators and inspection firms. You paste the WPS, PQR, test report or joint-list text into the request; no account or connector is needed.

| Skill | What you get |
|---|---|
| wps-pqr-crosscheck | The WPS fields the cited PQRs do not support, process by process, with each range rebuilt from the coupon values and heat input recomputed |
| pqr-test-reports | The places where a PQR and its lab reports disagree: specimen and coupon IDs, recomputed tensile stress, failure location, bend count, Charpy temperature and units |
| wps-joint-register | The joints that use a superseded, unknown or look-alike WPS number, or fall outside the WPS for material, thickness, PWHT or impact testing |

Try: "Does PQR 31 support this WPS?", "Check the PQR tensile numbers against the lab report", "Which joints on this weld map use an old WPS revision?".

## What it knows

The skills match document numbers and revisions across the records you paste, split combination procedures by process, and recheck the numbers that decide the answer. They carry the 2025 Section IX changes that most often affect a crosscheck: the wide-weave heat input variable QW-410.92 and its removal for overlay (Special Notice R25-1666, June 2026), the corrected list of P-Numbers exempt from the toughness variables (Special Notice R25-1674, June 2026), the QG-108 rule for moving an older PQR to the 2025 edition, the QW-407.2 80% time clarification, and the new P-Numbers 54 and 81. Each has a dated source in [references](references/official-sources.md). Your contract, construction code and licensed copy of Section IX decide.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. It works only on text you provide for the task, pasted or attached. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)

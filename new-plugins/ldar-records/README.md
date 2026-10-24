# LDAR Records

Reconcile LDAR records for valves under EPA NSPS subpart VVa: turn component, Method 21 monitoring, calibration, repair, delay-of-repair and remonitoring exports into a leak-by-leak chronology and a missing-evidence queue.
For LDAR data coordinators and environmental specialists at LDAR contractors, refineries and chemical plants.
Needs the records pasted or exported into the conversation (CSV, spreadsheet extracts or text from your LDAR database). No account, API key, connector or installation is required.

| Skill | Result |
|---|---|
| ldar-repair-timeline | Chronology per leaking valve against the 500 ppm leak definition, 5-day first attempt and 15-day repair deadline; late, open and unverified repairs |
| ldar-calibration-check | Day-by-day verdict on Method 21 calibration, drift, precision and response time, with the re-monitor list and its ppm band |
| ldar-delay-of-repair | Per-valve review of delay-of-repair grounds, signature, expected date, shutdowns and post-startup verification |
| ldar-monitoring-frequency | Monthly or quarterly status per valve, missed events, and percent leaking valves for skip periods |

Try "Which of these leaks are past the 15-day repair deadline?", "The end-of-day drift was minus 14 percent, what do we re-monitor?", "Review our delay of repair list before the semiannual report" or "Calculate percent leaking valves for Q2".

The rule profile is VVa valves in gas/vapor or light liquid service, including refinery units that apply VVa through subpart GGGa. You confirm applicability. A unit under subpart VVb, a Part 63 program, a consent decree, a state rule or a permit condition can set a different leak definition or deadline; the skills apply the stricter term you supply and never carry VVa numbers onto another program. When records are missing, the skills say "Cannot conclude" and name the record that decides it. The skills give no repair, isolation or shutdown instructions and draft no regulatory filing.

Built on 40 CFR 60.480a–60.487a (subpart VVa, eCFR text current to 2026-10-08), 60.480b and 60.482-7b (VVb applicability and leak definition), 60.592a (GGGa), EPA Method 21 (40 CFR part 60, appendix A-7) and EPA's LDAR Best Practices Guide (2007).

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, a license and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

Network use: none. The skills make no web requests, searches, uploads or downloads, and send no telemetry. Supplied URLs are treated as text. Regulatory sources were read when the package was built and are embedded in the references file. The skills read only what you paste or attach for the task.

The publisher receives no task data and runs no collection or storage service. Your assistant provider processes conversation and attachments under its own settings. Remove personal data the records do not need; operator IDs are enough.

[Official sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)

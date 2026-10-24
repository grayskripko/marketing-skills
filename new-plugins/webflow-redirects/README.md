# Webflow Redirects

Check my old-to-new URL map and prepare the redirect CSV without losing existing rules.

Review supplied Webflow 301 maps for wildcard/path precedence, URL encoding and pattern escaping, chains, loops, and destination paths and domains. Check destinations against supplied information and preserve existing rules while preparing the CSV handoff.
For site owners and migration teams. Needs a pasted map, readable export, or screenshot description; a complete current export is needed to preserve every existing rule. No account or install is needed for preparation. Webflow access is needed for the export and eventual upload.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. This working folder also contains development reviews and test records; they are not runtime components.

The redirect-review and CSV-preparation workflows use only task text, attachments, local files that you explicitly supply, and bundled references. They do not browse, fetch supplied URLs or robots.txt, call APIs, log in, send messages, upload redirects, publish sites, or change account settings. They may use your assistant's existing local code/file tools to parse supplied CSVs, save the requested CSV, reparse it, compare retained and approved rows, and count serialized bytes. No packages are installed. If code is unavailable, CSV preparation returns copyable text and marks parsing and size unverified. Tool execution, temporary files, and requested outputs are managed by your assistant provider, not by a bundled program.

The skills guide you to perform Webflow exports, imports, recovery imports, publishing to selected domains, and browser checks yourself. Those actions connect to Webflow or the checked sites; importing replaces the redirect set and publishing may release other pending changes. Webflow provides export/error downloads through its UI and email; the assistant does not access your email or send it. Public documentation URLs identify sources, including an API reference that does not authorize an API call. Both source registers also say to reopen official guidance before a future submission: that release-maintenance check would retrieve the listed pages from help.webflow.com and developers.webflow.com, exposing ordinary request metadata to those sites and the browser/tool provider. It is separate from supplied-map processing and does not require transmitting the map. The GitHub support link is for user-initiated support, not an automatic connection.

The publisher receives no task data through this package and operates no collection, telemetry, or storage service for it. Your assistant provider processes and may retain your conversation, attachments, and tool outputs under its own terms. Requested output files remain at the chosen destination under its file-retention controls. See [PRIVACY.md](PRIVACY.md).

| Skill | Give it | Get back |
|---|---|---|
| check-redirect-map | proposed moves and any existing rules | row-level problems and proposed fixes |
| prepare-redirect-csv | current export plus approved moves | merged CSV, or an incomplete draft with the missing input named |

Try “Look over these URL moves” or “Merge these moves into our current redirects.” Use `prepare-redirect-csv` to review Webflow’s returned import-error CSV.

Existing rules are retained unless you explicitly approve a change. Unclear screenshot text is not guessed. Producing a file does not establish live redirect behavior.

The agent can guide you to export current rules, review the merged file, import it and inspect returned errors. Keep the original export as a backup. Choose the intended domains before publishing and check old URLs there afterward.

Sources and revision dates are in each skill's references. Recheck official guidance before a future release.

MIT. See [LICENSE](LICENSE). [Support](https://github.com/grayskripko/marketing-skills/issues).

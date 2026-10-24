# Plumbing Permits

Diagnose NYC DOB NOW plumbing filing objections from pasted work types, initial/subsequent filing status and intended combined permits.
For NYC plumbing contractors, filing representatives and design applicants. Needs pasted objection text, selected work types, displayed filing status and the intended permit arrangement. No account, connector, keys or installation beyond loading the plugin is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon, with development review/build records. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

The skills analyze task text and user-selected local files and read bundled source registers. They do not instruct code execution or software installation. They are not strictly offline: rule verification can use your assistant's existing web tools to retrieve public NYC DOB pages and PDFs listed in the source registers, official NYC updates, and `https://www.nyc.gov/robots.txt`. Public searches use rule titles without project details. The registers instruct reopening deciding sources before filing submission and, for filing diagnosis, when a supplied error contradicts the snapshot; later filing dates also require effective-rule verification. Website requests expose the requested URL and ordinary connection metadata to NYC and the tool provider; searches expose public rule-title queries to the search provider. Supplied project text, identifiers, credentials and private export links must not be sent in requests or searches.

The skills do not log into DOB NOW, look up properties, call account APIs, send messages, submit applications, or change DOB records. Filing, permit, withdrawal and reporting steps are recommendations for the user to perform. GitHub metadata and support links identify documentation or support pages, not automatic retrieval or sending instructions. If web retrieval is unavailable, supply the relevant official passage and its applicable date; an unverified deciding rule remains unresolved.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Input | Output |
| --- | --- | --- |
| diagnose-plumbing-filing | DOB NOW objection, PL/SP/SD/GC selections, I1/S status, contractors and permit intent | corrected arrangement, cause of each supported objection and next steps |
| check-limited-plumbing | scope, new/replacement work, quantities, building type and costs over 12 months | minor-repair/ordinary-work/LAA/full-plan route, reporting duties and deciding limits |

Ask: “Why can't I add PL to this GC filing?” or “Can these PL/SP selections use one permit with two contractors?” For an LAA check, paste the actual scope and relevant prior work; a low quote alone does not establish eligibility.

The skills distinguish combined filings, composite permits and subsequent filings. They recommend changes from supplied facts; they do not access or change DOB records. Official references include the DOB NOW Build FAQ, limited plumbing categories, owner requirements and LAA filing guides.

Sources checked 2026-10-11. Verify deciding rules for the application's filing date; retrieval dates and effective dates are recorded separately in references.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT license. See LICENSE.

# Airbnb Disclosures

Check Airbnb cameras and noise monitors, and fix their listing disclosures.
For home hosts and property managers. Needs pasted device details and listing text or local exports; no account, keys, installs or paid API is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The tests directory and build/review notes are development evidence, not runtime components.

The skills analyze task text and local exports that you explicitly supply. Pasted-material review uses the embedded policy rules without additional network requests. When current verification is requested or a rule has changed, the assistant may use its existing web tool to retrieve these public policy pages, or an official Airbnb policy URL you supply, and follow redirects:

- https://www.airbnb.com/help/article/3061
- https://www.airbnb.com/help/article/2914
- https://www.airbnb.com/help/article/3589
- https://news.airbnb.com/an-update-on-our-policy-on-security-cameras

Policy retrieval sends the requested URL and ordinary connection metadata to the contacted sites, including redirect destinations, and the assistant's tool provider. The skills prohibit uploading your inventory or listing text. If retrieval fails, the answer separates the supported draft from the unresolved current-policy question. The policy registers also request a publisher policy recheck before submission. GitHub metadata links identify documentation, source and support; they are not skill retrieval instructions.

The skills do not direct code execution, software installation, API calls, message delivery, account access or publishing. They return findings, replacement copy and instructions for you to make physical corrections and edit/save Airbnb safety fields yourself; those instructions do not perform the changes. They contain no instruction to write local files.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

- **audit-device-inventory:** get a device-by-device finding and physical or disclosure correction.
- **repair-device-disclosures:** get replacement listing copy and safety-field edits based on confirmed device facts.

Supply country, home/private-room category, host control, each device's placement and viewing area, video/audio capability, on/off state, sleeping uses of rooms, and current description and Guest safety fields. For Japan entryway cameras, include license and check-in arrangements. Missing details are marked beside the affected item.

Knowledge includes disconnected indoor cameras, exterior privacy areas, sofa-bed noise-monitor restrictions, camera location and operating-state fields, optional smart-device disclosure and Japan's entryway exception. These skills review home listings. A hotel needs its applicable hotel policy before a verdict.

Official sources were checked on 2026-10-11. Source details and dates: [policy references](skills/audit-device-inventory/references/policies.md). Build evidence: [BUILD-NOTES.md](BUILD-NOTES.md).

# Acuity Scheduling

Diagnose unavailable Acuity slots from appointment durations, padding, resources, availability and calendar/global booking limits. Check proposed availability changes against the same constraints. Distinguish booking blockers from hidden times, including empty classes holding resources and template display horizons.
For service businesses and staff who need to explain missing client-facing appointment times.
Needs pasted Acuity settings or supplied exports: appointment types, availability, bookings and limits. No account, keys or installation of a connector is needed for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. BUILD-NOTES.md and REVIEW.md are development records, not runtime components.

The skills analyze task text and files you explicitly supply and read their bundled source registers. They do not instruct code execution, software installation, API calls, account access, message delivery, or configuration writes. When a current rule needs verification, they instruct your assistant to fetch public documentation at `help.acuityscheduling.com` and follow help-article redirects using its existing retrieval tools. Both source registers also instruct re-opening relevant articles before relying on a different setting or submission date. This verification makes network requests: the requested help URL and ordinary connection metadata are disclosed to the help site, any help-article redirect destination, and the assistant's tool provider. Supplied settings and exports are not uploaded. Booking links and account endpoints are not fetched. GitHub publisher, repository, and support links are reference links, not retrieval instructions.

Account changes and scheduler checks are recommendations for the user to carry out, not actions performed by the skills. The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, and retrieval activity under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

- **diagnose-acuity-slots** explains why an existing requested time is absent and, when requested, identifies the smallest supported correction.
- **check-acuity-schedule-changes** checks proposed hours, padding, resources, booking limits or new candidate starts. It returns the requested fit result or before/after comparison.

Paste the requested date/time, calendar and appointment type; their time zones; duration and padding; regular and override hours; overlapping appointments, blocked time and synced busy events; resource assignments/quantities; calendar/group and global booking limits; start intervals; and the page template/link if relevant. Supply only fields relevant to your case. Use anonymous appointment labels instead of client identities. An appointment export alone may omit settings needed to decide why a time is hidden.

The skills analyze the supplied snapshot and produce recommendations. They do not access Acuity accounts or apply changes. Settings navigation is included in the source register. Review a proposed change against actual staff and equipment capacity, then compare the same appointment/date on the client scheduler after applying it.

[Privacy](PRIVACY.md) · [License](LICENSE)

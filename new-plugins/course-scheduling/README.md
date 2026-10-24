Find when Teachable course sections unlock and when their emails go out, in local time and UTC.
For course owners and operations teams. Provide pasted section settings or exports, first course enrollment dates, announcement settings and an IANA time zone such as Europe/London. No account, key, paid API or installation is needed for the pasted-input workflow.

# Course Scheduling

## What this package runs and connects to

This skills-only package contains Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. Development review and evaluation records are also present in this working folder; they are not runtime components.

These skills analyze pasted task text and local files you explicitly select. Both skills may use your assistant's existing code or local calculation tools, such as Python datetime/zoneinfo with available IANA time-zone data, to calculate dates and UTC/local offsets. This is host tool execution, not a bundled program. They do not fetch pages, search the web, call APIs, connect accounts, send email, or change course settings during calendar work. Dependencies must not be installed without a separate user request; such a request is outside the supplied-input workflow and needs its own installation and destination details. Calendar creation saves a local text/CSV file only when you request a destination; tool execution and temporary files are managed by your assistant provider.

The README tells the course owner to export a CSV through Teachable Reports > Leaderboards and copy Curriculum > section > Drip settings. Both skills recommend manual settings remedies and may propose an Emails > Compose fallback; the owner reviews and performs these account actions, including any custom email send. The assistant does not perform them.

The bundled source register instructs release maintainers to reopen four public Teachable help pages at support.teachable.com and Python's zoneinfo documentation at docs.python.org before submission. That maintenance step makes network requests and exposes requested URLs and ordinary connection metadata to those sites and the tool provider; it does not require sending course inputs. It is distinct from calendar work, where those URLs are citations and are not fetched. Repository and support links identify GitHub pages, not runtime connections.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, selected files, and tool activity under its own terms. Use student labels and omit unnecessary personal data and credentials. See [PRIVACY.md](PRIVACY.md).

| Skill | Ask for | Result |
|---|---|---|
| course-release-calendar | “When does each section unlock and when is its email?” | Per-section and per-enrollment UTC/local calendar, with email status and setup deadlines |
| course-drip-check | “Why does our drip spreadsheet disagree with Teachable?” | Corrected calendar and specific settings to review |

Paste section name, drip on/off, Specific date or Days after enrollment, the date or day count, announcement enabled state, subject, and save/activation times. For rolling enrollment, add the original course enrollment date or UTC timestamp and any full-access/restoration history. Use student labels rather than email addresses. For an existing plan, include the proposed times and the as-of timestamp.

To obtain enrollment inputs, open the course's Reports, choose Leaderboards and Export CSV. The UTC field is Enrollments Created At. Copy drip and announcement settings from Curriculum's section Drip panel. A Leaderboards export alone does not supply those settings.

The calendar keeps release and email as separate events, shows UTC offsets at each event and marks suppressed or unresolved emails. A restored schedule retains the initial enrollment anchor. Setup checks compare against release time; a filled subject is required.

## License and support

MIT; see [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues

# Analyze Google customer reviews and draft replies.

Analyze supplied Google customer reviews and draft business replies. Summarize themes, assess potential policy concerns and prepare neutral review requests. Also check Google Business Profile and website details against approved branch facts. Provide review text with branch IDs and source dates, plus approved business context or profile and website text. No login or paid API is required.

## What this package runs and connects to

The skills are Markdown instructions and reference text, with JSON platform metadata and a static SVG icon. Installing the plugin does not launch a program or connect an account. It defines no installer, dependency setup, hook, MCP or LSP server, or background process. Both platform manifests are metadata, not executable servers.

These skills work only from task text, attachments and local files you explicitly supply. They do not direct web search, URL or robots.txt retrieval, API calls, software installation, account access, message delivery, publishing or settings changes. Source and support URLs are references, not connection endpoints or retrieval instructions. Supplied review and business URLs may be copied into requested drafts; they are not fetched. Paste the relevant content when a link alone is insufficient.

This is not a strict no-execution workflow: the three profile skills permit a local counter to verify the final Google description's character count. That counter may use your assistant's existing local code or text tool on the draft description; no counter program is supplied. No installation or network request is directed for counting. Tool execution and temporary files are managed by your assistant provider. Without a counter, the skills keep drafts comfortably short and do not assert an unchecked exact count. The review-analysis skill requests calculations from supplied records but names no code tool.

The current source folder also contains development material: Python harnesses and generated evaluation records under `tests/`, plus `BUILD-NOTES.md` and `REVIEW.md`. These are not invoked by the skills or manifests. Manually running `tests/harness.py` launches the existing Codex CLI for model evaluations and writes prompts, answers, logs and result JSON to a historical `business-profile-check/tests` path. Its rerun scripts execute a helper from `/tmp/gbp-suite.py` and perform further evaluations and file writes. Model evaluations use the configured assistant provider and are not offline. Do not submit this development folder as a clean no-executable package; move development material outside the submitted folder first.

The publisher receives no task data through the skills and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and tool activity under its own terms. The skills return draft text and do not instruct file writes, sends or account changes.

| Skill | What you provide | What you get |
|---|---|---|
| analyze-google-reviews | Supplied reviews, branch IDs, dates and approved business context | Review themes, copyable reply drafts, potential policy concerns or neutral review requests |
| assemble-business-facts | Branch notes, approval messages and dated facts | One sheet of approved facts per branch; changes needing approval kept separate |
| check-profile-consistency | Approved facts and dated copies of profile or website text | Conflicting wording, sources and exact replacements |
| write-profile-corrections | Approved facts or a correction table backed by approved sources | Copyable field and website text for owner review |

Say “summarize these reviews,” “draft replies to these complaints,” “sort these branch details,” “which hours disagree?” or “give me the corrected description.” Paste the text or provide readable files. Keep branch IDs and dates visible. Screenshots need an assistant that can read images; paste text for unclear fields. If facts disagree, ask the owner which source to use.

A September screenshot does not prove what a profile shows today. Holiday hours stay separate from ordinary hours. A private home address stays out of public copy. Business names do not get added search keywords. Google Business Profile description drafts contain no URLs, HTML, promotions, prices or sales copy. They stay within Google’s description field limit; see the dated [Google field guidance](skills/assemble-business-facts/references/google-fields.md).

The skills fetch nothing, including supplied links. They read only the text and files you provide for the task. There is no telemetry, account connection, live monitoring, publishing, review reporting or profile editing. Review replies are drafts for owner review. Review analysis describes the supplied sample, not the full live review corpus. It does not provide a complete local SEO audit, confirm listing eligibility or predict rankings. Review proposed replacements before applying them.

The assistant provider processes your conversation under its own terms. Minimize customer details and private addresses before sharing. See [PRIVACY.md](PRIVACY.md). Host usage may cost money.

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).

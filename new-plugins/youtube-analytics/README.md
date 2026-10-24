# YouTube Analytics

Understand your YouTube Studio exports and choose one change to try on your next video using results that can be compared.

For creators and editors reviewing their own channel. Supply Studio CSVs, pasted tables or readable screenshots, plus your goal. Load this skills-only plugin into your assistant. No account connection, credentials, paid API or other install is required. Screenshot reading requires an assistant that can see images; otherwise paste the visible values as a table.

## What this package runs and connects to

The skills are Markdown instructions and reference text, with JSON platform metadata and a static SVG icon. Neither platform manifest declares an installer, hook, MCP or LSP server, or background process. Installing the skill instructions does not launch a program or connect an account.

These skills use only task text, attachments, readable screenshots and local files that you explicitly supply. They forbid web search, URL retrieval, account access, API calls and dependency downloads. URLs identify sources or support pages, not retrieval instructions or connection endpoints; supply the relevant content instead of a link alone. The skills do not direct message delivery, publishing, channel changes or source-file edits.

All three skills explicitly allow your assistant's existing local tools to read supplied files and calculate results. This can involve host code or spreadsheet execution; it is not a strict no-execution workflow. No specific command, interpreter, package installation or API is prescribed. Tool execution and temporary files are managed by your assistant provider. The skills return a table, finding or text experiment brief; they do not instruct output-file creation. A proposed creator experiment, including asking viewers for feedback, is advice for the creator, not an automated test or message sent by the assistant.

The publisher receives no task data through these skills and operates no collection, telemetry or storage service for them. Your assistant provider still processes and may retain your conversation, attachments and tool activity under its own terms.

### Development material in this folder

This working folder also contains historical evaluation records and two executable development scripts: `tests/round3-20261010/harness-original.py` and `tests/round3-20261010/harness-retest.py`. The skills and manifests do not invoke them. If manually run, they launch the installed Codex CLI, use the developer's existing Codex authentication, send test prompts and skill text to its model service, and write local test results and temporary files. They are not part of the supplied-data analytics workflow. Under the packaging guidance, move development scripts and evaluation records outside the submitted plugin folder before release; this working folder cannot be described as containing no executable code.

## What you get

| Skill | Your request | Result |
|---|---|---|
| `align-video-exports` | “These reports don't match.” | A table showing which video rows can be compared and which need a missing detail. |
| `read-channel-performance` | “Which videos worked?” | A short finding tied to your goal, with source rows and the math for calculated figures. |
| `plan-next-video-experiment` | “What should I try next?” | One practical change, videos and a time window to compare, and a rule for what to try after the result. |

Paste the data into your assistant, or provide local files it can read. Include upload dates, the dates each report covers, video formats and lengths, and results by traffic source where available. Keep Studio's metric labels. If a needed field is missing, the assistant uses the supported parts and names the gap after the result.

Shorts, long videos and live streams stay separate. Lifetime totals cannot reveal a video's first week. Click-through rate (CTR) uses views from counted thumbnail impressions, not total views. A before/after title change cannot prove what caused a performance change. The result describes what happened and proposes a test. It does not guarantee growth or claim an algorithm penalty.

## Access and privacy

The instructions fetch nothing: no web search, URLs, robots.txt, APIs, account reads or downloads. They read only supplied text, files and visible image data. Your assistant may calculate locally from supplied files; source files are not changed. There is no telemetry or plugin-operated storage. Your assistant provider's processing and retention terms apply. Remove personal viewer details before sharing. See [PRIVACY.md](PRIVACY.md).

This plugin prepares text. It does not run native tests, publish videos, edit channel settings, create media or summarize transcripts. A pasted export is a snapshot, not live monitoring.

License: [MIT](LICENSE). Issues: https://github.com/grayskripko/marketing-skills/issues

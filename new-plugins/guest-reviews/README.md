# Guest Reviews

Check whether an Airbnb review can be removed and draft a removal request from your evidence.
For Airbnb hosts, co-hosts, booking guests and property managers. Needs pasted reviews, messages, reservation facts and request-history records or selected readable exports. No account, keys, installs or paid API is needed for preparation.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable servers.

The skills analyze pasted reviews, messages, reservation facts, request history, and explicitly selected readable files or attachments. They do not instruct code execution or software installation. They return assessment and drafting text; they do not direct file writes or alter original evidence.

This package is not strictly offline. Both skills direct a policy refresh when you ask for current rules, before preparing a filing for a later date, or when supplied policy text conflicts. Using the assistant's existing web tool, they may fetch https://www.airbnb.com/help/article/2673, https://www.airbnb.com/help/article/3582, https://www.airbnb.com/help/article/546, https://www.airbnb.com/help/article/13 and https://www.airbnb.com/help/article/32, or an official Airbnb policy URL you supply, plus the site's robots.txt. They honor robots restrictions and follow redirects only within airbnb.com. These requests disclose the requested URLs and ordinary connection metadata to Airbnb and the assistant's tool provider, but must contain no review text, reservation identifiers or evidence. If retrieval fails, the skills continue from embedded rules, flag the affected policy question and request current official text before treating an unresolved allegation as filing-ready. Analysis using supplied material and embedded rules requires no additional network request.

The skills do not call application APIs, connect accounts, log in, open account pages, upload evidence, submit requests, send messages, publish replies or change settings. They explain user-performed Airbnb actions: filing through the removal form, finding a review by its words, and removing your own review through your profile. An eligible user performs those actions in Airbnb; the package prepares text only. GitHub metadata and support links identify documentation or support pages, not runtime retrieval instructions.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms.

| Skill | Ask | Result |
|---|---|---|
| assess-review-removal | “Can this review be removed?” | Clause-specific assessment, contrary evidence and request-eligibility check |
| draft-review-request | “Put my removal request together” | Supported draft, timeline and attachment index with gaps |

Check retaliation, pressure, relevance, authenticity, competition and content grounds. Separate removal merits from requester roles, pending requests and the two-submission limit. A rating disagreement or subjective criticism alone does not establish a removal ground.

Paste the complete relevant review and message context. Use aliases and omit sensitive identity, health, child and criminal-history information. Selected files must be readable; filenames alone do not establish evidence. To file, use the eligible person's Airbnb account and the review-removal form; this package prepares the assessment and text.

## Data and network

Execution, permitted public-policy requests, recipients and manual filing actions are described above. Use aliases and redacted evidence copies; keep original files intact.

Dated source sections: [policy references](skills/assess-review-removal/references/policies.md). Build and test records: [BUILD-NOTES.md](BUILD-NOTES.md), [tests](tests/RESULT.md).

MIT. See [LICENSE](LICENSE). [Privacy](PRIVACY.md). [Support](https://github.com/grayskripko/marketing-skills/issues).

# Check and edit your newsletter issue, subject line and preview text

Check and edit a newsletter issue, subject line and preview text using the sources and offer terms you supply.
For newsletter editors and publishers. Paste the draft, source excerpts and any approved sponsor or subscription terms. Voice samples and an audience brief are optional. No accounts, keys or paid APIs are required. This reviews newsletter copy, not campaign performance reports.

## What this package runs and connects to

The editorial workflow uses Markdown instructions and reference text, JSON platform metadata, and a static SVG icon. It provides no installer, dependencies, hooks, MCP or LSP server, or background process. The platform manifests describe the package; they do not launch a program or connect an account.

The skills use only task text, attachments, and local files you explicitly supply. All three skills permit your assistant's existing local counting tools to check words, characters, or arithmetic without uploading the material. This can involve host code or spreadsheet execution; it is not a strict no-execution workflow. Tool execution and temporary files are managed by your assistant provider. The skills do not instruct software installation, web search, URL or robots.txt retrieval, API calls, account connections, message delivery, publishing, or settings changes. Supplied URLs are copied or compared as text; paste the relevant content instead. Source and support URLs are references, not retrieval instructions.

The publisher operates no collection, telemetry, or storage service for this workflow and receives no task data through it. Your assistant provider still processes and may retain your conversation, attachments, and tool activity under its own terms. The skills return editorial text and do not direct file writes; any output file you explicitly request uses your assistant's existing file tools.


## What you get

| Skill | Give it | You get |
|---|---|---|
| fact-check-newsletter-claims | draft and supporting passages | corrected claims and the important differences from your sources |
| edit-newsletter-issue | issue, notes, audience and optional voice samples | edited issue that keeps qualifications, disclosures and offer conditions |
| write-subject-line-and-preview-text | final body and any field limits | subject/preview pairs that match the issue |

For a full edit with subject options, start with edit-newsletter-issue. For a few disputed claims, use fact-check-newsletter-claims. For subjects alone, use write-subject-line-and-preview-text.

## Examples

- “Check Copperleaf Dispatch against these shop survey notes. Replace claims the notes do not support.”
- “Edit Juniper Market Letter in a calm voice. Keep the conditional opening date and omit my private plans.”
- “Give Alder Workshop Notes two subject/preview pairs. The venue approval is still pending.”

## How it works

Corrections use your sources and separately approved facts. Quotes stay exact; attribution, uncertainty and exceptions stay with the claim. Voice samples guide style. They do not authorize new claims. If approved terms disagree, the conflict stays marked for your decision. The output is an editorial draft for publisher review.

## Data and network

The editorial skills direct no network requests. No URLs are fetched, including supplied links. Paste source excerpts or supply readable local files selected for the task. The assistant may use local tools to count words, characters or figures. No usage tracking, account connection, sending, publishing or drafts created in email tools. It does not test how an email looks, whether links work or whether mail reaches inboxes. It does not certify legal compliance or discover new facts.

The plugin has no service or storage of its own. Your assistant processes and may retain conversations and files under its own terms. Redact personal contact details and unnecessary subscriber data before sharing. See [PRIVACY.md](PRIVACY.md).

## If information is missing

With only a link, paste the issue or source text. If approved offer terms disagree, say which version to use. You get the edits that can be made from the supplied information first. Missing facts appear as `[DETAIL NEEDED: …]`.

## Support and license

[Issues](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).

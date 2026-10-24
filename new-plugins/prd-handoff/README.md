# PRD Handoff

Compare a PRD with stories and acceptance criteria, then propose the smallest fixes for missing requirements, contradictions and added scope.
For product managers and engineering reviewers. Supply a versioned PRD, story text or exports, and approved changes. Pasted text works without setup, accounts or paid APIs.

| Skill | Give it | You get |
|---|---|---|
| map-prd-to-stories | PRD, stories and criteria | Coverage table with source passages and unsupported additions |
| review-handoff-gaps | The same documents, optional design notes in text | Concrete differences, source passages and decisions needed |
| prepare-handoff-patch | Current text, approved sources and optional findings | Exact before/after proposals, whether sources are approved and decisions needed |

## Try it

- “Compare this approved PRD with our stories. What was dropped or added?”
- “Our permissions changed after review. Which criteria disagree?”
- “Give me the smallest ticket changes without adding scope.”

## Inputs and limits

Keep document versions, IDs, headings, approval status and exceptions. Supply readable text, Markdown or readable exports. For images and scans, paste the relevant text; this package does not provide OCR. If only one document is available, the assistant reviews it and asks for the document to compare it with. It does not infer that the newest version is approved.

The output is a proposal for product and engineering review. A coverage table does not prove the work is ready to build, correctly implemented, secure or compliant. No live tracker is read or edited; proposals can be copied by the document owner after review.

## Data and network

Network fetches: none, including user-supplied URLs. Paste the content instead. The package has no telemetry or separate service. No connector, account, paid API or credentials are required. The assistant reads only authorized task material. Redact customer details, contact information and secrets before sharing. The instruction package stores nothing itself; your AI host handles conversations and any saved outputs under its own terms. Files are created only when you request them.

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE). Data handling: [PRIVACY.md](PRIVACY.md).

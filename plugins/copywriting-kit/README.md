# Copywriting Editor Kit

## What it does

Editing and diagnosis workflows for your own website copy and drafts. Every edit comes with a change log, and every number, name and claim in your draft is locked so it cannot drift. Existing pages are diagnosed layer by layer before anything is rewritten. Claims are checked against the evidence you provide. Proof, testimonials and urgency are never invented: where proof is missing, the copy gets a visible `[PROOF NEEDED]` marker.

## Skills

Each skill is chosen by what you give it:

| You give | Skill |
|---|---|
| Your draft, plus "edit", "tighten" or "proofread" | `copy-edit`: fact-lock table, change log, clean text, before/after counts |
| An existing page (URL or pasted), plus "what's wrong?" | `copy-diagnose`: first broken layer, 12-point checklist score, top 5 changes |
| Copy plus your evidence (notes, data, reviews) | `copy-proof-check`: claims ledger with accurate rewrites |
| A brief, no page yet | `page-copy`: message brief, draft, three headlines, skim test, fact ledger |
| Samples of your own writing | `voice-profile`: tone rules, word lists, rhythm figures |

## Examples

- "Edit this, keep every number: 'Northwind Ledger is a revolutionary platform that empowers teams to cut invoice time by 40%.'"
- "Check against my notes: 'The leading invoicing tool, trusted by 10,000 teams.' Notes: 212 paying customers, no ranking data."
- "Diagnose before any rewrite: 'Reimagine finance. All-in-one for every business. Offer ends tonight! Get started | Book a demo'"
- "Write our pricing page from this brief." (then paste the brief)

## Sample output

One row of a change log:

| # | Before | After | Pass | Rule | Reason |
|---|---|---|---|---|---|
| 1 | "a revolutionary platform that empowers teams to cut" | "a platform that lets teams cut" | P5 | SP-06 | Praise words carry no information; the claim is unchanged |

## How it works

The edit runs eight fixed passes (meaning, reader, specifics, proof, stock phrasing, rhythm, voice, action) and logs each change with a rule id. The diagnosis checks positioning, then message priority, then wording, and names the first layer that fails. The proof check gives each claim a status relative to your evidence only. Counts are computed with the assistant's code tool when it has one, and labelled approximate otherwise.

## What it will not do

- Write ads, cold email, social posts or search titles.
- Invent proof, testimonials, deadlines or scarcity.
- Add typos or noise to text.
- Imitate a real person's voice.
- Give legal advice or legal clearance.

## Data and network

The plugin contains only instructions and reference text. It ships no code and stores nothing. Only the copy-diagnose skill fetches pages: public pages at URLs the user gives, at most 3 per run. No skill runs web searches or calls any other service. If the assistant has a code tool, it may use it to count words and patterns in the text you pasted; the plugin ships no code. Text you paste stays in your conversation with the assistant.

## Troubleshooting

- **Page fetch fails or looks empty:** paste the page text.
- **Counts look off:** they are approximate without a code tool; ask for a recount.
- **The edit changed too much:** ask for the change log only, then accept rows one by one.

## Support

Report problems and requests through GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).

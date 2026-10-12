# Copywriting Editor Kit

## What it does

Edit, diagnose and draft copy for your own website. Paste a draft and get the edited text back first, with change notes when requested or materially necessary; factual meaning and supplied terms are preserved, subject to requested cuts and privacy handling. Paste a page or give its URL and get the main problem in plain words and the top changes before anyone rewrites it. Claims are checked against the evidence you provide. Proof, testimonials and urgency are never invented: evidence checks identify missing support; ordinary edits and drafts flag only material unresolved issues.

## Skills

Each skill is chosen by what you give it:

| You give | Skill |
|---|---|
| Your marketing draft, plus "edit", "tighten" or "make it less generic" | `copy-edit`: requested edited text first; change notes when requested or materially necessary |
| An existing page (URL or pasted), plus "what's wrong?" | `copy-diagnose`: the requested messaging diagnosis and up to five relevant changes; optional scoring with stated applicability |
| Copy plus your evidence (notes, data, reviews) | `copy-proof-check`: evidence verdict and supported wording; a comparison when useful for multiple claims |
| A brief or product facts, no page yet | `page-copy`: requested page draft and material unresolved details; headline alternatives on request |
| Samples of your own writing | `brand-voice`: practical tone rules, examples, word guidance and qualitative rhythm; metrics and edits on request |

## Examples

- "Edit this, keep every number: 'Northwind Ledger is a revolutionary platform that empowers teams to cut invoice time by 40%.'"
- "Check against my notes: 'The leading invoicing tool, trusted by 10,000 teams.' Notes: 212 paying customers, no ranking data."
- "Diagnose before any rewrite: 'Reimagine finance. All-in-one for every business. Offer ends tonight! Get started | Book a demo'"
- "Write our pricing page from this brief." (then paste the brief)

## Sample output

**Your draft:** "Northwind Ledger is a revolutionary platform that empowers teams to cut invoice time by 40%."

**Edited:** "Northwind Ledger lets teams cut invoice time by 40%."

**What changed:** "a revolutionary platform that empowers teams to cut" → "lets teams cut". The praise words told the reader nothing. 40% is unchanged; it needs a source before you publish.

## How it works

Editing uses relevant checks for meaning, reader, specifics, proof, stock phrasing, rhythm, voice and action, with a final fact check. Change explanations are conditional. Diagnosis inspects relevant positioning, message-order and wording problems and prioritises their impact and dependencies. The proof check gives each claim a status relative to your evidence only. Counts are labelled approximate unless a code tool computed them.

## What it will not do

- Write ads, cold email, social posts or search titles.
- Proofread documents or policies for errors only.
- Invent proof, testimonials, deadlines or scarcity.
- Add typos or noise to text.
- Imitate a real person's voice.
- Give legal advice or legal clearance.

## Data and network

The plugin contains only instructions and reference text; it ships no code and stores nothing. Only the copy-diagnose skill fetches pages: public pages at URLs you give, in initial batches of up to 3, continuing through explicitly supplied URLs when needed for the requested comparison and permitted by available tools, and never a page the site's robots.txt disallows. No skill runs web searches or calls any other service. If the assistant has a code tool, it may use it to count words in the text you pasted. Text you paste stays in your conversation with the assistant. Names of private people in pasted reviews or notes are replaced with labels in the answer.

## Troubleshooting

- **Page fetch fails or looks empty:** paste the page text.
- **Counts look off:** they are approximate without a code tool; ask for a recount.
- **The edit changed too much:** ask for the full change log, then accept rows one by one.

## Support

Report problems and requests through GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).

# Copywriting Editor Kit

## What it does

Edit, diagnose and draft copy for your own website. Paste a draft and get the edited text back first, with a short list of what changed; every number, name and claim stays as you wrote it. Paste a page or give its URL and get the main problem in plain words and the top changes before anyone rewrites it. Claims are checked against the evidence you provide. Proof, testimonials and urgency are never invented: where proof is missing, the answer says what to collect.

## Skills

Each skill is chosen by what you give it:

| You give | Skill |
|---|---|
| Your marketing draft, plus "edit", "tighten" or "make it less generic" | `copy-edit`: the edited text first, then what changed; every fact kept |
| An existing page (URL or pasted), plus "what's wrong?" | `copy-diagnose`: the main problem in plain words, top 5 changes, a checklist score out of 24 |
| Copy plus your evidence (notes, data, reviews) | `copy-proof-check`: claims ledger with accurate rewrites |
| A brief or product facts, no page yet | `page-copy`: the page draft, three headline options, gaps to fill |
| Samples of your own writing | `voice-profile`: tone rules, word lists, rhythm targets |

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

The edit runs eight fixed passes (meaning, reader, specifics, proof, stock phrasing, rhythm, voice, action) and lists what it changed in plain words. The diagnosis checks positioning, then message order, then wording, and reports the first of these that fails. The proof check gives each claim a status relative to your evidence only. Counts are labelled approximate unless a code tool computed them.

## What it will not do

- Write ads, cold email, social posts or search titles.
- Proofread documents or policies for errors only.
- Invent proof, testimonials, deadlines or scarcity.
- Add typos or noise to text.
- Imitate a real person's voice.
- Give legal advice or legal clearance.

## Data and network

The plugin contains only instructions and reference text; it ships no code and stores nothing. Only the copy-diagnose skill fetches pages: public pages at URLs you give, at most 3 per run, and never a page the site's robots.txt disallows. No skill runs web searches or calls any other service. If the assistant has a code tool, it may use it to count words in the text you pasted. Text you paste stays in your conversation with the assistant. Names of private people in pasted reviews or notes are replaced with labels in the answer.

## Troubleshooting

- **Page fetch fails or looks empty:** paste the page text.
- **Counts look off:** they are approximate without a code tool; ask for a recount.
- **The edit changed too much:** ask for the full change log, then accept rows one by one.

## Support

Report problems and requests through GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).

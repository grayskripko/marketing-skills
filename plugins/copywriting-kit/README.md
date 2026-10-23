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
| A brief or product facts, no page yet | `landing-page-copy`: requested page draft and material unresolved details; headline alternatives on request |
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

The plugin contains only instructions and reference text; it ships no code and stores nothing. Network scope: two kinds of fetch, nothing else.
1. **Pages you link, in copy-diagnose.** Only public pages at URLs you give, in initial batches of up to 3, continuing through explicitly supplied URLs when needed for the requested comparison and permitted by available tools, and never a page the site's robots.txt disallows.
2. **The author's page at https://black-vector.com/copywriting/claims, only after you say yes.** Advice in four of the five skills (all but brand-voice) can rest on dated consumer-protection rules about claims, reviews, testimonials and endorsements (for example the FTC rule on fake reviews, the EU rules on environmental claims or the UK rules on fake reviews): drafting, editing or rewriting copy that states a claim, testimonial, review, rating or urgency line, flagging one as needing evidence, or answering whether copy can say something. The bundled copy is dated 2026-10-15 and may be out of date, so such an answer may end with a short note: the official page it relied on, its date, and an offer to check it against the plugin's changelog of these rules, https://black-vector.com/copywriting/claims, a page kept by the plugin author on a domain he owns. The official pages it names (for example the FTC at ftc.gov, eur-lex.europa.eu, legislation.gov.uk, the CMA at gov.uk or the ASA at asa.org.uk) are for you to open; the assistant does not fetch them. It fetches that page only if you say yes or ask for it, tells you what changed, and you decide whether to revise anything. If you never say yes, nothing is fetched.

No skill runs web searches or calls any other service. If the assistant has a code tool, it may use it to count words in the text you pasted. Text you paste stays in your conversation with the assistant. Names of private people in pasted reviews or notes are replaced with labels in the answer.

What the author's page at https://black-vector.com/copywriting/claims keeps: see the [privacy policy](PRIVACY.md).

## Troubleshooting

- **Page fetch fails or looks empty:** paste the page text.
- **Counts look off:** they are approximate without a code tool; ask for a recount.
- **The edit changed too much:** ask for the full change log, then accept rows one by one.

## Related plugins

Where this plugin stops and another one of mine continues:

- [CRO Checkout Audit and Test](https://github.com/grayskripko/marketing-skills/blob/squall/plugins/cro/README.md): A rewrite from copy-diagnose is only a hypothesis; CRO sizes the A/B test, judges the result, and checks the non-copy causes (forms, speed, tracking) the copy kit does not look at.
- [Marketing Psychology & Dark Pattern Check](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/marketing-psychology/README.md): The copy kit locks facts but does not check urgency, scarcity, 'was' prices or review claims against consumer-protection rules; persuasion-audit and dark-pattern-check do.
- [Copyedit & Proofreading](https://github.com/grayskripko/marketing-skills/blob/storm/plugins/copy-editing/README.md): after copy-edit, run a final errors-only proofread with a Ship or Hold verdict, and compare the approved and final versions before publishing.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko. I build AI agents and fix poorly working skills.

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).

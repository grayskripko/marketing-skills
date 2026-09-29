# Stock phrasing catalogue (SP-01 to SP-30)

Patterns that make copy longer, vaguer or less credible without telling the reader anything. The catalogue is grouped by what each pattern costs the reader. Each entry has a cue for spotting it and a fix. Examples use fictional companies.

How to use it:
- In an edit, log every removal with its SP id.
- Remove the pattern; do not replace it with another stock phrase.
- A pattern is a problem only when it carries no information. Check the false-positive note of each family before flagging.
- Correct grammar, a rich vocabulary and smooth reading are never signs of a problem.
- In the examples, every fact in an "after" version is assumed to come from the user's material. In a real edit, a fact that is not in the user's material becomes a `[DETAIL NEEDED: …]` marker instead.

## Family 1. Empty scaffolding (the reader waits for the point)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-01 | Announcement opener | Opens by announcing, being excited, or "introducing" | Start with what the product does | "We're excited to introduce Northwind Ledger" → "Northwind Ledger matches supplier invoices to purchase orders" |
| SP-02 | Stakes-setting opener or vision slogan | Opens with how fast the world or the market is changing, or puts a vision slogan where a statement belongs ("reimagine…", "the future of…", "next-generation", "for modern businesses") | Start with the reader's actual situation, or say what the product does | "In a rapidly shifting finance landscape…" → "Month-end close stalls when invoices wait for approval" |
| SP-03 | Signpost sentence | A sentence that says a point is coming, or that something is worth noting | Delete it and state the point | "It is worth noting that setup is quick." → "Setup takes one afternoon." |
| SP-04 | Summary closer | A last line that restates the page in softer words | Cut it, or end with the next step | "In short, Acme Invoicing makes billing easier." → "Start with one client's invoices this week." |
| SP-05 | Hopeful sign-off | A vague upbeat ending about the future or possibilities | Replace with a concrete next step or cut | "The possibilities are endless." → (cut) |

False positives: an opener that names the reader's specific situation is not scaffolding; a closing line with a real next step is not a summary closer.

## Family 2. Unearned emphasis (the reader stops believing)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-06 | Praise adjective | "revolutionary", "game-changing", "cutting-edge", "world-class" | Say what it does, or cut | "a revolutionary platform" → "a platform" |
| SP-07 | Unbacked superlative | "best", "#1", "fastest", "leading" with no source | Remove, or send to proof check | "the fastest AP tool" → "approves invoices in the same screen as the PO" `[PROOF NEEDED: speed comparison]` |
| SP-08 | Empowerment verb | "empower", "unlock", "supercharge", "elevate" | Use the plain verb for what happens | "empowers teams to cut invoice time" → "lets teams cut invoice time" |
| SP-09 | Intensifier stack | "truly", "incredibly", "seamlessly", "effortlessly" | Delete the intensifier; keep the fact | "seamlessly integrates" → "connects to" + the named system |
| SP-10 | Decorative bold | Bold on many phrases in one section | Bold at most one phrase per section, or none | — |

False positives: a superlative with a named source is a claim to check, not a stock phrase; "fast" with a number attached is a specific.

## Family 3. Padding shapes (the reader reads twice as much)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-11 | Reflexive triple | Three adjectives or three nouns where one carries the meaning | Keep the item that matters, or the real count | "fast, simple and powerful" → "approval in two clicks" |
| SP-12 | Synonym stack | Two or three words for one idea | Keep one | "clear and transparent pricing" → "published pricing" |
| SP-13 | Question echo | Restating the question or the heading before answering | Answer directly | "Wondering how pricing works? Here's how pricing works." → "Pricing is per approved invoice." |
| SP-14 | Restating paragraph | A paragraph that repeats an earlier one in new words | Cut it | — |
| SP-15 | List where prose would do | Bullets for two short connected ideas | Merge into one sentence | — (not for lists of features, steps or plan contents a reader scans) |

False positives: three real, distinct items belong in a list of three; repetition of a key term is clarity, not padding.

## Family 4. Hidden actor (the reader cannot tell who does what)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-16 | Actorless passive | "Invoices are matched" with no doer | Name who or what does it | "Invoices are matched" → "Northwind Ledger matches each invoice" |
| SP-17 | Abstract-noun chain | "optimization of the enablement of…" | Turn the nouns back into verbs | "streamlining of approval processes" → "approving invoices faster" |
| SP-18 | Company as subject everywhere | Most sentences start with "we" or the brand | Make the reader the subject where natural | "We provide reminders" → "You get a reminder before an invoice is due" |
| SP-19 | Vague association | "connected to", "related to", "plays a role in" without saying how | State the mechanism | "plays a key role in cash flow" → "shows which invoices are due this week" |

False positives: a passive is fine when the doer is unknown or irrelevant; "we" is right in an about page or a commitment ("we reply within one business day").

## Family 5. Manufactured tension (the reader feels handled)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-20 | Straw contrast | "It's not X. It's Y." when nobody claimed X | State Y | "It's not just software, it's a partner." → state what the service includes |
| SP-21 | Rhetorical question chain | Several questions in a row before any answer | Keep one question at most, then answer | — |
| SP-22 | Teaser heading | A heading that withholds the point to create suspense | Put the point in the heading | "The secret to faster close" → "Approve invoices from the PO screen" |
| SP-23 | Dropped analogy | A comparison introduced and never used again | Carry it through or cut it | — |

False positives: a real objection the reader holds can be named and answered; a question heading that the reader would actually ask is fine.

## Family 6. Template residue (the reader sees the machinery)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-24 | Unfilled token | `{{firstName}}`, `[Company]`, `<insert>` | Flag for the user; never guess the value | — |
| SP-25 | Assistant residue | "Here is your copy", "I hope this helps", notes to the writer | Delete | — |
| SP-26 | Emoji as heading marker | An emoji at the start of every heading | Remove unless the brand voice uses them | — |
| SP-27 | Uniform rhythm | Several sentences in a row of nearly equal length and shape | Vary length; follow a long sentence with a short one | — |

False positives: a placeholder the user asked for is not residue; emoji that the user's voice profile allows stay.

## Family 7. Hedge stacks (the reader cannot tell what is promised)

| id | Pattern | Cue | Fix | Example (before → after) |
|---|---|---|---|---|
| SP-28 | Qualifier pile | "may potentially help to some extent" | One honest qualifier, or a scoped fact | "may potentially help reduce errors" → "flags invoices whose amount differs from the PO" |
| SP-29 | Vague quantity | "many", "numerous", "a variety of" where a number exists | Use the number from the user's material or `[DETAIL NEEDED: count]` | "used by many teams" → "used by 212 teams" (from the brief) |
| SP-30 | Weasel attribution | "experts say", "studies show" with no source | Name the source or cut | "Studies show automation saves time" → `[PROOF NEEDED: source]` or cut |

False positives: a real uncertainty stated once is honest; "some customers" is fine when the user cannot share a count.

## Density for the diagnosis scorecard (DG-12)

Count SP-xx hits per 100 words of body copy. The bands below are a heuristic for this plugin, not a published standard:
- 0 to 1 hits per 100 words: score 2;
- more than 1 and up to 3: score 1;
- more than 3: score 0.

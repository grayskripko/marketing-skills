# Edit rules (passes P1 to P8)

Each pass has rule ids. Log every change with its pass and rule id. Run the passes in order; a later pass never undoes an earlier one without saying so in the log.

## P1 Meaning

- **P1.1** For each paragraph, name the reader question it answers ("what is it?", "will it work for me?", "how does it work?", "what does it cost?", "what do I do next?"). If it answers none, cut it or flag it.
- **P1.2** One idea per paragraph. Split a paragraph that carries two.
- **P1.3** The first sentence of a section carries the section's point. Move buried points up.

## P2 Reader

- **P2.1** Where natural, make the reader the subject: "You see every open invoice" rather than "We provide visibility".
- **P2.2** Describe the reader's situation in their terms, taken from the user's material. Mark it as assumed if the user gave none.
- **P2.3** Keep "we" where the company makes a commitment ("we reply within one business day").

## P3 Specifics

- **P3.1** Replace a vague phrase with a concrete fact from the user's material: a number, a named step, a named system.
- **P3.2** If no fact exists, insert `[DETAIL NEEDED: what is missing]` rather than making one up.
- **P3.3** Every promise gets one sentence on how it works (input, action, result), or `[DETAIL NEEDED: mechanism]`. A promise without a mechanism invites the objection "if this worked, everyone would do it".

## P4 Proof

- **P4.1** A number without a source stays as written and gets `[PROOF NEEDED: source for the number]`.
- **P4.2** A testimonial or quote without an identifiable source stays locked and gets `[PROOF NEEDED: customer name and permission]`.
- **P4.3** Superlatives and rankings from `claims.md` get `[PROOF NEEDED: …]` or are cut with the user's agreement; they are never strengthened.

## P5 Stock phrasing

- **P5.1** Remove patterns SP-01 to SP-30 from `stock-phrasing.md`. Log the SP id as the rule id.
- **P5.2** After removal, the sentence must say something specific. If it says nothing, cut the sentence.
- **P5.3** Do not replace a removed phrase with a different stock phrase.

## P6 Rhythm

- **P6.1** Vary sentence length. After a long, dense sentence, a short one lands the point.
- **P6.2** Do not reuse the same bridge phrase ("in practice", "here's the thing") within one page.
- **P6.3** Keep paragraphs short on the web: usually one to three sentences.

## P7 Voice

- **P7.1** If a voice profile is given, apply its tone rules, word lists and rhythm targets.
- **P7.2** If the profile conflicts with clarity or with a locked fact, keep the fact, and log the conflict for the user.
- **P7.3** With no profile, keep the draft's existing register; do not impose a new one.

## P8 Action and hygiene

- **P8.1** One primary call to action per page or section. Secondary links stay visually and verbally secondary.
- **P8.2** The call to action says what happens next: "Book a 20-minute walkthrough" rather than "Learn more". Use only facts from the user's material for details such as duration.
- **P8.3** Flag raw merge tokens (`{{firstName}}`, `[Company]`) and never fill them with guesses. Cut one only when the text type uses no greeting (for example a web page), and log the cut.
- **P8.4** Do not add deadlines, stock levels, discounts or "limited time" language. Existing ones stay locked and are flagged for proof check if no basis is given.
- **P8.5** Consistency: product names, capitalisation, number formats and terms are the same throughout.

# Bridge test, capture rule and form design

All rules on this page are heuristics of this plugin unless a register id is given. The user may override them, except the consent defaults, which come from the register. Print the step number that fired.

## Bridge test (applied before scoring)

Form: "Once the reader has used [asset], they hold [result]; [offer] delivers [that result] with less effort, repeatedly, or across a team."

- Passes (S5 = 2): "Once the reader has used the unbilled-hours calculator, they hold a monthly figure for hours worked but never invoiced; the invoicing product captures those hours automatically."
- Passes with one extra step (S5 = 1): "Once the reader has used the month-end checklist, they hold a clean close; the product runs most of the close steps for them." The reader must first see the steps as a burden.
- Fails: a payroll vendor offering a recipe e-book. Nothing the reader holds afterwards is something payroll software produces, so no honest sentence exists. Excluded, with the reason printed.

A sentence that needs words like "and then they will also want" to reach the offer, or that only works if the reader already wants the product, is a fail.

## Capture mode: ordered rule

Go through the steps in order. The first one that fires decides; print its number.

1. **Reach only.** The user wants search visibility, links, shares or citations and not contacts, or the asset teaches readers who are just noticing the problem. → **Open**, with an optional sign-up for updates next to it.
2. **A tool.** The asset computes or scores something on the reader's own input (calculator, scorecard, self-assessment). → **Use first, then save by email**: the result is shown on screen before any email is asked for.
3. **Contacts and reach together.** → **Summary open, full version by email** (summary, first section or one table open).
4. **Contacts only.** → **Full gate** only when all four conditions hold; otherwise summary open, full version by email.
   - (a) the substance is figures the company gathered itself, or a working instrument that does part of the reader's job, and neither is available at no cost elsewhere;
   - (b) a message after sign-up would be worth receiving for its own sake, not only a pitch;
   - (c) the reader is comparing or deciding, not just noticing the problem;
   - (d) a reader would plausibly pay a small sum for it.
   Print each condition as true, false or unknown; unknown counts as false. Print which condition failed when step 4 ends in "summary open".

Whatever the step, the consent defaults below still apply: a full gate for EU or UK individuals asks for an email to deliver the asset, never for marketing consent.

## Fields

| Rule | Why |
|---|---|
| Every field states one use before the next step: delivery, routing (which version to send), or the promised next step | data minimisation, GDPR Art 5(1)(c), register CR-05 |
| A field with no such use comes off the form, not made optional | same |
| Email only is the default | each extra field is one more reason to leave; no rate is claimed |
| Phone only when the next step is a call the reader asked for | same |
| Labels stay visible above the field; hint text is not the label | WCAG 2.2 SC 3.3.2; NN/g, Sherwin, 2014-05-11 |
| Optional fields say "optional" | NN/g, Whitenton, "Website Forms Usability: Top 10 Recommendations", 2016-05-01 |

## Consent defaults by region

| Readers | Default | Register |
|---|---|---|
| EU or UK individuals | Asset delivered whether or not marketing is ticked; one unticked optional box per stream; privacy notice linked beside the button | CR-01 to CR-05, CR-07 |
| UK corporate subscribers (companies, LLPs, public bodies) | Opt-out marketing allowed; identity and an opt-out address in every message. Sole traders and some partnerships count as individuals | CR-07, CR-08 |
| EU company addresses | ASK: member-state law decides | CR-06 |
| US | Opt-out model allowed if the user accepts it; CAN-SPAM duties on every commercial message | CR-09 |
| California | Notice at collection only if the company meets a CCPA threshold (ASK first); financial-incentive question goes to counsel | CR-10 |
| Elsewhere | ASK: which law applies | CR-11 |

## Draft box and notice text (the user's counsel has the last word)

- One stream: "☐ Also send me product news from [Company]. Optional; the [asset] arrives either way."
- Two streams: one unticked box each, e.g. "☐ Quarterly [report] update" and "☐ Product news".
- Next to the button: "We use your email to send the [asset]. [Company] is responsible for your data: [privacy notice link]."
- Never for EU or UK individuals: a pre-ticked box; one box covering several streams or sharing with others; "By downloading you agree to receive marketing"; "unsubscribe anytime" offered in place of a box; a download that only works after the marketing box is ticked.

The nearest EDPB text is its cookie-wall passage (paras 39 to 41, Example 6a in para 40): content held back until the person accepts leaves no genuine choice. That passage is about cookies, so it is cited as the closest analogue, not as a ruling on downloads.

## Worked example (gate-only mode)

A salary report built from the company's own anonymised data, which it may publish; readers in the EU and US; the user wants demos and also search visibility and citations.
- Step 1 does not fire (contacts are wanted too), step 2 does not fire (not a tool), step 3 fires: summary open, full tables by role and region by email.
- Fields: work email (delivery), job function (which table to send first). Company size removed: no use before the next step.
- EU: the report is sent whether or not either box is ticked. Two unticked boxes: quarterly salary update; product news.
- California: ASK whether the company meets a CCPA threshold before any notice or incentive question.

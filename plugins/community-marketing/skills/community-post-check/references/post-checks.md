# Post checks PC-01 to PC-13

Each check returns **Pass**, **Fail** or **Not checkable**, quotes the words of the draft it is judging, and names its rows from `rule-register.md` with their label. "Not checkable" always says what to supply. The statuses are a closed set, printed exactly as written, never with a qualifier such as "Pass if you follow the outline". Status judges the text actually supplied; with no draft, every check is Not checkable. Conditional advice goes in a separate "To pass" column (columns: Id, Status, Quoted words, Rules (label), To pass). If the answer depends on facts you do not have (for example the poster's history on the site), use Not checkable and say in "To pass" what to supply.

| Id | Question | Fails when | Rows (label) | Pass example | Fail example |
|---|---|---|---|---|---|
| PC-01 | Is the connection (employee, founder, contractor, agency, paid or gifted advocate, affiliate) stated in plain words in the opening sentence, before any claim about the product or the problem it solves? | No disclosure; disclosure after the first sentence or after a claim. Wording that also presents the poster as an outside user ("I found", "came across") fails PC-10 as well | US-255.5, US-255.5-Ex8 (guidance); EU-I-22 for staff, EU-A7-2 for advocates (law); UK-CAP2 2.3 (code); P-SE (platform, unverified). Opening sentence rather than anywhere clear: POL-FIRST (plugin policy) | "I work on the tool I'm about to mention." | "Found a great fix for this last week..." from the vendor's engineer |
| PC-02 | Is the disclosure inside the post itself? | Only in a profile, bio, signature, link preview or a cluster of hashtags | US-FAQ, US-D101, UK-ASA (guidance) | Disclosure in the first line of the message body | A reply that never names the employer, signed "Engineer at [COMPANY]" |
| PC-03 | Is the wording unambiguous in every market the post reaches? | "sp", "spon", "collab", "aff", a lone "thanks", "#ambassador" or "partner" alone, "gifted" alone, a discount code alone. For UK readers also "sponsored", "gifted by [brand]" and any ambassador tag, even brand-named | US-FAQ, US-D101, UK-ASA (guidance); POL-PLAIN (plugin policy). No disclosure at all: Not checkable here (PC-01 and PC-02 already fail) | "I'm a paid [BRAND] ambassador." | "#collab", or "#[Brand]Ambassador" as the only label for UK readers |
| PC-04 | Value without the link: does the post still help once the product sentence and link are deleted? | Nothing useful is left | plugin policy | Two concrete causes and fixes remain | Only "try [PRODUCT], link below" remains |
| PC-05 | At most one product mention and one link, and is the link needed for the answer? | More mentions, or a link that does not help answer | plugin policy; P-HN (not mainly for promotion) | One link to the docs page that answers the question | Links to pricing, docs and signup in one answer |
| PC-06 | No requests for votes, likes, stars or boosts, and no plan for colleagues or friends to engage on cue? | Any such request or plan | P-HN, P-PH, P-RDT2, P-DSC15, P-LI, P-GH (platform), whichever applies to the venue; POL-VOTE (plugin policy) for any venue, including one whose rules say nothing about votes. US-255.2d (guidance) only where reviews are voted on | No call to vote | "Upvote if it helps!" or "I'll post the link in our team chat so everyone can support it" |
| PC-07 | Does the post follow the venue's own rules, line by line? | A rule is broken. No rules supplied: Not checkable, "paste the rules or give the public rules page" | the venue's rules; P-RDT2 | Vendor post in the weekly thread the rules allow | Vendor post in the main feed where the rules forbid it |
| PC-08 | Are paid referral, affiliate or tracking links disclosed as paid? | A paid link without a disclosure | US-255.5 (guidance); UK-ASA (guidance) | "Referral link: I get a fee if you sign up" | A link with a referral code and no fee line |
| PC-09 | Is the text written for this venue rather than copied across several? | The same text prepared for several venues | P-RDT2, P-DSC13 (platform) | Text answers this thread's question | "I'll drop this same post in five groups today" |
| PC-10 | Is it posted by the person, from their own account, as themselves? | The poster is presented as someone they are not: another account, a persona, a company account where banned, posing as another person or organisation, or staff writing as an outside customer ("I found", "as a long-time user", "just switched to"). An undisclosed founder or employee writing as themselves ("we built", "we had this problem") fails PC-01 only, not PC-10 | EU-I-22 (law); US-465.5 for reviews (law); P-RDT5 (impersonation only), P-PH company accounts, P-DSC18, P-LI (platform) | Personal account, own name or usual handle, role stated | "As a long-time user..." written by staff |
| PC-11 | No rewards tied to votes, reviews or what a review says? | Any such reward | US-465.4 (law); UK-P13 when concealed (law, statute page unverified); P-PH (platform) | No incentive | "Leave five stars and we'll extend your trial" |
| PC-12 | No messages to members gathered from the community, and no bulk unsolicited messages? | Either is planned | P-DSC13, P-LI (platform); D-ICO (guidance) | Replies stay in the thread | "Then message everyone who commented" |
| PC-13 | Does the venue allow AI-written or AI-edited text? | Banned (P-HN-AI, or a pasted rule saying so): output becomes checks plus an outline. Unknown: outline only, with "check the venue's rules on AI text" | P-HN-AI (platform); the venue's rules; POL-AI (plugin policy) | Pasted rules allow assisted writing | Any Hacker News post or comment |

## Verdict logic

Print one of four verdicts with the check ids that decided it: **Verdict: Do not post (PC-01, PC-06)**. Apply the rules in order; the first match decides.

1. Any Fail on PC-01, PC-06, PC-10, PC-11 or PC-12: **Do not post** as drafted. PC-01 and PC-06 can be fixed (state the connection first; delete the ask) and checked again. For PC-10, PC-11 and PC-12 the plugin does not rework that version; it offers the disclosed alternative from `refusals.md`.
2. PC-07 Fail: **Do not post** in this place, or **Ask the moderators first** when the rules allow vendor posts with approval.
3. PC-07 Not checkable: the verdict is at best **Ask the moderators first**, and the output asks for the rules.
4. Fails only among PC-02, PC-03, PC-04, PC-05, PC-08 and PC-09: **Revise**.
5. No Fail, PC-01 and PC-07 Pass: **Post**. PC-13 never blocks a verdict; it decides only the form of the help below.

A Revise with PC-07 Not checkable becomes Ask the moderators first once the revision is done.

## What the user receives after the verdict

- PC-13 Pass (the venue allows assisted text) and the verdict is Revise or better: one revised version. Opening sentence = the disclosure; then the answer to the thread; the product sentence comes last, marked "[optional: delete if not needed]". No vote request, one link at most.
- PC-13 Fail or Not checkable: a numbered outline of at most five points, in order ("1. Open by saying you work on [PRODUCT]. 2. ..."), then "write it in your own words". No sentence the user could paste. A request to make it "sound human" for such a venue is declined with RF-9.
- A vote request is deleted, not reworded.
- PC-10, PC-11 or PC-12 failed: that version is not reworked. Print the refusal line from `refusals.md` first, for example "PC-10 failed, so this version is not reworked (RF-1: staff writing as an outside user; US-255.5-Ex8, EU-I-22).", then the disclosed alternative, as a revision or an outline under the PC-13 rule above.

## Stop rules (print with every verdict)

- Post removed: pause in that venue and ask the moderators what would be acceptable.
- Warning or ban: stop in that venue. Do not appeal through new posts.
- Never post again from another account or under another name (P-RDT2, P-DSC19).

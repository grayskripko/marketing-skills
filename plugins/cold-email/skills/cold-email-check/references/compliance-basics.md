# Compliance basics

Checks, not legal advice. Rules change; the user confirms what applies to their recipients. Every row here was read on 2026-09-30 (the United Kingdom row re-read on 2026-10-08); if today is more than 6 months later, the output says "These may have changed; check the current text." Read dates stay in this file and are not printed.

## United States: CAN-SPAM
Source: Federal Trade Commission, "CAN-SPAM Act: A Compliance Guide for Business", https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business (read 2026-09-30). Duties the check covers:

| Id | Duty |
|---|---|
| CO-01 | Header and routing information ("From", "To", "Reply-To", domain) is accurate and identifies the sender |
| CO-02 | The subject line reflects the content of the message |
| CO-03 | The message identifies itself as a commercial message where the law requires, clearly and conspicuously |
| CO-04 | The message includes the sender's valid physical postal address |
| CO-05 | The message explains clearly how to opt out of future email |
| CO-06 | Opt-out requests are honored within 10 business days, and the opt-out method works for at least 30 days after sending |
| CO-07 | The law makes no exception for business-to-business email |

The FTC guide also makes the sender responsible for anyone it hires to send on its behalf; if the user mentions an agency, add an ASK row.

## Known rules by country
Each row is the general rule as the law states it, read on the statute's own text on 2026-09-30, and what to check. Stated as "the law says … — confirm with counsel"; checks, not legal advice. Rows are ASK when the answer depends on facts only the user has.

| Country | General rule | Statute | What to check |
|---|---|---|---|
| Germany | Marketing email needs the recipient's prior express consent; business addresses are not exempt. A narrow exception covers existing customers who bought a product, for similar products, with a clear objection notice. | UWG § 7(2) no. 2 and § 7(3), https://www.gesetze-im-internet.de/uwg_2004/__7.html | Is there documented consent or an existing-customer relationship? If not, do not send cold. |
| Canada | A commercial electronic message needs express or implied consent and must identify the sender, give contact details and an unsubscribe mechanism. Implied consent can exist when the person conspicuously published the address without a "no unsolicited messages" statement and the message is relevant to their business role. | CASL, S.C. 2010, c. 23, s. 6(1)–(2) and s. 10(9)(b), https://laws-lois.justice.gc.ca/eng/acts/E-1.6/ | Was the address published by the person, with no refusal statement, and is the message about their role? Keep a record of where it was published. |
| United Kingdom | Email marketing to individual subscribers (including sole traders and some partnerships) needs consent or the existing-customer "soft opt-in". Corporate bodies (companies, LLPs, government bodies) may be emailed. Every marketing email, to any subscriber, must not hide the sender and must give a valid address for opt-out requests. | PECR 2003, regulation 22 (consent, soft opt-in) and regulation 23 (sender identity, opt-out address), https://www.legislation.gov.uk/uksi/2003/2426/regulation/22 and https://www.legislation.gov.uk/uksi/2003/2426/regulation/23 (re-read 2026-10-08) | Is the recipient a corporate body or an individual/sole trader? |
| EU (general) | Email for direct marketing to natural persons needs prior consent, with an existing-customer exception; protection for business subscribers is left to each member state, and several require consent for business addresses too. | Directive 2002/58/EC, article 13 (as transposed nationally), https://eur-lex.europa.eu/eli/dir/2002/58/oj | Which member state, and does its law cover business addresses? |

For any other country, add one ASK row: "check the rule for recipients in [country]".

## Always
- CO-08 An opt-out reply means stop and suppress (ground rule 7).
- CO-09 No deceptive subject, sender or claimed relationship (ground rule 5).

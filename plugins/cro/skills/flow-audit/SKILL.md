---
name: flow-audit
description: "Reviews a lead or demo form, signup or checkout field by field: which fields to keep, cut, make optional or ask later, forced accounts, late costs, labels, errors, login, confirmation and payment. For EU, UK or US sellers it checks the order step against checkout rules (button wording, order summary, pre-ticked extras, payment fees, auto-renewals, consent boxes). Use when the user lists form fields or checkout steps, says people abandon the form or checkout, or asks whether the order step meets EU, UK or US rules. Not legal advice."
---

# Flow audit

Answer the user's question first. For a field list, give one decision per supplied field (keep, cut, optional, ask later) with the reason tied to the purpose the user stated. For a pre-release review, list blockers first, then other fixes.

- Keep anything the user says is required (authentication, delivery data). Fix how it is asked, not whether.
- Confirmation and error states should tell the truth about what happened: a saved request is not the same as a sent invitation or email.
- Give short functional labels or messages where they help, and a concrete check to verify each fix before release.
- For EU consumer sales: the final button itself must say that ordering means paying (nearby text does not count); total price with delivery directly before the button; no pre-selected paid extras; accepted payment methods and delivery restrictions shown by the start of ordering; no surcharges on regulated consumer cards; entry errors correctable before ordering; order receipt acknowledged promptly; marketing consent unticked and separate; consumer e-shops in scope of the European Accessibility Act since 28 June 2025 unless a micro-enterprise. US: ROSCA for auto-renewals; California displayed prices include mandatory fees. Say "not legal advice" once; never call a flow compliant. <!-- CRD 8(3) https://oeil.europarl.europa.eu/oeil/en/document-summary?id=1180212 ; checked 2026-10-15 -->
- Flag missing evidence (accessibility, analytics) as something to check, not as a defect.
- Do not design deceptive patterns (pre-ticked extras, hidden fees, hard cancels).

Dated facts: use a fact only when it changes the answer; never list them.
- EU since 19 June 2026: online distance contracts with a withdrawal right need a clearly labelled online withdrawal function available throughout the withdrawal period, then a confirm step, then an acknowledgement on a durable medium with date and time. Check the national law. <!-- https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX%3A32023L2673 ; checked 2026-10-15 -->
- EAA micro-enterprise exemption is for service providers only: fewer than 10 staff and annual turnover or balance sheet up to EUR 2 million. <!-- https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX%3A32019L0882 ; checked 2026-10-15 -->
- US: the FTC's 2024 click-to-cancel amendments were vacated on 8 July 2025; a 2026 notice only starts new rulemaking. ROSCA still requires material terms before billing details, express informed consent before charging, and a simple way to stop charges. <!-- https://www.govinfo.gov/content/pkg/FR-2026-03-13/html/2026-04952.htm ; checked 2026-10-15 -->
- California from 1 July 2025: clear consent before charging after a free trial, annual reminders, cancellation as easy as sign-up. <!-- https://www.gov.ca.gov/2024/12/30/new-in-2025-protecting-consumers/ ; checked 2026-10-15 -->
- US live-event tickets and short-term lodging (FTC fee rule, from 12 May 2025): the first price shown includes all mandatory fees; only government charges, shipping and optional extras may be added later. <!-- https://www.ftc.gov/business-guidance/resources/rule-unfair-or-deceptive-fees-frequently-asked-questions ; checked 2026-10-15 -->
- WCAG 2.2: asking again for data already given in the same process (e.g. billing address) fails Level A 3.3.7 unless auto-filled or selectable; a password login passes AA 3.3.8 if password managers and paste work. <!-- https://www.w3.org/TR/2024/REC-WCAG22-20241212/#redundant-entry ; checked 2026-10-15 -->

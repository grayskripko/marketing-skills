---
name: flow-audit
description: "Reviews a lead or demo form, signup or checkout field by field: which fields to keep, cut, make optional or ask later, forced accounts, late costs, labels, errors, login, confirmation and payment. For EU, UK or US sellers it checks the order step against checkout rules (button wording, order summary, pre-ticked extras, payment fees, auto-renewals, consent boxes). Use when the user lists form fields or checkout steps, says people abandon the form or checkout, or asks whether the order step meets EU, UK or US rules. Not legal advice."
---

# Flow audit

Answer the user's question first. For a field list, give one decision per supplied field (keep, cut, optional, ask later) with the reason tied to the purpose the user stated. For a pre-release review, list blockers first, then other fixes.

- Keep anything the user says is required (authentication, delivery data). Fix how it is asked, not whether.
- Confirmation and error states should tell the truth about what happened: a saved request is not the same as a sent invitation or email.
- Give short functional labels or messages where they help, and a concrete check to verify each fix before release.
- For EU consumer sales: the final button itself must say that ordering means paying (nearby text does not count); total price with delivery directly before the button; no pre-selected paid extras; accepted payment methods and delivery restrictions shown by the start of ordering; no surcharges on regulated consumer cards; entry errors correctable before ordering; order receipt acknowledged promptly; marketing consent unticked and separate; consumer e-shops in scope of the European Accessibility Act since 28 June 2025 unless a micro-enterprise. US: ROSCA for auto-renewals; California displayed prices include mandatory fees. Say "not legal advice" once; never call a flow compliant.
- Flag missing evidence (accessibility, analytics) as something to check, not as a defect.
- Do not design deceptive patterns (pre-ticked extras, hidden fees, hard cancels).

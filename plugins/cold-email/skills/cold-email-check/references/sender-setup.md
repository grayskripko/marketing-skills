# Sender setup

Judged only from records or headers the user pastes. Run no DNS query. Ask about sending volume and destination mix only when needed to determine requested provider-policy applicability. For an authentication diagnosis, report only relevant knowns, unknowns and admin fixes in the requested shape. Provider tables are background for provider-policy questions, not mandatory output. Sources were read on 2026-09-30; if provider-policy advice is requested, identify the applicable scope and any uncertainty about current verification.

## All senders

| Requirement | Google | Yahoo | Microsoft |
|---|---|---|---|
| SPF or DKIM for the sending domain | required | required | see bulk block |
| Valid forward and reverse DNS for sending IPs or domains | required | required | — |
| TLS connection | required | — | — |
| Message format per RFC 5322 (Yahoo also cites RFC 5321) | required | required | — |
| Spam complaint rate below 0.3% | required (Postmaster Tools; aim below 0.1%) | required | — |
| DMARC record published (p=none at least) | recommended for every sender (heuristic of this plugin); required for bulk senders, see below | same | same |

## Provider-specific bulk-sender requirements

Use this block only when the user asks about provider requirements; omit it for paste-only authentication diagnosis. Keep providers and applicability scopes separate. Use supplied volume and destination context; ask the minimum missing scope question only when it changes the requested applicability answer.

- Google: senders of 5,000 or more messages a day to personal Gmail accounts need SPF and DKIM, a DMARC record, a From domain aligned with SPF or DKIM, and one-click unsubscribe for marketing and subscribed messages, plus a visible unsubscribe link.
- Yahoo: bulk senders need SPF and DKIM, a DMARC policy of at least p=none that passes, a From domain aligned with the SPF or DKIM domain, a working list-unsubscribe header (one-click per RFC 8058 recommended) and must honor unsubscribes within 2 days.
- Microsoft (Outlook.com consumer addresses: hotmail.com, live.com, outlook.com): domains sending more than 5,000 emails a day must pass SPF and DKIM and publish DMARC of at least p=none aligned with SPF or DKIM, enforced from 2025-05-05. The post states both that failing mail is routed to Junk and, in its 2025-04-29 update, that it is rejected with "550; 5.7.515"; treat it as "junked or rejected" and check the current post.

## Sources
- Google Workspace Admin Help, "Email sender guidelines", support.google.com/a/answer/81126 (requirements from 2024-02-01).
- Yahoo Sender Hub, "Sender Best Practices", senders.yahooinc.com/best-practices.
- Microsoft Tech Community, "Strengthening Email Ecosystem: Outlook's New Requirements for High-Volume Senders" (2025-04-02, updated 2025-04-29).

## Reading pasted records
- SPF: a TXT record starting `v=spf1`. "~all" is a soft fail, "-all" a hard fail; "+all" or "?all" lets any server send as the domain and is a FIX. More than one SPF record for a domain is a fault. More than 10 DNS-lookup mechanisms and modifiers (include, a, mx, ptr, exists, redirect) makes SPF fail with a permanent error (RFC 7208, section 4.6.4); count them and report "can't tell" when an include is not expanded.
- DKIM: a TXT record at `<selector>._domainkey.<signing-domain>` with `v=DKIM1`. Both selector and actual signing domain must be established; never assume the visible From domain is the signing domain. A `p=` key that looks cut off (very short, or ending mid-value in the paste) is "can't tell from input: publish or paste the full key".
- DMARC: a TXT record at `_dmarc.domain` starting `v=DMARC1` with a `p=` tag. A `rua=` address receives aggregate reports, which show who sends as the domain; suggest adding one if missing.
- Headers: `Authentication-Results` shows spf=, dkim= and dmarc= pass or fail for a real message.

# Reading AI-bot access from pasted logs

Useful fields: UTC timestamp, host, method, exact path, full user agent, original client IP, edge status, origin status, response size and type, cache result, WAF action and rule ID, request ID, and a short response excerpt. Work with what is supplied; do not demand every field.

1. Identity. A user agent is a claim. Compare the original source IP with the provider's published IP list (OpenAI, Perplexity and Anthropic lists in `provider-controls.md`); for Google use reverse DNS plus forward confirmation or Google's published ranges. Behind a proxy, use only a trusted original-client field. Today's list is evidence for today, not proof for an old log. IPs in documentation ranges (192.0.2.0/24, 198.51.100.0/24, 203.0.113.0/24, RFC 5737) or redacted IPs cannot be verified: say so.
2. Policy. Evaluate the robots group and path that applied at the time of the visit, on that host.
3. Delivery. Separate an edge block or challenge from an origin failure. An origin-only log misses requests denied at the edge; cache hits may never reach the origin. A 200 alone does not prove the page was delivered: Cloudflare challenge pages carry `cf-mitigated: challenge` <!-- https://developers.cloudflare.com/cloudflare-challenges/challenge-types/challenge-pages/detect-response/, updated 2026-05-05 -->. Distinguish 401/403, 429, 5xx and challenge responses.
4. Content. Compare what was delivered with the intended public page.
5. Conclusion. Report separately: policy permission, identified request, content delivery, indexing evidence and citation evidence. No rows means no observed request in that window, not that the bot cannot access the site. Access does not prove indexing or citation.

For a blocked verified search bot, propose a scoped exception to the identified WAF rule for that bot's published IPs; never a user-agent-only exception or disabling the WAF.

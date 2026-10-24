# Privacy

This package contains skill instructions, reference text and an icon. It runs no service and includes no executable integration.

Input can contain reservation dates, location, guest messages and payment amounts. Names, contact details, addresses, reservation codes and payment identifiers are unnecessary; redact them before sharing. The assistant uses supplied facts only to identify cancellation terms and calculate refunds in the current conversation.

Network: when verifying current policy, the assistant fetches public Airbnb Help Center URLs cited in the references, relevant official Help Center links from those pages, and https://www.airbnb.com/robots.txt. Redirects remain on Airbnb-owned public Help Center pages. Booking details are never added to a URL, search query or request body. Paths disallowed by robots.txt are not fetched. There is no account login, connector, API key, reservation access or payment operation.

The plugin has no telemetry, database or retention of its own. The assistant provider processes and retains the conversation under the user's existing settings. Local exported files are read only when supplied for the task. Delete supplied files or the conversation using the host application's controls.

Support: https://github.com/grayskripko/marketing-skills/issues

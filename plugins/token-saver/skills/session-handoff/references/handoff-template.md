# Handoff note template

Copy this block and fill every field. Write "none stated" when the conversation has nothing for a field.

```
HANDOFF

Goal:
<one sentence>

Done so far:
- <what> (<path or artifact>)

Current state:
- Works: <what>
- Fails: <what>
- Last error: <copied exactly>

Decisions and why:
- <decision> because <reason>

Tried and failed, don't retry:
- <attempt>: <why it failed>

Constraints and preferences:
- <as the user stated them>

Open questions:
- <question>

Next step:
<one concrete action>

Commands to re-run:
<command, copied exactly>
```

## Example (fictional)

```
HANDOFF

Goal:
Fix the logout flow in the Northwind Ledger web app so the session ends cleanly.

Done so far:
- Token refresh moved to the auth service (src/auth/refresh.ts)

Current state:
- Works: login, token refresh
- Fails: logout test
- Last error: expected status 200, received 401

Decisions and why:
- Keep cookies httpOnly because the security review requires it

Tried and failed, don't retry:
- Changing the cookie domain to the parent domain: same 401, cookie still sent

Constraints and preferences:
- No new dependencies

Open questions:
- Does the logout endpoint expect the refresh token or the access token?

Next step:
Log which token the logout endpoint receives in the failing test.

Commands to re-run:
npm test -- logout
```

# SOP: Password / MFA Reset

**Scope:** Account lockouts, forgotten passwords, MFA re-enrollment requests.

## Before making any change

1. Verify requestor identity. Never reset credentials from a chat/email request alone.
   - Acceptable verification: employee ID lookup + manager confirmation via a channel separate from the request itself (e.g. Slack, not email if the request came by email).
   - If identity can't be confirmed, escalate to security team rather than proceeding.
2. Check sign-in/audit logs for the account before resetting anything — rule out active compromise (impossible travel, unfamiliar IP ranges, unusual failed-attempt patterns) before treating this as routine.

## Standard reset steps

1. Unlock the account in the identity provider admin console (Entra ID / Okta / equivalent).
2. If MFA method is lost (new device, lost phone): revoke the old MFA method entirely rather than leaving it registered.
3. Issue a secure, time-limited re-enrollment link — never send a temporary password over an unencrypted channel.
4. Stay on the call/session until the employee confirms successful sign-in.

## Escalation triggers

- Any sign of account compromise → escalate to security immediately, do not just reset and close.
- Repeated lockouts for the same user within 30 days → flag for a deeper look (could indicate a phishing attempt or a device/sync issue worth investigating).

## Closing the ticket

- Confirm the employee has verified access to their primary tools (not just the login screen) before marking resolved.

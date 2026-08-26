# SOP: VPN Troubleshooting

**Scope:** Remote employee VPN connection failures.

## Step 1 — Gather the essentials

- Exact error message or code (don't accept "it just doesn't work" — ask for a screenshot).
- When did it last work? Anything change recently (new device, OS update, location, network)?

## Step 2 — Rule out account/permissions issues first

- Confirm the employee's account is active and has VPN group membership in the identity provider.
- If access was recently changed or the account is new, this is likely the cause — check here before touching the client.

## Step 3 — Client-side checks

- Confirm VPN client version is current.
- Check device certificate expiry (a very common silent failure point — certs typically auto-renew but the job can fail without alerting anyone).
- Restart the VPN client and, if needed, the device.

## Step 4 — Server-side checks (if client-side is clean)

- Check VPN gateway logs for the connection attempt.
- Confirm no active outage or maintenance window affecting the gateway.
- Escalate to network team if the issue appears server-side.

## Step 5 — Confirm full resolution, not just connection

- After reconnecting, confirm the employee can actually reach the internal resources they need (Git server, staging, internal tools) — a successful VPN handshake doesn't always mean full network access is working.

## Closing the ticket

- Note the root cause clearly (cert expiry, credential issue, client bug, network outage) so patterns across multiple tickets can be spotted.

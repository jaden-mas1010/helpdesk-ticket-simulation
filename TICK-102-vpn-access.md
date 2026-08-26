# TICK-102 — Remote employee cannot connect to VPN

| Field | Value |
|---|---|
| Requestor | R. Okafor (Engineering, Remote) |
| Category | Network / Access |
| Priority | P2 |
| SLA target | 2 business hours |
| Time to resolve | 1 hour 10 minutes |
| Platform | macOS Sonoma, GlobalProtect VPN client |

## Intake

Employee cannot connect to the corporate VPN. Getting a generic "connection failed" error. Blocks access to internal Git server and staging environment — flagged P2 since it's blocking active work.

## Triage

- Asked for exact error text and a screenshot — error code pointed to a certificate handshake failure, not a credentials issue.
- Checked VPN gateway logs: no connection attempt reaching the gateway at all, suggesting a local client-side issue rather than a server-side block.
- Confirmed employee's account has active VPN group membership (ruled out an access/permissions problem).

## Resolution steps

1. Followed [VPN Troubleshooting SOP](../sops/SOP-vpn-troubleshooting.md) — started with client-side checks before escalating to network team.
2. Confirmed the VPN client's machine certificate had expired (routine annual renewal event, not unique to this user).
3. Remotely pushed an updated device certificate via MDM profile.
4. Had the employee restart the VPN client and reconnect — successful on first attempt post-fix.
5. Verified access to internal Git server and staging environment to confirm full resolution, not just a successful handshake.

## Root cause

Expired device certificate; the auto-renewal MDM job had silently failed for this device the prior week.

## Follow-up

- Flagged the failed auto-renewal job to the systems team to check if other devices are affected (proactive check beyond just closing this one ticket).
- Ticket closed after employee confirmed sustained connectivity for 30+ minutes.

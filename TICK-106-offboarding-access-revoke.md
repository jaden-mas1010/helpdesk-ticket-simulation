# TICK-106 — Immediate access revocation for departing employee

| Field | Value |
|---|---|
| Requestor | People Team (on behalf of departing employee: D. Osei, Sales) |
| Category | Offboarding |
| Priority | P1 (security-sensitive, time-bound to termination timestamp) |
| SLA target | All access revoked within 15 minutes of the effective termination time |
| Time to resolve | 12 minutes |
| Platform | Microsoft 365, VPN, CRM, Slack, physical badge system |

## Intake

People team notified IT of an involuntary termination effective immediately at 2:00 PM. Required same-day, time-boxed access revocation across all systems per company offboarding policy — this category always runs P1 given the security exposure of any delay.

## Triage

- No troubleshooting needed here — this is a scripted, checklist-driven action, not a diagnostic ticket. Priority was execution speed and completeness, not investigation.
- Pulled the employee's full access list from the identity provider to confirm every system they had standing access to (avoids missing a less obvious tool like a shared drive or third-party SaaS seat).

## Resolution steps

1. Disabled the M365 account and revoked all active sessions at exactly 2:00 PM, per the [offboarding runbook](https://github.com/jaden-mas1010) procedure.
2. Revoked VPN certificate and removed the device from the MDM trusted list.
3. Removed CRM and Slack access; transferred CRM record ownership to the employee's manager per data continuity policy.
4. Deactivated the physical badge in the building access system.
5. Placed the employee's mailbox on litigation hold pending People team confirmation it wasn't required, then converted to a shared mailbox for manager handoff.
6. Logged every revoked system with a timestamp in the ticket for audit purposes.

## Root cause

N/A — policy-driven offboarding action.

## Follow-up

- Confirmed with the employee's manager that no active work was locked in inaccessible files; coordinated file handoff before final account deletion 30 days out.
- Ticket closed with a full audit trail attached, in case of a later access-dispute review.

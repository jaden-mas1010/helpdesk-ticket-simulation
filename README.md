# Helpdesk Ticket Simulation

A set of realistic IT support tickets simulating a day-to-day helpdesk workload across Windows, macOS, M365, and general access management — modeled on the ticket types a Tier 1/2 IT Support Engineer resolves in a mid-sized SaaS company.

## Why this repo exists

Most of my public work leans security/network-engineering heavy (SOC lab, OT/ICS detection lab, SIEM investigations). This repo demonstrates the other half of IT operations: hands-on end-user support, ticket triage under SLA, and clear documentation — the day-to-day of an IT Support Engineer role.

Each ticket follows a consistent format: **intake → triage → resolution steps → root cause → follow-up**, the way it would appear in a real ticketing system (Jira Service Management / Freshservice / Zendesk style).

## Ticket index

| ID | Category | Priority | Summary |
|----|----------|----------|---------|
| [TICK-101](tickets/TICK-101-password-reset.md) | Access | P3 | Locked out after failed MFA attempts |
| [TICK-102](tickets/TICK-102-vpn-access.md) | Network/Access | P2 | Remote employee cannot connect to VPN |
| [TICK-103](tickets/TICK-103-software-install-failure.md) | Software | P3 | M365 app install fails with error code |
| [TICK-104](tickets/TICK-104-hardware-fault.md) | Hardware | P2 | Laptop won't boot past login screen |
| [TICK-105](tickets/TICK-105-new-hire-onboarding.md) | Onboarding | P1 | New hire device + account setup for Day 1 |
| [TICK-106](tickets/TICK-106-offboarding-access-revoke.md) | Offboarding | P1 | Immediate access revocation for departing employee |

## SOPs referenced

- [Password / MFA Reset SOP](sops/SOP-password-mfa-reset.md)
- [VPN Troubleshooting SOP](sops/SOP-vpn-troubleshooting.md)
- [New Hire Provisioning Checklist](sops/SOP-new-hire-provisioning.md)

## Format notes

- Priorities follow a standard P1 (critical, <1hr response) → P4 (low, <2 business days) scale.
- Timestamps and SLA windows are illustrative, based on common industry SLA benchmarks, not pulled from a live system.
- Screenshots are recreated/mocked for demonstration — no real company data is used anywhere in this repo.

## Related work

- [IT Onboarding/Offboarding Runbook](https://github.com/jaden-mas1010) — the process-level runbook this ticket set operationalizes, with live Jira Service Management tickets.

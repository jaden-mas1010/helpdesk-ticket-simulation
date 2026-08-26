# TICK-105 — New hire device + account setup for Day 1

| Field | Value |
|---|---|
| Requestor | People Team (on behalf of new hire: A. Fernandes, Marketing) |
| Category | Onboarding |
| Priority | P1 (hard deadline: employee start date) |
| SLA target | Device + accounts ready 1 business day before start date |
| Time to resolve | Completed 1 day ahead of start date |
| Platform | macOS, Microsoft 365, internal SaaS tools |

## Intake

People team submitted a new hire request 5 business days before A. Fernandes's start date, per standard lead time. Role: Marketing Coordinator, remote, needs a MacBook and access to M365, the CRM, and the design tool suite.

## Triage

- Cross-checked the request against the [New Hire Provisioning Checklist](../sops/SOP-new-hire-provisioning.md) to confirm all required fields were present (manager, department, start date, role-based access tier).
- Flagged one gap: request didn't specify which CRM permission tier — followed up with the hiring manager same day to avoid a delay.

## Resolution steps

1. Provisioned a MacBook from inventory: applied the standard corporate image, enrolled it in MDM, and pre-installed the baseline app set (M365, Slack, VPN client, endpoint security agent).
2. Created the M365 account and mailbox; assigned the correct license tier and added to relevant distribution lists.
3. Requested CRM and design tool licenses through the respective app owners once permission tier was confirmed.
4. Set up MFA enrollment to be completed as a guided Day 1 first step, not pre-done, for security (avoids shipping a device with live MFA already bound to IT's setup session).
5. Shipped the device with a printed quick-start guide; confirmed tracking and delivery one business day before start date.
6. Sent Day 1 IT welcome instructions to the new hire and their manager.

## Root cause

N/A — standard onboarding, not an incident.

## Follow-up

- Confirmed successful first login and MFA enrollment on start day.
- Closed ticket only after new hire confirmed access to all required tools, not at device shipment.

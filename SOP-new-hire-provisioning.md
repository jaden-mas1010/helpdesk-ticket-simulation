# SOP: New Hire Provisioning Checklist

**Scope:** Device and account setup ahead of a new employee's start date.

## Intake requirements (request is incomplete without these)

- [ ] Employee name, role, department, manager
- [ ] Start date
- [ ] Work location (remote / office / hybrid) — determines device type and shipping lead time
- [ ] Role-based access tier (which tools: CRM, design suite, engineering repos, finance systems, etc.)

If any field is missing, follow up with the requester immediately rather than guessing — incorrect access tier is a common source of Day 1 delays.

## Lead time

- Standard: 5 business days before start date.
- Remote hires: add 1–2 extra days to account for hardware shipping.

## Device setup

1. Select device from inventory matching role requirements (standard build vs. higher-spec for engineering/design roles).
2. Apply corporate image and enroll in MDM.
3. Install baseline app set: M365, Slack, VPN client, endpoint security agent.
4. Do **not** pre-bind MFA to the device before shipping — MFA enrollment should happen with the new hire present on Day 1, for security continuity (avoids a device in transit having live, unbound MFA credentials).

## Account setup

1. Create M365 account, assign license tier, add to relevant distribution lists and groups.
2. Request role-specific tool licenses (CRM, design suite, etc.) from respective app owners.
3. Pre-stage a Day 1 welcome email with login instructions, sent the morning of start date, not before.

## Day 1 confirmation

- Confirm first successful login and MFA enrollment.
- Confirm access to every tool listed in the original request — close the ticket only after this is verified, not at device shipment.

## Common failure points to watch for

- Ambiguous or missing access tier in the original request.
- Device shipping delays for remote hires in areas with longer courier lead times.
- Forgetting to add the new hire to team-specific distribution lists or shared drives.

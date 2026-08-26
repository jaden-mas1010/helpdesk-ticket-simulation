# TICK-104 — Laptop won't boot past login screen

| Field | Value |
|---|---|
| Requestor | T. Lindqvist (Customer Success, Office) |
| Category | Hardware |
| Priority | P2 |
| SLA target | 2 business hours |
| Time to resolve | 3 hours (includes loaner swap) |
| Platform | Windows 11, Dell Latitop 5440 |

## Intake

Employee's laptop hangs on a black screen with spinning dots immediately after entering their password. Has tried restarting three times with no change. Employee has back-to-back customer calls starting in 90 minutes — flagged P2 due to business impact.

## Triage

- Asked the employee to note any recent changes: a Windows update had installed overnight per their recollection.
- Attempted remote diagnostics via MDM — device was unreachable, consistent with it being stuck pre-desktop rather than a network issue.
- Given the time-sensitive customer calls, decided a loaner swap was faster than an on-the-spot fix, with the original device triaged in parallel.

## Resolution steps

1. Issued a pre-imaged loaner laptop from the office hardware pool; had the employee signed in and ready for their first call within 20 minutes.
2. Took the original laptop for diagnosis: booted into Safe Mode successfully, isolating the issue to the recent Windows update rather than a hardware failure.
3. Rolled back the problematic update via Safe Mode's update history.
4. Confirmed clean boot to desktop after rollback; ran a full system health check before returning the device.
5. Swapped the employee back to their original laptop at end of day, confirmed data/settings were untouched throughout.

## Root cause

A faulty Windows cumulative update caused a boot hang; not device-specific, so flagged for wider monitoring.

## Follow-up

- Escalated the specific update KB number to IT ops for temporary deferral across the fleet pending Microsoft's fix.
- Logged the loaner swap and return in the asset tracker to keep hardware inventory accurate.

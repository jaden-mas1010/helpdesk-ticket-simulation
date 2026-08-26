# TICK-103 — M365 app install fails with error code

| Field | Value |
|---|---|
| Requestor | S. Mehta (Finance, Office) |
| Category | Software |
| Priority | P3 |
| SLA target | 1 business day |
| Time to resolve | 35 minutes |
| Platform | Windows 11, Microsoft 365 Apps |

## Intake

Employee trying to install Microsoft Access (not part of the default M365 install package) for a finance reporting tool. Install fails partway through with error code 30015-1015 (0-4).

## Triage

- Looked up the error code: known Click-to-Run install conflict, usually caused by a partial/corrupted prior install or leftover install cache.
- Confirmed employee has a valid M365 license tier that includes Access (ruled out a licensing gap before troubleshooting further).

## Resolution steps

1. Ran the Microsoft Support and Recovery Assistant (SaRA) tool to fully uninstall the broken M365 Apps install state.
2. Cleared the leftover Click-to-Run cache directories.
3. Reinstalled Microsoft 365 Apps via the company software center, selecting the Access component explicitly.
4. Verified Access launched cleanly and could open a test database file.
5. Confirmed no other Office apps (Outlook, Excel) were disrupted by the reinstall.

## Root cause

Corrupted Click-to-Run cache from a previous forced update, unrelated to the current install attempt.

## Follow-up

- Documented the SaRA fix in the internal knowledge base under "Office install error 30015" so future occurrences can be self-served or resolved faster by other team members.

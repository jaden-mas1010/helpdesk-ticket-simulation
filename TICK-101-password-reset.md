# TICK-101 — Locked out after failed MFA attempts

| Field | Value |
|---|---|
| Requestor | J. Alvarez (Sales, Remote) |
| Category | Access / Identity |
| Priority | P3 |
| SLA target | 4 business hours |
| Time to resolve | 22 minutes |
| Platform | Windows 11, Microsoft 365 (Entra ID) |

## Intake

Employee reports they cannot sign into their laptop or Outlook. Says they changed phones over the weekend and their Microsoft Authenticator app no longer has the account registered. Three failed MFA attempts triggered an account lockout.

## Triage

- Confirmed identity via employee ID and manager Slack confirmation (standard verification step before any access change).
- Checked Entra ID sign-in logs: three failed MFA challenges from a new, unrecognized device — consistent with a new phone with no authenticator re-registration, not a compromise attempt.
- No suspicious IP or impossible-travel flag on the sign-in log.

## Resolution steps

1. Verified requestor identity per SOP (see [Password/MFA Reset SOP](../sops/SOP-password-mfa-reset.md)).
2. Unlocked the account in Entra ID admin center.
3. Revoked the old MFA method tied to the previous phone.
4. Sent a secure MFA re-registration link; walked the employee through re-enrolling Authenticator on the new device via screen share.
5. Confirmed successful sign-in to both the laptop and Outlook.

## Root cause

Device migration without re-registering MFA before the old device was wiped.

## Follow-up

- Added a note to the new-device offboarding checklist: remind employees to re-register MFA *before* wiping an old phone, not after.
- No further action needed; ticket closed same-session.

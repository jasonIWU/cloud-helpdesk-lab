# INC002 — MFA Not Working After Getting New Phone

| Field | Value |
|-------|-------|
| Ticket Number | INC002 |
| Date | March 31, 2026 |
| Caller | Sandra Kim |
| Priority | 2 - High |
| Category | User Account |
| State | Resolved |
| Time to Resolve | ~20 minutes |

---

## Issue Description

User received a new phone and Microsoft Authenticator is no longer generating valid codes. User cannot access any company applications requiring MFA.

---

## Troubleshooting Steps

1. Verified user identity.
2. Confirmed user has a new device and old Authenticator data was not transferred.
3. Navigated to Entra ID > Users > Sandra Kim > Authentication methods.
4. Deleted old registered authenticator device.
5. Generated Temporary Access Pass (TAP) for user to re-register MFA.
6. Guided user through re-registering Microsoft Authenticator on new device.
7. Confirmed user can access applications successfully.

---

## Resolution Notes

MFA registration was tied to previous device. Old authentication method removed and Temporary Access Pass issued. User successfully re-registered Authenticator on new phone. Advised user to set up a backup authentication method (e.g. email) to prevent this issue in future.

---

## Resolution Code

Solved (Permanently)

---

## Lessons Learned

- Advise all users to set up a secondary MFA method (email or alternate phone) as a backup.
- Temporary Access Pass is the correct tool for MFA re-registration — do not disable MFA entirely.
- Document device changes in the user's profile for audit purposes.

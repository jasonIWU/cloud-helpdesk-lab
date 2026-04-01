# INC001 — Account Lockout

| Field | Value |
|-------|-------|
| Ticket Number | INC001 |
| Date | March 31, 2026 |
| Caller | Marcus Webb |
| Priority | 2 - High |
| Category | User Account |
| State | Resolved |
| Time to Resolve | ~15 minutes |

---

## Issue Description

User reports seeing an account locked message when attempting to log in to their workstation. Multiple failed login attempts detected.

---

## Troubleshooting Steps

1. Verified user identity by confirming employee ID and department.
2. Checked Entra ID audit logs — confirmed 5 failed login attempts in the past 10 minutes.
3. Reset user password in Azure Entra ID with must change on next login flag enabled.
4. Communicated temporary password to user via verified phone callback.
5. Confirmed user was able to log in successfully and set new password.

---

## Resolution Notes

Account was locked due to multiple failed login attempts. Password reset performed in Entra ID. User confirmed successful login. Advised user to enable SSPR for future self-service resets.

---

## Resolution Code

Solved (Permanently)

---

## Lessons Learned

- Always verify user identity before performing a password reset to prevent social engineering attacks.
- Advise users to register for SSPR to reduce repeat tickets of this type.
- Check audit logs before resetting — helps identify whether lockout was due to user error or a potential brute force attempt.

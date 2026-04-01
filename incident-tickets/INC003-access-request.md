# INC003 — Access Request: HR Shared Resources

| Field | Value |
|-------|-------|
| Ticket Number | INC003 |
| Date | March 31, 2026 |
| Caller | James Tran |
| Priority | 3 - Moderate |
| Category | Request |
| State | Resolved |
| Time to Resolve | ~10 minutes |

---

## Issue Description

New HR employee requires access to HR-Staff shared resources. Currently has no group membership and cannot access department files.

---

## Troubleshooting Steps

1. Verified request came from HR Director Lisa Morales via email confirmation (approver required before any access grant).
2. Navigated to Entra ID > Groups > HR-Staff.
3. Added James Tran as a member of the HR-Staff security group.
4. Confirmed group membership propagated (allow 5 minutes for propagation).
5. Followed up with user to confirm access granted successfully.

---

## Resolution Notes

Access request approved by HR Director. User added to HR-Staff security group in Entra ID. Access to HR shared resources confirmed active.

---

## Resolution Code

Solved (Permanently)

---

## Lessons Learned

- Never grant access without documented approval from an authorized manager or director.
- Group membership propagation can take up to 5 minutes — set expectations with the user.
- Access requests should always be tracked in the ticketing system for audit purposes.

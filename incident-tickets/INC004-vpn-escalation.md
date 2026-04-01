# INC004 — VPN Connectivity Issue (Tier 2 Escalation)

| Field | Value |
|-------|-------|
| Ticket Number | INC004 |
| Date | March 31, 2026 |
| Caller | Robert Chen |
| Priority | 2 - High |
| Category | Network |
| State | In Progress — Escalated to Tier 2 |
| Assigned To | Network Team |

---

## Issue Description

IT Manager is unable to connect to company VPN from home office. Receiving "Authentication failed" error. On-site access works normally.

---

## Troubleshooting Steps (Tier 1)

1. Verified user identity and confirmed issue is remote VPN only — on-site access works fine.
2. Checked Entra ID sign-in logs — no failed authentication events found for this user.
3. Confirmed VPN client version is up to date.
4. Attempted basic troubleshooting: restarted VPN client, cleared credentials cache — issue persists.
5. Issue is beyond Tier 1 scope — requires network team access to VPN gateway logs.
6. Escalated ticket to Tier 2 Network team with full troubleshooting notes attached.

---

## Escalation Notes

Tier 1 troubleshooting completed. VPN client verified current, credentials cache cleared, Entra ID sign-in logs checked with no errors found. Issue escalated to Tier 2 Network team for VPN gateway investigation. Ticket remains open and assigned to Network queue.

---

## Lessons Learned

- Know your escalation boundaries — attempting Tier 2 fixes without proper access wastes time and can cause additional issues.
- Always document all troubleshooting steps before escalating so Tier 2 doesn't repeat work.
- Entra ID sign-in logs are the first place to check for authentication-related VPN issues — if no errors appear there, the problem is likely on the network/VPN gateway side.

# CarterTech IT Help Desk Runbook

**Version:** 1.0  
**Last Updated:** March 2026  
**Maintained by:** IT Support Team

This runbook documents standard operating procedures (SOPs) for the most common helpdesk scenarios at CarterTech Inc. All technicians should follow these procedures to ensure consistent, secure, and auditable support delivery.

---

## SOP 1 — Password Reset in Azure Entra ID

**When to use:** User is locked out, forgot their password, or requires a forced reset.

**Steps:**
1. Verify user identity — confirm full name, employee ID, and department before proceeding.
2. Navigate to Azure portal > Entra ID > Users.
3. Search for and click on the user's name.
4. Click **Reset password** in the top toolbar.
5. Check **"Require this user to change their password when they first sign in"**.
6. Click **Reset password** and note the temporary password shown.
7. Communicate the temporary password to the user via verified phone callback — never via email or chat.
8. Confirm the user can log in successfully.
9. Document the action in the ServiceNow ticket with timestamps.
10. Advise the user to register for SSPR to self-serve future resets.

**Escalate if:** User cannot log in even after reset — may indicate MFA issue or account disable.

---

## SOP 2 — Add User to Security Group

**When to use:** User needs access to shared resources, applications, or department files.

**Steps:**
1. Verify that the request is approved by the user's manager or department director — do not grant access without documented approval.
2. Navigate to Azure portal > Entra ID > Groups.
3. Search for and click the appropriate group (e.g. HR-Staff, IT-Staff).
4. Click **Members** in the left sidebar.
5. Click **+ Add members**.
6. Search for the user and select them.
7. Click **Select** to confirm.
8. Inform the user that access may take up to 5 minutes to propagate.
9. Follow up to confirm access is working.
10. Document the change in the ServiceNow ticket.

**Escalate if:** User needs access to a group that does not exist — may require a new group to be created by a senior admin.

---

## SOP 3 — Disable a Departing Employee's Account

**When to use:** Employee has been terminated, resigned, or is on extended leave requiring account suspension.

**Steps:**
1. Confirm the offboarding request from HR or the employee's manager in writing.
2. Navigate to Azure portal > Entra ID > Users.
3. Click on the departing employee's name.
4. Click **Edit properties** in the top toolbar.
5. Click the **Settings** tab.
6. Uncheck **Account enabled**.
7. Click **Save**.
8. Confirm the account status shows **Disabled** in the user's profile overview.
9. Do NOT delete the account — disabled accounts retain data and can be reinstated if needed.
10. Document the action in ServiceNow with the time, reason, and authorizing manager.

**Escalate if:** Employee has admin roles or owns critical resources — senior admin must review before disabling.

---

## SOP 4 — New Hire Account Provisioning Checklist

**When to use:** New employee is starting and requires IT account setup.

**Pre-provisioning (get from HR):**
- [ ] Full legal name
- [ ] Job title
- [ ] Department
- [ ] Manager name
- [ ] Start date

**Provisioning steps:**
- [ ] Create Entra ID account: firstname.lastname@cartertech.onmicrosoft.com
- [ ] Set temporary password with "must change on first login" enabled
- [ ] Fill in job title, department, and manager fields
- [ ] Add user to appropriate security group (IT-Staff or HR-Staff)
- [ ] Verify account shows as Active in the users list
- [ ] Send welcome email to manager (not the new hire directly) with:
  - Username
  - Temporary password
  - Link to aka.ms/sspr for SSPR registration
  - IT helpdesk contact info
- [ ] Create a ServiceNow ticket documenting all steps and close it as Resolved
- [ ] Follow up on the employee's first day to confirm access is working

---

## SOP 5 — When and How to Escalate to Tier 2

**Escalate to Tier 2 when:**
- The issue requires access to systems you do not have credentials for (VPN gateway, server logs, firewall)
- Basic troubleshooting has been exhausted with no resolution
- The issue affects multiple users or a critical system
- The fix requires changes to infrastructure, DNS, DHCP, or network routing

**How to escalate properly:**
1. Document all troubleshooting steps taken in the Work Notes field — be specific and include timestamps.
2. Change the ticket Assignment Group to the appropriate Tier 2 team (Network, Server, Security).
3. Change the Assigned To field to the Tier 2 team lead if known.
4. Set ticket State to **In Progress** — do not close an escalated ticket.
5. Notify the Tier 2 team via their preferred channel (Slack, email, or phone for P1/P2).
6. Communicate to the user that their ticket has been escalated and provide an estimated response time based on SLA.
7. Follow up with Tier 2 after the SLA window to ensure the ticket is being worked.

**SLA reference:**
- P1 - Critical: 1 hour response
- P2 - High: 4 hour response
- P3 - Moderate: 8 hour response (business hours)

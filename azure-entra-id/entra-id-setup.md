# Azure Entra ID — Setup & Task Documentation

## Tenant Details

| Field | Value |
|-------|-------|
| Tenant Name | CarterTech Inc |
| Account Type | Azure Free Tier |
| Platform | Microsoft Azure Entra ID |
| Completed | March 2026 |

---

## Task 1 — User Account Provisioning

8 user accounts provisioned across IT and HR departments using the format `firstname.lastname@tenant.onmicrosoft.com`.

| User | Department | Title |
|------|------------|-------|
| Marcus Webb | IT | IT Support Technician |
| Priya Nair | IT | IT Support Technician |
| Daniel Ortega | IT | IT Support Technician |
| Robert Chen | IT | IT Manager |
| Sandra Kim | HR | HR Coordinator |
| James Tran | HR | HR Coordinator |
| Aaliyah Foster | HR | HR Coordinator |
| Lisa Morales | HR | HR Director |

**Screenshots:** See `screenshots/` folder — users list showing all 8 accounts.

---

## Task 2 — Security Group Configuration

Two security groups created for department-based access control.

**IT Staff Group**
- Type: Security
- Members: Marcus Webb, Priya Nair, Daniel Ortega, Robert Chen
- Total: 4 members

**HR Staff Group**
- Type: Security
- Members: Sandra Kim, James Tran, Aaliyah Foster, Lisa Morales
- Total: 4 members

**Screenshots:** IT Staff and HR Staff group overview pages.

---

## Task 3 — Multi-Factor Authentication (MFA)

Per-User MFA enabled for all 8 CarterTech accounts via the Entra ID Users panel.

> **Licensing Note:** Conditional Access policy-based MFA requires Entra ID P1 licensing. Per-User MFA is the free-tier alternative. Conditional Access policy was designed and documented but not applied due to licensing constraints. This is a real-world scenario IT administrators regularly encounter.

**Conditional Access Policy Design (not applied — premium required):**
- Policy name: Require MFA for All Users
- Scope: All users, All cloud apps
- Control: Grant access — Require multifactor authentication
- Mode: Report-only (initial), then On after testing

---

## Task 4 — Location-Based Access Policy

> **Licensing Note:** Conditional Access location-based policies also require Entra ID P1. Policy designed and documented below.

**Policy Design:**
- Policy name: Block Sign-in Outside US
- Named location: Approved US Location (marked trusted)
- Scope: All users
- Control: Block access for any location except Approved US Location

---

## Task 5 — Password Reset (Account Lockout Simulation)

| Field | Value |
|-------|-------|
| Target User | Marcus Webb |
| Action | Password reset via Entra ID admin console |
| Setting | Must change password on next sign-in |
| Outcome | Password reset successful |
| Date | March 30, 2026 |

**Screenshot:** Password reset confirmation screen for Marcus Webb.

---

## Task 6 — Account Disable & Reinstatement (Offboarding Simulation)

| Action | User | Status | Time |
|--------|------|--------|------|
| Disable account | Daniel Ortega | Account status: Disabled | 10:06 PM |
| Re-enable account | Daniel Ortega | Account status: Enabled | 10:07 PM |

**Screenshots:** Disabled state and re-enabled state with success notification.

---

## Task 7 — Self-Service Password Reset (SSPR)

> **Licensing Note:** SSPR requires Entra ID Premium licensing on free tier. Configuration documented below.

**SSPR Policy Design:**
- Scope: IT-Staff security group (scoped rollout)
- Authentication methods required: 1
- Available methods: Email, Mobile phone
- Self-service portal: aka.ms/sspr

---

## Task 8 — Audit Log Review

Administrative actions confirmed in Entra ID audit log:

| Action | Target | Status | Time |
|--------|--------|--------|------|
| Enable account | Daniel Ortega | Success | 10:07 PM, March 30 |
| Disable account | Daniel Ortega | Success | 10:06 PM, March 30 |
| Update user | Daniel Ortega | Success | 10:06 PM, March 30 |
| Reset password | Marcus Webb | Success | 9:57 PM, March 30 |
| Create user (x8) | All accounts | Success | March 29, 2026 |

**Screenshot:** Audit log list showing UserManagement entries with Success status.

# Cloud Help Desk Simulation Lab

**Platforms:** Microsoft Azure Entra ID · ServiceNow PDI (Zurich) · GitHub  
**Completed:** March 2026  
**Author:** Jason Iwuoha — B.S. Computer Software Engineering, Washington State University Everett  
**Certifications:** CompTIA Security+

---

## Overview

A cloud-based IT help desk simulation lab built to demonstrate core IT support competencies without requiring local virtual machine infrastructure. The lab simulates a small enterprise environment (CarterTech Inc) with 8 employees across two departments, managed through Azure Entra ID for identity management and ServiceNow for ITSM ticketing.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Microsoft Azure Entra ID | Cloud identity and access management (IAM) |
| ServiceNow PDI (Zurich release) | IT service management (ITSM) and ticketing |
| GitHub | Portfolio documentation and version control |

---

## Skills Demonstrated

- User account provisioning and lifecycle management
- Security group creation and membership management
- Multi-Factor Authentication (MFA) enforcement
- Account lockout, disable, and reinstatement procedures
- Conditional Access policy design and licensing awareness
- Audit log review and administrative accountability
- ITSM ticket creation, documentation, and resolution (ITIL lifecycle)
- SLA definition and priority-based response targets (P1/P2/P3)
- Knowledge Base article creation for self-service support
- Escalation procedures and Tier 2 handoff documentation

---

## Fictional Company

**CarterTech Inc** — simulated small enterprise with two departments

| Department | Users |
|------------|-------|
| IT | Marcus Webb, Priya Nair, Daniel Ortega, Robert Chen (IT Manager) |
| HR | Sandra Kim, James Tran, Aaliyah Foster, Lisa Morales (HR Director) |

---

## Project Structure

```
cloud-helpdesk-lab/
├── README.md
├── lab-report.docx              ← Full documentation report
├── azure-entra-id/
│   ├── entra-id-setup.md        ← Azure setup and task documentation
│   └── screenshots/             ← Azure portal screenshots
├── servicenow/
│   ├── sn-setup.md              ← ServiceNow setup documentation
│   └── screenshots/             ← ServiceNow screenshots
├── incident-tickets/
│   ├── INC001-account-lockout.md
│   ├── INC002-mfa-new-phone.md
│   ├── INC003-access-request.md
│   ├── INC004-vpn-escalation.md
│   └── INC005-new-hire-onboarding.md
└── runbook/
    └── helpdesk-runbook.md      ← Standard operating procedures
```

---

## Key Outcomes

- Provisioned 8 user accounts and 2 security groups in Azure Entra ID
- Enabled MFA for all CarterTech accounts
- Completed 4 resolved incidents and 1 Tier 2 escalation in ServiceNow
- Configured P1/P2/P3 SLA definitions on the Incident table
- Authored and published a Knowledge Base article for self-service password reset
- Documented all findings including real-world licensing constraints (Entra ID P1 required for Conditional Access and SSPR)

---

## Full Report

See [`lab-report.docx`](./lab-report.docx) for the complete documentation including all ticket records, findings, and resume bullets.

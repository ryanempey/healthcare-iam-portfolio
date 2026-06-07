# Project 01 – Healthcare IAM Tenant

## Executive Summary

This project simulates a healthcare organization's Microsoft Entra ID environment and demonstrates core Identity and Access Management (IAM) concepts commonly used in healthcare enterprises.

The environment was designed to showcase identity lifecycle management, security group administration, delegated administration, Role-Based Access Control (RBAC), emergency access account management, and Conditional Access readiness.

The project aligns with Microsoft SC-300 Identity and Access Administrator objectives and demonstrates practical implementation of IAM controls in a healthcare-focused environment.

---

# Business Scenario

Front Range Health Partners is a fictional multi-department healthcare organization.

The environment was designed to simulate how healthcare organizations structure identities, delegate administration, and secure access using Microsoft Entra ID.

Departments included:

* Radiology
* Nursing
* Physicians
* Health Information Management (HIM)
* Billing
* IT
* Contractors
* Students

---

# Environment Design

The tenant was structured using a layered IAM model:

```text
HR Roster
    ↓
Microsoft Entra ID Users
    ↓
Department Security Groups
    ↓
Administrative Units
    ↓
Scoped Administrative Roles
    ↓
Conditional Access Policies
```

This design follows the principle of least privilege and supports scalable administration.

---

# Identity Source

User identities were generated from a simulated healthcare HR roster and imported into Microsoft Entra ID.

Source File:

```text
user-roster.csv
```

The roster contains:

* Display Name
* Username
* Department
* Job Title
* Employee Type

---

# Security Groups

Department-based security groups were created to support access management and policy targeting.

| Group Name         |
| ------------------ |
| GRP-01-Radiology   |
| GRP-02-Nursing     |
| GRP-03-Physicians  |
| GRP-04-HIM         |
| GRP-05-Billing     |
| GRP-06-IT          |
| GRP-07-Contractors |
| GRP-08-Students    |

### Example: GRP-01-Radiology

Members:

* Alex Rivera
* Sarah Chen
* Michael Torres

Purpose:

Provide department-based access management for Radiology personnel.

---

# Administrative Units

Administrative Units were implemented to enable delegated administration without granting tenant-wide permissions.

| Administrative Unit |
| ------------------- |
| AU-01-Radiology     |

### Purpose

Limit administrative scope to Radiology users and resources.

### Users Assigned

* Alex Rivera
* Sarah Chen
* Michael Torres

---

# Delegated Administration

A scoped administrative model was implemented using Administrative Units.

### Scenario

A Helpdesk Administrator should only manage Radiology users.

Instead of granting tenant-wide permissions, administration is restricted to the AU-01-Radiology Administrative Unit.

### Administrative User

```text
Jamie Parker
```

### Role Assigned

```text
Helpdesk Administrator
```

### Scope

```text
AU-01-Radiology
```

### Result

Jamie Parker can perform approved helpdesk functions for Radiology users without receiving tenant-wide administrative privileges.

---

# Emergency Access (Break Glass)

Emergency access accounts were created to ensure administrative access remains available during authentication outages or Conditional Access lockout scenarios.

### Accounts Created

```text
breakglass01@tenant.onmicrosoft.com
breakglass02@tenant.onmicrosoft.com
```

### Security Controls

* Cloud-only accounts
* Excluded from Conditional Access policies
* Intended for emergency use only
* Monitored through sign-in logging
* Documented separately from standard administrative accounts

---

# Conditional Access Security Baseline

The environment was configured using Conditional Access best practices aligned with healthcare security requirements.

### Policies Created

#### CA-001 – Require MFA for Admins

Purpose:

Require Multi-Factor Authentication for privileged administrative accounts.

---

#### CA-002 – Require MFA for All Users

Purpose:

Require Multi-Factor Authentication for all standard users.

---

#### CA-003 – Block Legacy Authentication

Purpose:

Prevent sign-ins using insecure legacy authentication protocols.

---

#### CA-004 – Require MFA for Azure Management

Purpose:

Require Multi-Factor Authentication when accessing Azure management resources.

---

#### CA-005 – Require MFA Outside Trusted Locations

Purpose:

Require Multi-Factor Authentication when users access resources from locations outside trusted networks.

---

### Status

Policies configured in Report-Only mode for validation and testing before production enforcement.

---

# Trusted Network Locations

### NL-Trusted-Hospital-Network

Purpose:

Represents a trusted healthcare network location used to reduce unnecessary MFA prompts and support Conditional Access policy design.

### Configuration

* Created trusted named location
* Added approved IPv4 range
* Marked as trusted network
* Prepared for Conditional Access integration

### Status

Trusted Location Enabled

---

# Security Principles Demonstrated

### Least Privilege

Users receive only the permissions necessary to perform their responsibilities.

### Delegated Administration

Administrative responsibilities are scoped through Administrative Units rather than tenant-wide access.

### Segregation of Duties

Administrative responsibilities can be separated among different roles.

### Conditional Access Readiness

Access controls are designed before enforcement to reduce operational risk.

### Emergency Access Planning

Break Glass accounts provide a recovery mechanism during authentication or policy failures.

---

# Architecture Diagram

See:

```text
Diagrams/architecture.md
```

---

# Evidence

| Screenshot                                       |
| ------------------------------------------------ |
| 01-grp-radiology-members.png                     |
| 02-department-groups-created.png                 |
| 03-administrative-units-created.png              |
| 04-au-01-radiology-users.png                     |
| 05-au-01-radiology-helpdesk-admin-assignment.png |
| 06-break-glass-accounts-created.png              |
| 07-named-location-trusted-network.png            |
| 08-conditional-access-policy-overview.png        |
| 09-named-location-configuration.png              |
| 10-project-structure.png                         |

---

# Skills Demonstrated

* Microsoft Entra ID
* Identity Lifecycle Management
* User Administration
* Security Groups
* Administrative Units
* Delegated Administration
* Role-Based Access Control (RBAC)
* Emergency Access Account Design
* Conditional Access
* Named Locations
* Multi-Factor Authentication (MFA)
* IAM Documentation
* Healthcare IAM Architecture

---

# Lessons Learned

### Administrative Units

Administrative Units allow organizations to delegate administration without granting global administrative access.

### Role Scoping

Administrative roles can be scoped to Administrative Units, significantly reducing risk.

### Healthcare IAM Design

Department-based grouping and delegated administration closely align with healthcare operational structures.

### Conditional Access Planning

Policy design and testing should occur before enforcement to reduce business disruption.

---

# Future Enhancements

* Additional Administrative Units
* Authentication Administrator role delegation
* Groups Administrator role delegation
* Access Reviews
* Entitlement Management
* Lifecycle Workflows
* Privileged Identity Management (PIM)
* Identity Governance controls
* Conditional Access policy enforcement
* Risk-based access controls

---

# Project Structure

```text
Project 01 - Healthcare IAM Tenant
│
├── README.md
├── user-roster.csv
│
├── Diagrams
│   └── architecture.md
│
├── Documentation
│
├── Screenshots
│   ├── 01-grp-radiology-members.png
│   ├── 02-department-groups-created.png
│   ├── 03-administrative-units-created.png
│   ├── 04-au-01-radiology-users.png
│   ├── 05-au-01-radiology-helpdesk-admin-assignment.png
│   ├── 06-break-glass-accounts-created.png
│   ├── 07-named-location-trusted-network.png
│   ├── 08-conditional-access-policy-overview.png
│   ├── 09-named-location-configuration.png
│   └── 10-project-structure.png
│
└── Loom Notes
```

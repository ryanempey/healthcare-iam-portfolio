# Department Groups

## Objective

Define department-based security groups used to assign access across the healthcare organization.

## Department Security Groups

| Group Name | Department | Purpose |
|---|---|---|
| GRP-01-Radiology | Radiology | Radiology department access |
| GRP-02-Nursing | Nursing | Nursing department access |
| GRP-03-Physicians | Physicians | Provider access |
| GRP-04-HIM | Health Information Management | Medical records access |
| GRP-05-Billing | Billing | Revenue cycle access |
| GRP-06-IT | IT | IT support access |
| GRP-07-Contractors | Contractors | Temporary/vendor access |

## Application Access Groups

| Group Name | Application | Purpose |
|---|---|---|
| APP-Epic-Clinical-Users | Epic EHR | Clinical user access |
| APP-PACS-Users | PACS | Diagnostic imaging access |
| APP-Teams-Standard | Microsoft Teams | Collaboration access |
| APP-SharePoint-Department | SharePoint | Department resource access |
| APP-Billing-System-Users | Billing System | Revenue cycle access |

## Design Notes

Department groups represent organizational structure.

Application groups represent system access.

Users should be assigned through groups whenever possible instead of direct application permissions.
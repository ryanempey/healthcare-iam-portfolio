# Least Privilege Model

## Objective

Demonstrate how least privilege principles are applied within a healthcare IAM environment.

## Definition

Least privilege means users receive only the access required to perform their job duties.

Access should be:

- Role-based
- Time-bound when appropriate
- Reviewed regularly
- Removed when no longer needed

## Examples

### Radiology Technologist

Allowed:

- Epic Radiology workflows
- PACS access
- Microsoft Teams
- Department SharePoint

Not Allowed:

- Billing systems
- HR systems
- Global Administrator rights

---

### Billing Specialist

Allowed:

- Billing platform
- Epic billing functions
- Teams
- Department SharePoint

Not Allowed:

- PACS
- Clinical imaging workflows
- Administrative roles

---

### IT Helpdesk

Allowed:

- Password resets
- User account management
- Group membership management

Not Allowed:

- Global Administrator
- Security Administrator
- Privileged Role Administrator

Without approval and elevation process.

## Risk Reduction

Applying least privilege helps reduce:

- Unauthorized access
- Insider threats
- Credential abuse
- Accidental data exposure
- Compliance violations

## Healthcare Compliance Alignment

This model supports:

- HIPAA Minimum Necessary Standard
- Access Governance
- Identity Security Best Practices
- Audit Readiness

## Expected Outcome

Users receive only the access necessary to perform assigned responsibilities while reducing organizational risk.
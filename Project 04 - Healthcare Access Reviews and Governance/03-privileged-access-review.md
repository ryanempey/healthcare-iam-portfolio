# 03 – Privileged Access Review

## Objective

Validate that privileged accounts retain only the elevated permissions required to perform administrative responsibilities.

## Business Scenario

Front Range Health Partners maintains several privileged roles used to administer Microsoft Entra ID and healthcare systems.

Privileged access presents increased risk because compromise of an administrator account could result in:

- Unauthorized access changes
- Privilege escalation
- Security policy modification
- Service disruption
- Unauthorized access to healthcare resources

## Review Scope

Roles reviewed:

- Global Administrator
- Helpdesk Administrator
- Authentication Administrator
- Conditional Access Administrator
- Security Administrator

## Review Owner

Information Security Manager

Secondary Review:

- IAM Team
- IT Leadership

## Review Frequency

Quarterly

## Review Process

1. IAM exports role assignments.
2. Security leadership reviews privileged users.
3. Business justification is validated.
4. Unnecessary privileged assignments are removed.
5. Results are documented.

## Access Review Questions

- Does the user still require elevated access?
- Is the assigned role appropriate?
- Can privileges be reduced?
- Is a less privileged role available?
- Has job responsibility changed?

## Healthcare IAM Risks Addressed

| Risk | Mitigation |
|---|---|
| Privilege escalation | Quarterly privileged review |
| Excessive administrative access | Least privilege validation |
| Insider threat | Manager approval and review |
| Unauthorized changes | Role certification |

## Security Principles Demonstrated

- Least Privilege
- Separation of Duties
- Role Certification
- Administrative Governance
- Zero Trust

## Expected Outcome

Only authorized personnel retain privileged access required for their job responsibilities.

## Compliance Considerations

- HIPAA Security Rule
- Administrative Safeguards
- Audit Readiness
- Access Governance

## Evidence

Privileged role reports and review approvals would be retained for audit purposes.
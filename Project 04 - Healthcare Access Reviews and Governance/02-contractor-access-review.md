# 02 – Contractor Access Review

## Objective

Validate that contractors retain only the access necessary to perform their assigned responsibilities.

## Business Scenario

Front Range Health Partners uses contractors for:

- IT Support
- Imaging Equipment Maintenance
- Application Support
- Clinical System Upgrades

Contractor access presents elevated risk because individuals are not direct employees and may have temporary assignments.

## Review Scope

Groups reviewed:

- GRP-07-Contractors
- Vendor Support Groups
- Temporary Project Groups

## Review Owner

Contract Sponsor

Secondary Review:

- Information Security
- IAM Team

## Review Frequency

Quarterly

## Review Process

1. IAM exports contractor accounts.
2. Contract sponsor validates active engagement.
3. Access requirements are reviewed.
4. Expired contractor access is removed.
5. Results are documented.

## Access Review Questions

- Is the contractor still actively engaged?
- Is access still required?
- Does the contractor require all assigned permissions?
- Has the contract expired?
- Should access be removed?

## Healthcare IAM Risks Addressed

| Risk | Mitigation |
|---|---|
| Former contractor access | Quarterly review |
| Excessive vendor permissions | Least privilege validation |
| PHI exposure | Access justification review |
| Compliance violations | Contract sponsor approval |

## Expected Outcome

Only active contractors retain approved access to healthcare systems and organizational resources.

## Compliance Considerations

- HIPAA
- Vendor Access Governance
- Minimum Necessary Access Principle
- Audit Readiness

## Evidence

Documented review results and contractor access reports would be retained for audit purposes.
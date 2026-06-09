# 01 – Quarterly Access Review

## Objective

Validate that department users retain only the access required for their current role.

## Business Scenario

Front Range Health Partners performs quarterly access reviews to reduce excessive access and support healthcare compliance requirements.

The IAM team reviews department security groups to confirm that users still require access.

## Review Scope

Groups reviewed:

- GRP-01-Radiology
- GRP-02-Nursing
- GRP-03-Physicians
- GRP-04-HIM
- GRP-05-Billing

## Review Owner

Department Manager

## Review Frequency

Quarterly

## Review Process

1. IAM exports group membership.
2. Department manager reviews access.
3. Manager approves valid users.
4. Manager flags users who no longer need access.
5. IAM removes unnecessary group memberships.
6. Review results are documented for audit evidence.

## Access Review Questions

- Does this user still work in this department?
- Does this user still need this access?
- Has this user changed roles?
- Is this access appropriate for their job title?
- Should access be removed?

## Healthcare IAM Risks Addressed

| Risk | Mitigation |
|---|---|
| Access creep | Quarterly manager review |
| Excessive permissions | Remove unnecessary group memberships |
| Orphaned access | Validate active users |
| Compliance gaps | Maintain audit evidence |

## Expected Outcome

Department access remains aligned with current job responsibilities and least-privilege principles.

## Evidence

Documented review results and group membership exports would be retained for audit purposes.
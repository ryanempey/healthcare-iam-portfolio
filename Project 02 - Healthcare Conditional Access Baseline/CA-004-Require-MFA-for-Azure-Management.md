# CA-004 – Require MFA for Azure Management

## Objective

Require Multifactor Authentication for all access to Azure management resources.

## Business Justification

Azure management interfaces provide administrative control over cloud resources and identity infrastructure.

Compromise of an administrative session could result in:

- Unauthorized role assignments
- Security policy changes
- Resource deletion
- Privilege escalation
- Service disruption

## Assignments

### Users

Included:

- All Users

Excluded:

- BreakGlass01
- BreakGlass02

## Cloud Apps

Included:

- Microsoft Azure Management

## Conditions

None

## Access Controls

Grant Access:

- Require Multifactor Authentication

## Policy State

Report-only

## Expected Outcome

All users accessing Azure management resources must complete MFA before gaining access.

## Healthcare Considerations

Administrative access to healthcare systems often contains privileged access to identity, security, and operational resources.

Protecting Azure management interfaces helps reduce the risk of unauthorized administrative activity.

## Screenshots

Placeholder for policy screenshots.
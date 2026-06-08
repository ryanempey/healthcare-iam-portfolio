# CA-005 – Require MFA Outside Trusted Locations

## Objective

Require Multifactor Authentication when users access Microsoft resources from outside trusted organizational networks.

## Business Justification

Users connecting from unknown locations present increased identity risk.

Requiring MFA for external access helps reduce the likelihood of unauthorized access due to:

- Credential theft
- Phishing attacks
- Session hijacking
- Unauthorized remote access

## Assignments

### Users

Included:

- All Users

Excluded:

- BreakGlass01
- BreakGlass02

## Cloud Apps

All Cloud Apps

## Conditions

### Locations

Included:

- Any Location

Excluded:

- Trusted Hospital Network
- Corporate Office Network

## Access Controls

Grant Access:

- Require Multifactor Authentication

## Policy State

Report-only

## Expected Outcome

Users connecting from outside trusted locations must complete MFA before accessing Microsoft resources.

## Healthcare Considerations

Trusted hospital networks may include:

- Main hospital campus
- Imaging centers
- Administrative offices

Named Locations should be reviewed regularly to ensure accuracy.

## Screenshots

Placeholder for policy screenshots.
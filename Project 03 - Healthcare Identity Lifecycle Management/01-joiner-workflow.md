# 01 – Joiner Workflow

## Objective

Provision secure access for newly hired healthcare employees while maintaining least-privilege access principles.

---

## Business Scenario

Front Range Health Partners hires a new Registered Nurse for the Emergency Department.

The nurse requires access to clinical and collaboration systems before their first shift.

Required access includes:

- Microsoft 365
- Microsoft Teams
- Exchange Online
- Epic Electronic Health Record (EHR)
- PACS Viewer
- SharePoint

The IAM team must ensure all access is provisioned prior to the employee start date while maintaining least-privilege access principles and HIPAA compliance.

---

## Trigger

Human Resources enters a new employee record into the HR system.

---

## Workflow

### Step 1 – HR Creates Employee Record

Required Information:

- Legal Name
- Employee ID
- Department
- Manager
- Job Title
- Start Date
- Employment Status

---

### Step 2 – Identity Creation

IAM automatically creates:

- Entra ID Account
- User Principal Name
- Mailbox
- Employee Profile

Example:

jane.smith@fronthrangehealth.org

---

### Step 3 – Group Assignment

Employee is assigned to:

- Nursing Staff
- Emergency Department
- Clinical Applications
- MFA Required Users

---

### Step 4 – License Assignment

Assign:

- Microsoft 365 E3
- Teams
- Exchange Online

---

### Step 5 – Application Access

Access granted through security groups:

| Application | Access Type |
|------------|-------------|
| Epic EHR | Clinical User |
| PACS Viewer | Diagnostic Image Access |
| Microsoft Teams | Collaboration |
| SharePoint | Department Resources |
| Exchange Online | Email |

Access is assigned through role-based groups rather than direct user permissions.

---

### Step 6 – Security Controls

Apply:

- Conditional Access Policies
- MFA Registration
- Password Policies

---

### Step 7 – Manager Verification

Manager verifies:

- Correct department
- Correct applications
- Correct role assignments

---

### Step 8 – Day One Readiness

User can:

- Sign in
- Access required applications
- Complete MFA registration

---

## Security Considerations

- HIPAA minimum necessary access
- Least privilege access model
- MFA enforcement
- Conditional Access enforcement
- Role-based access control (RBAC)
- Group-based access management
- Manager approval validation

---

## Expected Outcome

New employees receive required access before their start date while minimizing security risk.

---

## IAM Concepts Demonstrated

- Identity Provisioning
- RBAC
- Group-Based Access
- Conditional Access
- Access Governance

---

## Healthcare IAM Risks Addressed

| Risk | Mitigation |
|--------|------------|
| Excessive Access | RBAC and Group Assignments |
| Shared Credentials | Individual Identity Provisioning |
| Unauthorized Access | MFA Enforcement |
| Orphaned Accounts | Lifecycle Management |
| Compliance Violations | Manager Verification |

## Screenshots

Placeholder for workflow diagrams.

# Wild Rift

**Target:** WR.010.001

---

- [ ] [Project Homepage](project-homepage.md)
- [ ] [Authentication](authentication.md)
- [ ] [Exam Paper Scanner](exam-paper-scanner.md)
- [ ] [Result Processing](result-processor.md)
- [ ] [Exam Analytics](exam-analytics.md)
- [ ] [Feedback Management](feedback-provider.md)
- [ ] [Notification Alert](notification.md)

---
# Authentication – Sign In

Project Homepage > Authentication > Sign In

---

## Module Description

The Sign In module allows registered users to securely access the Tuon system using their email and password credentials.

The system verifies user identity and assigns role-based access control (Administrator, Instructor, or Student).

---

## Inputs

- Email Address
- Password

---

## Outputs

- Successful login → Redirect to Dashboard
- Failed login → Error message displayed

---

## Validation Rules

- Email must exist in database.
- Password must match stored encrypted password.
- Account must not be deactivated.

---

## Error Handling

- "Invalid email or password"
- "Account not found"
- "Account is disabled"

---

## Use Case Scenario

### Actor:
Registered User (Admin / Instructor / Student)

### Pre-condition:
User must already have a registered account.

### Main Flow:

| Step | Action |
|------|--------|
| 1 | User navigates to Sign In page |
| 2 | User enters email and password |
| 3 | User clicks Login button |
| 4 | System validates credentials |
| 5 | System redirects to dashboard |

© 2026 Hasa

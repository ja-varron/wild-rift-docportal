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

### Alternative Flow:

| Step | Condition | Action |
|------|------------|--------|
| 3A | Invalid credentials | System displays error message |
| 3B | Account disabled | System blocks access |

---

## Security Considerations

- Passwords stored using hashing (bcrypt).
- HTTPS encryption required.
- Session token generated upon successful login.

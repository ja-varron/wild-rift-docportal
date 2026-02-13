# Authentication – Sign In

Project Homepage > Authentication > Sign In

---

## 1. Module Overview

The Sign In module allows registered users to securely access the Tuon system using their email and password credentials.

This module ensures:
- Secure authentication of users
- Role-based access control
- Protection of system data
- Encrypted password validation
- Session management using secure tokens

Only users with valid accounts (Administrator, Instructor, or Student) can log in.

---

## 2. Actors

- Administrator
- Instructor
- Student

---

## 3. Pre-Conditions

- User must already have a registered account.
- User account must be active.
- User must access the system via HTTPS connection.

---

## 4. Post-Conditions

- Successful authentication generates a secure session.
- User is redirected to their respective dashboard.
- Login attempt is recorded in the system logs.

---

## 5. Inputs

| Field Name | Type | Required | Description |
|------------|------|----------|-------------|
| Email | Text | Yes | Registered email address |
| Password | Password | Yes | User’s encrypted password |

---

## 6. Outputs

### Success Response
- Redirect to dashboard
- Session token generated
- Role-based interface loaded

### Error Response
- "Invalid email or password"
- "Account not found"
- "Account is disabled"

---

## 7. Validation Rules

1. Email must follow proper email format.
2. Email must exist in the database.
3. Password must match encrypted password stored in database.
4. Account must be marked as active.
5. Maximum 5 failed login attempts before temporary lock.

---

## 8. Business Rules

- Passwords are stored using hashing algorithm (e.g., bcrypt).
- System must use HTTPS encryption.
- Session expires after 2 hours of inactivity.
- Only authenticated users can access protected modules.

---

## 9. Main Use Case Scenario

### Primary Actor:
Registered User (Admin / Instructor / Student)

### Main Flow:

| Step | System/User Action |
|------|--------------------|
| 1 | User navigates to Sign In page |
| 2 | User enters email and password |
| 3 | User clicks "Login" button |
| 4 | System validates input format |
| 5 | System verifies credentials in database |
| 6 | System generates secure session token |
| 7 | System redirects user to dashboard |

---

## 10. Alternative Flows

### A1 – Invalid Credentials

| Step | Condition | Action |
|------|------------|--------|
| 5A | Email not found | Display "Invalid email or password" |
| 5B | Password incorrect | Display "Invalid email or password" |

---

### A2 – Account Disabled

| Step | Condition | Action |
|------|------------|--------|
| 5C | Account inactive | Display "Account is disabled. Contact administrator." |

---

### A3 – Too Many Failed Attempts

| Step | Condition | Action |
|------|------------|--------|
| 5D | 5 failed attempts | Lock account temporarily for 15 minutes |

---

## 11. Security Considerations

- Passwords must never be stored in plain text.
- Use hashing algorithm (bcrypt).
- JWT token or secure session ID must be generated.
- Session timeout after inactivity.
- Prevent SQL injection using parameterized queries.
- Implement brute-force protection.

---

## 12. Non-Functional Requirements

| Category | Requirement |
|----------|-------------|
| Performance | Login response time must be under 2 seconds |
| Security | Must comply with data privacy standards |
| Reliability | 99% system availability |
| Usability | Clear error messages displayed |

---

## 13. Related Modules

- Authentication – Sign Up
- Authentication – Forgot Password
- Dashboard Module
- Role-Based Access Control

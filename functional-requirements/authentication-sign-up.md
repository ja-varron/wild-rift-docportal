# Wild Rift

**Target:** WR.010.001

---

### 📑 Site Map

- [ ] [Project Homepage](project-homepage.md)
- [ ] [Authentication](/functional-requirements/authentication.md)
- [ ] [Exam Paper Scanner](/functional-requirements/exam-paper-scanner.md)
- [ ] [Result Processing](/functional-requirements/result-processor.md)
- [ ] [Exam Analytics](/functional-requirements/exam-analytics.md)
- [ ] [Feedback Management](/functional-requirements/feedback-provider.md)
- [ ] [Notification Alert](/functional-requirements/notification.md)

---

# Authentication – Sign Up

Project Homepage > Authentication > Sign Up

---

## 1. Module Overview

The Sign Up module allows new users to create an account in the system.

This module ensures:
- Secure registration of users
- Proper role assignment
- Data validation and sanitization
- Encrypted password storage
- Prevention of duplicate accounts

Only authorized roles (Administrator, Instructor, Student) can be registered depending on system configuration.

---

## 2. Actors

- Administrator
- Instructor
- Student

---

## 3. Pre-Conditions

- User must not already have a registered account.
- Email address must be unique.
- Required registration fields must be completed.

---

## 4. Post-Conditions

- New user account is stored in the database.
- Password is securely hashed.
- User account is created as active (or pending approval if required).
- Confirmation message is displayed.

---

## 5. Inputs

| Field Name   | Type     | Required | Description |
|--------------|----------|----------|-------------|
| Full Name    | Text     | Yes      | User's complete name |
| Email        | Email    | Yes      | Unique email address |
| Password     | Password | Yes      | User password |
| Confirm Password | Password | Yes | Must match password |
| Role         | Dropdown | Yes      | Admin / Instructor / Student |

---

## 6. Outputs

### Success Response
- "Account successfully created"
- Redirect to Sign In page
- Optional: Email verification sent

### Error Response
- "Email already exists"
- "Passwords do not match"
- "Invalid input format"

---

## 7. Main Use Case Scenario

### Primary Actor:
New User

### Main Flow:

| Step | System/User Action |
|------|--------------------|
| 1 | User navigates to Sign Up page |
| 2 | User enters required details |
| 3 | User selects role |
| 4 | User clicks "Register" button |
| 5 | System validates inputs |
| 6 | System checks for duplicate email |
| 7 | System hashes password |
| 8 | System saves user to database |
| 9 | System displays success message |
| 10 | User is redirected to Sign In page |

---

© 2026 Hasa


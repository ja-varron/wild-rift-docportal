# Wild Rift

**Target:** WR.010.001

## Notification Alert

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

### 📋 Functional Requirements

- [ ] The system shall generate a notification after an instructor finalizes exam results.
- [ ] The notification shall be sent to students via email.
- [ ] The notification shall include the exam title and a summary of the results.
- [ ] Only students who took the exam shall receive the notification.
- [ ] The system shall log all sent notifications for auditing purposes.

---

### 🧩 Use Case Scenario


**Actor:** System (triggered by instructor action)

**Precondition:** Instructor has finalized the exam results.

**Steps:**
1. Instructor finalizes the exam results in the system.
2. The system generates a notification containing the exam title and result summary.
3. The system sends the notification to each student via email.
4. The system logs the notification event for record-keeping.
5. Students receive the notification and can view their result summary.

**Postcondition:** All students are notified via email with the exam title and result summary after results are finalized.

---

### 🛠️ Quick Actions

- [ ] View Sent Notifications
- [ ] Resend Notification
- [ ] Download Notification Log
- [ ] Return to Exam List

---

© 2026 Hasa
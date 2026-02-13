# Wild Rift

**Target:** WR.010.001

## Result Processing

---

### 📑 Site Map
- [ ] [Project Homepage](project-homepage.md)
- [ ] [Authentication](authentication.md)
- [ ] [Exam Paper Scanner](exam-paper-scanner.md)
- [ ] [Result Processing](result-processor.md)
- [ ] [Exam Analytics](exam-analytics.md)
- [ ] [Feedback Management](feedback-provider.md)
- [ ] [Notification Alert](notification.md)

---

### 📋 Functional Requirements

- [ ] The system shall compare scanned answers with the stored answer keys.
- [ ] The system shall automatically compute the total score for each exam paper.
- [ ] The system shall compute per-topic scores based on the answer key mapping.
- [ ] The computed results shall be stored securely in the database.
- [ ] The process shall be automated and require minimal manual intervention.

---

### 🧩 Use Case Scenario

**Actor:** System (triggered by instructor or automatically after scanning)

**Precondition:** Scanned exam papers and corresponding answer keys are available in the system.

**Steps:**
1. The system retrieves scanned answers from the uploaded exam papers.
2. The system fetches the corresponding stored answer keys.
3. The system compares each scanned answer to the answer key.
4. The system calculates the total score for the exam paper.
5. The system calculates per-topic scores based on the answer key mapping.
6. The system stores the computed results in the database.
7. The instructor is notified that results are available.

**Postcondition:** Exam results (total and per-topic scores) are computed and stored in the database.

---

### 🛠️ Quick Actions

- [ ] Start Result Processing
- [ ] View Computed Scores
- [ ] Download Results Report
- [ ] Notify Instructor
- [ ] Reprocess Exam Paper

---

© 2026 Hasa
# Salesforce Summer Program – Day 5  
## Apex Introduction

## 📌 What is Apex?

Apex is Salesforce’s programming language used to add custom business logic inside the Salesforce platform. It is similar to Java and is specially designed for CRM-related operations and database interactions.

Salesforce provides many no-code tools like Flows and Process Builder, but some business requirements become too complex. Apex helps developers build advanced automation, validations, integrations, and custom operations that cannot be achieved using only clicks and configuration.

### Key Features of Apex
- Object-oriented programming language
- Runs on Salesforce servers
- Supports database operations using SOQL and DML
- Used for Triggers, Classes, Controllers, and Integrations
- Helps automate complex business logic

---

# 🔄 Flow vs Apex

| Feature | Flow (Declarative) | Apex (Programmatic) |
|---|---|---|
| Development Type | No-code / Low-code | Coding |
| Ease of Use | Easy for admins | Requires programming |
| Best For | Simple automation | Complex logic |
| Performance | Good for basic tasks | Better for advanced operations |
| Flexibility | Limited | Highly flexible |
| External Integrations | Limited | Strong support |
| Error Handling | Basic | Advanced |
| Maintenance | Easier | Requires developers |

---

# ⚙️ Configuration vs Coding

| Configuration | Coding |
|---|---|
| Uses clicks and setup tools | Uses programming language |
| Faster for simple tasks | Better for advanced requirements |
| Less technical knowledge needed | Requires developer skills |
| Easier maintenance | More customizable |
| Limited logic capability | Unlimited business logic possibilities |

### Example
- Configuration: Create a Flow to send welcome emails.
- Coding: Build complex admission eligibility calculation using Apex.

---

# 💡 Real Examples Where Apex Is Needed

## 1. Complex Fee Calculation
A college may calculate fees based on:
- Scholarship percentage
- Attendance
- Course type
- Hostel facilities
- Late payment penalties

This logic becomes too complicated for normal Flows. Apex can efficiently manage these calculations.

---

## 2. Integration with External Payment System
Suppose the College Management System must connect with:
- Razorpay
- Stripe
- Banking APIs

Flows have limitations for secure API handling and advanced processing. Apex enables secure external integrations and response handling.

---

## 3. Advanced Eligibility Logic
Example:
- Student must have minimum attendance
- No pending fee dues
- Required prerequisite subjects completed
- GPA above cutoff

This involves multiple object checks and conditional processing. Apex handles such advanced logic effectively.

---

# 🏫 Integrated College Management System Design

## 📌 CRM Functionality
The College Management System acts as a CRM by managing:
- Student admissions
- Course registrations
- Faculty management
- Notifications
- Attendance tracking

---

## 📌 Objects Used

| Object | Purpose |
|---|---|
| Student | Stores student details |
| Course | Stores course information |
| Faculty | Stores faculty information |
| Admission | Tracks admission process |
| Attendance | Maintains attendance records |

---

## 📌 Relationships

| Relationship | Description |
|---|---|
| Student ↔ Course | Many students can enroll in courses |
| Faculty ↔ Course | Faculty teaches courses |
| Student ↔ Attendance | Attendance linked to each student |

---

## 📌 Validation Rules

### Example Validations
- Email field cannot be empty
- Phone number must contain 10 digits
- Attendance cannot exceed 100%
- Course seats cannot go below zero

---

## 📌 Formula Fields

### Example Formula

```text
Total_Seats - Filled_Seats
```

Used to automatically calculate available seats.

---

## 📌 Flow Automation

### Example Flows
- Send admission confirmation email
- Notify students about attendance shortage
- Auto-create student ID after admission
- Alert faculty when seats are full

---

## 📌 Apex Usage

### Example Apex Business Logic
- Advanced eligibility checking
- Fee calculations
- API integrations
- Bulk admission processing
- Exception handling

Apex adds flexibility where Flows become insufficient.

---

# 🧠 Apex Thinking Exercise

## Case 1 — Complex Fee Structure
### Why Flow is not enough:
Too many nested conditions and calculations.

### Why Apex is needed:
Apex can efficiently process multiple calculations and conditions.

---

## Case 2 — External Payment Gateway Integration
### Why Flow is not enough:
Secure API calls and response parsing are difficult in Flow.

### Why Apex is needed:
Apex supports HTTP callouts and secure integrations.

---

## Case 3 — Smart Admission Eligibility System
### Why Flow is not enough:
Requires checking data from multiple related objects with complex rules.

### Why Apex is needed:
Apex can implement advanced business decision logic.

---

# 📝 Pseudocode Examples

## Example 1 — Seat Availability

```text
IF available seats = 0
THEN block student registration
ELSE allow admission
```

---

## Example 2 — Attendance Alert

```text
IF attendance < 75%
THEN send warning notification to student
```

---

## Example 3 — Fee Due Notification

```text
IF fee payment is pending
THEN send reminder email
```

---

# 🤔 Reflection

## Why can’t all enterprise logic be built using only clicks and configuration?

Enterprise systems often involve:
- Complex business rules
- External integrations
- Large-scale data processing
- Dynamic calculations
- Advanced validations
- Security requirements

No-code tools like Flows are excellent for simple automation, but they have limitations when handling highly customized and scalable enterprise requirements.

Programming languages like Apex provide:
- Better flexibility
- Advanced logic handling
- Greater control
- Reusability
- Efficient performance

That is why enterprise applications eventually require custom programming along with declarative tools.

---

# ✍️ Reflective Questions

## 1. Why is Apex needed if Salesforce already has Flows?
Flows are useful for basic automation, but Apex is needed for complex logic, integrations, and advanced processing.

---

## 2. When should developers prefer no-code solutions?
Developers should prefer no-code solutions when requirements are simple, maintainable, and achievable without custom code.

---

## 3. What problems require custom programming?
Problems involving:
- Complex calculations
- API integrations
- Advanced validations
- Bulk processing
- Dynamic logic

require custom programming.

---

## 4. Why is business logic important in enterprise systems?
Business logic ensures that company rules, workflows, and operations function correctly and consistently.

---

## 5. Why should developers avoid unnecessary coding?
Unnecessary coding increases maintenance complexity, debugging effort, and technical debt.

---

## 6. How does programming increase flexibility?
Programming allows developers to create customized solutions tailored to specific business requirements.

---

# ✅ Day 5 Learning Outcome

By completing Day 5, I understood:
- What Apex is
- Why Salesforce requires programming
- Difference between declarative and programmatic development
- How Flows and Apex work together
- How enterprise business logic is implemented
- How all Salesforce concepts connect in a real-world CRM system

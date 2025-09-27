# 📚 Online Education Database System

## 📖 Overview
The **Online Education Database System** is a relational database project designed to manage users, courses, enrollments, lessons, assessments, payments, discounts, and interactions in an online learning platform.  
It is implemented in **Oracle SQL & PL/SQL**, with features such as stored procedures, triggers, cursors, error handling, and sample datasets.

---

## 🗄️ Database Schema

### Entities & Tables
- **Users** – Stores student, instructor, and admin details.  
- **Courses** – Contains course metadata (instructor, duration, enrollment dates).  
- **Modules & Lessons** – Structured breakdown of course content.  
- **Content** – Lesson materials (videos, documents, etc.) with versioning.  
- **UserEnrollments** – Tracks which students are enrolled in which courses.  
- **Assessments** – Quizzes, assignments, or tests linked to lessons.  
- **UserAssessmentAttempts** – Student submissions with scores.  
- **UserInteractions** – Logs activity like viewing or completing content.  
- **Forums, Threads & Posts** – Course-level discussion forums.  
- **Payments & Discounts** – Course purchase transactions and discount codes.  
- **UserDiscounts** – Tracks applied discount codes per user.

---

## ⚙️ PL/SQL Components

### 🔹 Procedures
1. **CreateUser** – Registers a new user with hashed password and validation.  
2. **EnrollUserInCourse** – Enrolls users only within valid course enrollment dates.  
3. **SubmitAssessment** – Records a student’s assessment attempt with validations.  
4. **ProcessPayment** – Processes payments, applies discounts, and updates enrollment status.

### 🔹 Functions
1. **CalculateDiscountedPrice** – Computes discounted course price for a user.  
2. **GetUserRoleDescription** – Returns role description (`Student`, `Instructor`, `Administrator`).  
3. **CalculateCourseProgress** – Computes a student’s progress based on lessons & assessments.

### 🔹 Cursors
1. **CourseEnrollmentCursor** – Lists all students enrolled in a course.  
2. **TopPerformersCursor** – Fetches top scorers in a course.  
3. **PendingAssessmentsCursor** – Finds due assessments for a student.  
4. **RecentActivityCursor** – Returns recent interactions of a user.

### 🔹 Exception Handling
- **DuplicateEmailException** – Prevents duplicate registrations.  
- **EnrollmentClosedException** – Ensures enrollment occurs within allowed dates.  
- **AssessmentDueDateViolationException** – Prevents late submissions.  
- **PaymentFailureException** – Handles payment errors.

---

## 🔔 Triggers
1. **ContentVersionTrigger** – Auto-increments content version on updates.  
2. **EnrollmentClosureTrigger** – Prevents enrollment outside allowed dates.  
3. *(Optional)* **ForumThreadCreationTrigger** – Auto-creates forum threads when posts are made (commented out for flexibility).

---

## 🧑‍💻 Sample Data
Sample inserts are provided for:
- Users (`Student`, `Instructor`, `Administrator`)  
- Courses (e.g., *Introduction to Programming*, *Web Development Fundamentals*)  
- Modules, Lessons, Content (Python basics, data types, etc.)  
- Enrollments & Payments  
- Assessments & Attempts  
- Forums, Threads, and Posts  
- Discounts & Applied User Discounts  

---

## 🚀 Features
- **Role-based system** – Students, instructors, administrators.  
- **Course lifecycle management** – From creation to enrollment closure.  
- **Lesson tracking** – With modules, lessons, content, and version control.  
- **Assessment system** – Supports quizzes, assignments, and grading.  
- **Payment integration** – Supports discounts and payment tracking.  
- **Forum discussions** – Community-driven learning.  
- **User progress tracking** – Combines lesson completion + assessments.  

---

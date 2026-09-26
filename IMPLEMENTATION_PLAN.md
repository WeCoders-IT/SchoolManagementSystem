# School Management System - Project Issue Hierarchy

> Structure:
>
> **Epic → Feature → Task**

---

# Epic: Phase 0 – Project Preparation & Planning

## Feature: Project Setup & Planning

### Tasks

- [ ] Create GitHub repository
- [ ] Define project README
- [ ] Agree on coding standards & naming conventions
- [ ] Define MVP scope
- [ ] Decide Git branching strategy
- [ ] Create GitHub Project board with phases as columns

---

# Epic: Phase 1 – Project Setup & Authentication

## Feature: Application Foundation & Infrastructure

### Tasks

- [ ] Create ASP.NET Core MVC project (Individual Accounts)
- [ ] Configure SQL Server connection
- [ ] Apply initial EF Core migration
- [ ] Setup layout (_Layout.cshtml)

## Feature: Authentication & Role-Based Access Control

### Tasks

- [ ] Configure ASP.NET Identity
- [ ] Create roles (Admin, Teacher, Student, Parent)
- [ ] Seed roles on application startup
- [ ] Create admin user seeding logic
- [ ] Implement role-based navigation menu
- [ ] Protect controllers with [Authorize]

---

# Epic: Phase 2 – Academic Year Management

## Feature: Academic Year Management

### Tasks

- [ ] Create AcademicYear entity
- [ ] Add AcademicYear DbSet to DbContext
- [ ] Create EF Core migration
- [ ] AcademicYear CRUD controller
- [ ] AcademicYear CRUD views
- [ ] Make academic year selectable only by Admin

## Feature: Active Academic Year Governance

### Tasks

- [ ] Create AcademicYearService
- [ ] Implement GetActiveAcademicYear()
- [ ] Enforce “only one active year” rule
- [ ] Prevent deleting academic year with dependent data

---

# Epic: Phase 3 – Core People Management

## Feature: Student Management

### Tasks

- [ ] Create Student entity
- [ ] Link Student to Identity User
- [ ] Student CRUD controller
- [ ] Student CRUD views
- [ ] Activate / deactivate student
- [ ] Auto-generate student number
- [ ] Validation (unique student number)

## Feature: Parent Management & Student Association

### Tasks

- [ ] Create Parent entity
- [ ] Link Parent to Identity User
- [ ] Parent CRUD controller
- [ ] Parent CRUD views
- [ ] Implement parent–student many-to-many relation
- [ ] UI to assign students to parents
- [ ] Restrict parent access to own children

## Feature: Teacher Management

### Tasks

- [ ] Create Teacher entity
- [ ] Link Teacher to Identity User
- [ ] Teacher CRUD controller
- [ ] Teacher CRUD views

---

# Epic: Phase 4 – School Structure (Classes, Subjects, Rooms)

## Feature: Class Management

### Tasks

- [ ] Create Class entity (grade + section)
- [ ] Class CRUD controller
- [ ] Class CRUD views
- [ ] Validation for duplicate class/section

## Feature: Subject Management

### Tasks

- [ ] Create Subject entity
- [ ] Subject CRUD controller
- [ ] Subject CRUD views

## Feature: Room Management

### Tasks

- [ ] Create Room entity
- [ ] Room CRUD controller
- [ ] Room CRUD views
- [ ] Room capacity and type validation
- [ ] Enable/disable room availability

---

# Epic: Phase 5 – School Hours & Timetable

## Feature: Time Slot Management

### Tasks

- [ ] Create TimeSlot entity
- [ ] TimeSlot CRUD controller
- [ ] TimeSlot CRUD views
- [ ] Validate overlapping time slots

## Feature: Timetable & Schedule Management

### Tasks

- [ ] Create ClassSchedule entity
- [ ] Add relations (Class, Subject, Teacher, Room, TimeSlot, AcademicYear)
- [ ] ClassSchedule CRUD controller
- [ ] Weekly timetable UI (grid view)
- [ ] Filter schedules by class
- [ ] Filter schedules by teacher
- [ ] Filter schedules by room
- [ ] Validate room conflicts
- [ ] Validate teacher conflicts
- [ ] Restrict scheduling to active academic year
- [ ] Read-only schedules for past academic years

---

# Epic: Phase 6 – Enrollment (Per Academic Year)

## Feature: Student Enrollment Management

### Tasks

- [ ] Create Enrollment entity
- [ ] Enrollment CRUD controller
- [ ] Enroll student into class for academic year
- [ ] Prevent duplicate enrollment same year
- [ ] View enrolled students per class
- [ ] Admin-only enrollment management

---

# Epic: Phase 7 – Attendance

## Feature: Lesson-Based Attendance Recording

### Tasks

- [ ] Update Attendance entity to reference ClassSchedule
- [ ] Attendance marking UI for teachers
- [ ] Attendance per date validation
- [ ] Prevent attendance for unscheduled lessons

## Feature: Attendance Visibility

### Tasks

- [ ] Student attendance view
- [ ] Parent attendance view

## Feature: Attendance Reporting & Analytics

### Tasks

- [ ] Admin attendance reports
- [ ] Attendance summary calculations

---

# Epic: Phase 8 – Exams & Grades

## Feature: Exam Management

### Tasks

- [ ] Create Exam entity
- [ ] Link Exam to Subject
- [ ] Link Exam to Academic Year
- [ ] Exam CRUD controller
- [ ] Exam CRUD views
- [ ] Prevent editing exams in past years

## Feature: Grade Management & Reporting

### Tasks

- [ ] Create Grade entity
- [ ] Grade entry UI for teachers
- [ ] Score validation (0–MaxScore)
- [ ] Calculate averages
- [ ] Student grade report view
- [ ] Parent grade report view

---

# Epic: Phase 9 – Dashboards

## Feature: Admin Dashboard

### Tasks

- [ ] Active academic year display
- [ ] Student / teacher counts
- [ ] Attendance summary

## Feature: Teacher Dashboard

### Tasks

- [ ] Today’s schedule
- [ ] Classes taught
- [ ] Attendance shortcuts

## Feature: Student Dashboard

### Tasks

- [ ] Weekly timetable
- [ ] Attendance summary
- [ ] Grade overview

## Feature: Parent Dashboard

### Tasks

- [ ] Children list
- [ ] Attendance overview
- [ ] Grade overview

---

# Epic: Phase 10 – Security, Validation & Polish

## Feature: Validation & Data Integrity

### Tasks

- [ ] Add DataAnnotations across entities
- [ ] Input validation
- [ ] Historical data protection

## Feature: Security & Authorization Hardening

### Tasks

- [ ] Global exception handling
- [ ] Anti-forgery validation
- [ ] Authorization review for all controllers

## Feature: User Experience & Accessibility Improvements

### Tasks

- [ ] UI consistency cleanup
- [ ] Improve error messages
- [ ] Accessibility basics (labels, validations)

---

# Epic: Phase 11 – Testing, Refactor & Documentation

## Feature: System Testing & Verification

### Tasks

- [ ] Manual test all user roles
- [ ] Test academic year switching
- [ ] Test schedule conflict scenarios
- [ ] Fix identified issues

## Feature: Application Architecture Refactoring

### Tasks

- [ ] Refactor controllers → services
- [ ] Clean up unused code
- [ ] Improve maintainability

## Feature: Documentation & Developer Onboarding

### Tasks

- [ ] Write basic developer documentation
- [ ] Update README with setup instructions
- [ ] Create setup documentation
- [ ] Create architecture documentation

---

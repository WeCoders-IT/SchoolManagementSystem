# ✅ School Management System – Development Plan

## 🎯 Project Overview
This project is a **School Management System** built with **ASP.NET Core MVC** for a **small high school**.
The goal is to serve as a **learning project** while following **real-world architecture and workflows**.

### Key Features
- Role-based access (Admin, Teacher, Student, Parent)
- Academic Year–based data isolation
- Students, Parents, Teachers management
- Classes, Subjects, Rooms
- Weekly timetable with hours & rooms
- Student enrollment per academic year
- Attendance per scheduled lesson
- Exams & grades
- Role-based dashboards

---

## Tech Stack
- ASP.NET Core MVC
- Entity Framework Core
- SQL Server
- ASP.NET Identity
- Razor Views + Bootstrap
- GitHub Projects (Kanban)

---

## Development Phases & Tasks

---

## 🧱 Phase 0 – Project Preparation & Planning

**Goal:** Establish shared understanding and repository structure

### Tasks
- Create GitHub repository
- Add README with project scope and tech stack
- Define MVP scope (features in/out)
- Define coding standards and naming conventions
- Decide Git branching strategy (main / develop / feature)
- Create GitHub Project board
- Add labels (`backend`, `frontend`, `database`, `critical`, etc.)

---

## 🏗 Phase 1 – Project Setup & Authentication

**Goal:** Running application with secure login and role-based access

### Tasks
- Create ASP.NET Core MVC project (Individual Accounts)
- Configure SQL Server connection
- Setup Entity Framework Core
- Apply initial migration
- Configure ASP.NET Identity
- Create roles: Admin, Teacher, Student, Parent
- Seed roles on application startup
- Seed default Admin user
- Setup base layout (`_Layout.cshtml`)
- Implement role-based navigation menu
- Protect controllers using `[Authorize]`

**Deliverable:** Users can log in and see role-aware navigation

---

## 📅 Phase 2 – Academic Year Management

**Goal:** Academic Year drives all academic data

### Tasks
- Create `AcademicYear` entity
- Add DbSet to DbContext
- Create EF Core migration
- Academic Year CRUD controller
- Academic Year CRUD views
- Enforce only one active academic year
- Prevent deleting academic year with dependent data
- Create `AcademicYearService`
- Implement `GetActiveAcademicYear()` method
- Make Academic Year pages Admin-only

**Deliverable:** Single active academic year enforced system-wide

---

## 👥 Phase 3 – Core People Management

### Students

**Goal:** Manage student profiles and lifecycle

- Create `Student` entity
- Link Student to Identity User
- Student CRUD controller
- Student CRUD views
- Generate unique student number
- Activate / deactivate student
- Validation for uniqueness

---

### Parents

**Goal:** Parent access to children data

- Create `Parent` entity
- Link Parent to Identity User
- Parent CRUD controller
- Parent CRUD views
- Implement Student–Parent many-to-many relation
- UI to assign students to parents
- Restrict parent access to own children only

---

### Teachers

**Goal:** Manage teaching staff

- Create `Teacher` entity
- Link Teacher to Identity User
- Teacher CRUD controller
- Teacher CRUD views

**Deliverable:** Students, parents, and teachers fully managed

---

## 🏫 Phase 4 – School Structure

### Classes

- Create `Class` entity (Grade + Section)
- Class CRUD controller
- Class CRUD views
- Validate unique Grade + Section

---

### Subjects

- Create `Subject` entity
- Subject CRUD controller
- Subject CRUD views

---

### Rooms

- Create `Room` entity
- Room CRUD controller
- Room CRUD views
- Room capacity and type fields
- Enable / disable rooms

**Deliverable:** Academic and physical school structure defined

---

## 🕘 Phase 5 – School Hours & Timetable

### Time Slots (Hours)

**Goal:** Define school periods

- Create `TimeSlot` entity
- TimeSlot CRUD controller
- TimeSlot CRUD views
- Validate overlapping time slots

---

### Class Schedule (Timetable)

**Goal:** Weekly timetable with conflict validation

- Create `ClassSchedule` entity
- Relations: Class, Subject, Teacher, Room, TimeSlot, AcademicYear
- ClassSchedule CRUD controller
- Weekly timetable grid view (days × time slots)
- Filter timetable by class / teacher / room
- Validate teacher conflicts
- Validate room conflicts
- Lock past academic year schedules

**Deliverable:** Conflict-free scheduling system

---

## 🎓 Phase 6 – Student Enrollment

**Goal:** Assign students to classes per academic year

### Tasks
- Create `Enrollment` entity
- Enrollment CRUD controller
- UI to enroll students into class for academic year
- Prevent duplicate enrollment in same year
- View enrolled students per class
- Restrict enrollment management to Admin

**Deliverable:** Correct student placement per year

---

## ✅ Phase 7 – Attendance Management

**Goal:** Attendance tied to scheduled lessons

### Tasks
- Update Attendance entity to reference `ClassSchedule`
- Attendance marking page for teachers
- Date validation (lesson must exist)
- Prevent duplicate attendance entries
- Student attendance view (read-only)
- Parent attendance view (read-only)
- Admin attendance reports
- Attendance summary calculations

**Deliverable:** Accurate lesson-based attendance

---

## 📝 Phase 8 – Exams & Grades

### Exams

- Create `Exam` entity
- Link Exam to Subject + Academic Year
- Exam CRUD controller
- Exam CRUD views
- Lock exams in past academic years

---

### Grades

- Create `Grade` entity
- Grade entry UI for teachers
- Score validation (0–MaxScore)
- Calculate averages
- Student grade report
- Parent grade report

**Deliverable:** Academic performance tracking

---

## 📊 Phase 9 – Dashboards

### Admin Dashboard
- Active academic year display
- Student / teacher counts
- Attendance overview

### Teacher Dashboard
- Today’s schedule
- Classes taught
- Attendance shortcuts

### Student Dashboard
- Weekly timetable
- Attendance summary
- Grade summary

### Parent Dashboard
- Child selector
- Attendance overview
- Grade overview
- Timetable view

**Deliverable:** Role-specific experience

---

## 🔐 Phase 10 – Security, Validation & Polish

**Goal:** Production-quality behavior

### Tasks
- DataAnnotations validation across models
- Authorization review for all controllers
- Anti-forgery token verification
- Global exception handling
- Disable editing historical data
- Improve validation and error messages
- UI consistency cleanup

---

## 🧪 Phase 11 – Testing & Documentation

**Goal:** Stability and maintainability

### Tasks
- Manual testing for all roles
- Test academic year switching
- Test timetable conflict scenarios
- Refactor controllers into services
- Remove unused code
- Update README with setup instructions
- Write developer onboarding notes

---

## 🚀 Done Criteria
- All MVP features functional
- No critical bugs
- Academic-year data isolation enforced
- Clean architecture respected
- Code ready for learning review

---

**End of Development Plan**

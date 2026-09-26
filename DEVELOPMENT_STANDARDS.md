# Development Standards

This document defines the coding, naming, repository, and collaboration standards for the School Management System project.

---

# 1. General Principles

- Follow Clean Code principles.
- Prefer readability over cleverness.
- Write self-explanatory code whenever possible.
- Keep classes and methods focused on a single responsibility.
- Avoid unnecessary complexity.
- Use meaningful names instead of abbreviations.
- Follow SOLID principles where appropriate.

---

# 2. C# Naming Conventions

## Classes

Use PascalCase.

✅ Good

```csharp
Student
TeacherService
AcademicYearController
ClassSchedule
```

❌ Bad

```csharp
student
teacher_service
academicyearcontroller
```

---

## Interfaces

Prefix with "I".

✅ Good

```csharp
IStudentService
IAcademicYearService
IRepository
```

❌ Bad

```csharp
StudentServiceInterface
StudentServiceContract
```

---

## Methods

Use PascalCase.

✅ Good

```csharp
GetStudentById()
CreateEnrollment()
CalculateAverageGrade()
```

---

## Properties

Use PascalCase.

✅ Good

```csharp
FirstName
StudentNumber
DateOfBirth
```

---

## Private Fields

Use camelCase with underscore prefix.

✅ Good

```csharp
private readonly IStudentService _studentService;
private readonly ApplicationDbContext _context;
```

❌ Bad

```csharp
private readonly IStudentService studentService;
private readonly ApplicationDbContext Context;
```

---

## Local Variables

Use camelCase.

✅ Good

```csharp
var student = ...
var activeYear = ...
```

---

## Constants

Use PascalCase.

✅ Good

```csharp
public const int MaxStudentsPerClass = 30;
```

---

# 3. Entity Naming Standards

Entity names should be singular.

✅ Good

```csharp
Student
Teacher
Parent
Room
Enrollment
AcademicYear
Subject
Grade
Exam
```

❌ Bad

```csharp
Students
Teachers
Rooms
Grades
```

---

## Database Tables

Entity Framework will generate plural table names if configured.

Example:

```text
Student -> Students
Teacher -> Teachers
Exam -> Exams
```

Entities remain singular in code.

---

## Entity Primary Keys

Use:

```csharp
Id
```

Example:

```csharp
public int Id { get; set; }
```

Avoid:

```csharp
StudentId
TeacherId
```

as primary keys.

---

## Foreign Keys

Use entity name + Id.

```csharp
public int StudentId { get; set; }
public int TeacherId { get; set; }
public int AcademicYearId { get; set; }
```

---

# 4. Service Naming Standards

Services represent business logic.

Naming convention:

```text
<Entity>Name + Service
```

Examples:

```csharp
StudentService
TeacherService
AcademicYearService
EnrollmentService
AttendanceService
```

Interfaces:

```csharp
IStudentService
ITeacherService
IAcademicYearService
```

---

## Service Methods

Use action-oriented names.

✅ Good

```csharp
GetActiveAcademicYear()
EnrollStudent()
GenerateStudentNumber()
CalculateAttendancePercentage()
```

❌ Bad

```csharp
HandleStudent()
ProcessData()
DoStuff()
```

---

# 5. Controller Naming Standards

Controllers follow MVC conventions.

Format:

```text
<Entity>Name + Controller
```

Examples:

```csharp
StudentController
TeacherController
AcademicYearController
EnrollmentController
AttendanceController
```

---

## Actions

Use clear CRUD-friendly names.

```csharp
Index()
Details()
Create()
Edit()
Delete()
```

Additional examples:

```csharp
AssignStudents()
ViewTimetable()
MarkAttendance()
GenerateReport()
```

---

# 6. ViewModel Naming Standards

Format:

```text
<Entity>Name + ViewModel
```

Examples:

```csharp
StudentViewModel
TeacherViewModel
AttendanceViewModel
```

Create/Edit models:

```csharp
CreateStudentViewModel
EditStudentViewModel
StudentDetailsViewModel
```

---

# 7. Folder Structure

```text
SchoolManagementSystem

├── Controllers
│
├── Services
│   ├── Interfaces
│   └── Implementations
│
├── Models
│   ├── Entities
│   └── ViewModels
│
├── Data
│   ├── Context
│   ├── Configurations
│   └── Migrations
│
├── Views
│
├── wwwroot
│   ├── css
│   ├── js
│   └── images
│
├── Extensions
│
├── Middleware
│
├── Constants
│
└── Helpers
```

---

# 8. Branch Naming Strategy

Format:

```text
feature/<feature-name>
bugfix/<bug-name>
hotfix/<hotfix-name>
refactor/<refactor-name>
docs/<documentation-name>
```

Examples:

```text
feature/student-management
feature/timetable-ui

bugfix/attendance-validation

refactor/academic-year-service

docs/update-readme
```

---

# 9. Git Commit Message Standards

Use imperative mood.

Format:

```text
<type>: <description>
```

---

## Commit Types

### Feature

```text
feat: add student enrollment functionality
```

### Bug Fix

```text
fix: prevent duplicate enrollment records
```

### Refactor

```text
refactor: move attendance logic to service layer
```

### Documentation

```text
docs: update setup instructions
```

### Style

```text
style: format student controller
```

### Test

```text
test: add enrollment service tests
```

### Chore

```text
chore: update NuGet packages
```

---

## Examples

✅ Good

```text
feat: create academic year management module

fix: validate unique student number

refactor: extract timetable conflict logic

docs: add development standards
```

❌ Bad

```text
update

fixed bug

changes

new stuff
```

---

# 10. Pull Request Naming Standards

Format:

```text
[Type] Short Description
```

Examples:

```text
[Feature] Student Management

[Feature] Academic Year Management

[Bug Fix] Timetable Conflict Validation

[Refactor] Attendance Service Cleanup

[Documentation] Initial Project Standards
```

---

# 11. Pull Request Requirements

Every Pull Request should:

- Build successfully
- Pass all manual testing
- Have a clear description
- Reference related GitHub Issue
- Include screenshots for UI changes
- Follow naming conventions
- Have no unnecessary commented code

---

# 12. Code Review Checklist

Before merging:

- [ ] Naming conventions followed
- [ ] No duplicated code
- [ ] Business logic placed in services
- [ ] Authorization verified
- [ ] Validation implemented
- [ ] Error handling considered
- [ ] Code is readable
- [ ] Documentation updated if necessary
- [ ] No debug code left behind
- [ ] Pull Request linked to an Issue

---

# 13. Definition of Done

A task is considered complete when:

- [ ] Code implemented
- [ ] Build succeeds
- [ ] Manual testing completed
- [ ] Acceptance criteria satisfied
- [ ] Documentation updated
- [ ] Pull Request approved
- [ ] Changes merged into main branch

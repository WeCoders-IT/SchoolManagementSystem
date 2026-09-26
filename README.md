# School Management System (ASP.NET Core MVC)

This repository contains a **School Management System** built with **ASP.NET Core MVC** as a **learning-oriented but real‑world inspired project**.

The application is designed for a **small high school** and demonstrates how to build a **role-based, academic-year–driven web application** using modern .NET practices such as Entity Framework Core, ASP.NET Identity, and clean MVC architecture.

---

## 🎯 Project Purpose

The main goals of this project are:

- To practice **realistic system design** for educational institutions  
- To apply **ASP.NET Core MVC** patterns in a structured way  
- To model **academic-year–based data isolation** correctly  
- To demonstrate **role-based authorization** and access control  
- To simulate real development workflows using **GitHub boards and tasks**

This project is suitable for:
- Learning ASP.NET Core MVC
- Practicing data modeling with EF Core
- Team collaboration and task assignment
- Code reviews and architecture discussions

---

## 🏫 Core Features

- **Role-based authentication**
  - Admin
  - Teacher
  - Student
  - Parent

- **Academic Year Management**
  - One active academic year at a time
  - Historical academic data is read-only

- **People Management**
  - Students, Teachers, Parents
  - Parent–Student relationships

- **School Structure**
  - Classes (Grade + Section)
  - Subjects
  - Rooms with capacity and type

- **Scheduling & Timetable**
  - Weekly timetable
  - School hours (time slots)
  - Room and teacher conflict validation

- **Enrollment**
  - Students enrolled per class per academic year

- **Attendance**
  - Lesson-based attendance
  - Teacher-managed
  - Student & Parent read-only views

- **Exams & Grades**
  - Exam management per academic year
  - Grade entry and reporting

- **Dashboards**
  - Admin overview
  - Teacher daily schedule
  - Student & Parent academic views

---

## 🛠 Technology Stack

- **ASP.NET Core MVC**
- **Entity Framework Core**
- **SQL Server**
- **ASP.NET Identity**
- **Razor Views**
- **Bootstrap**
- **GitHub Projects / Issues**

---

## 🧱 Architecture Overview

The application follows a layered MVC architecture designed to separate presentation, business logic, and data access concerns.

### Layers

- Controllers – Handle HTTP requests and responses
- Services – Contain business logic and validation rules
- Models – Domain entities and database objects
- ViewModels – Data transfer between controllers and views
- Data Layer – Entity Framework Core DbContext and configurations
- SQL Server – Persistent data storage

### Cross-Cutting Concerns

- ASP.NET Identity for authentication and authorization
- Role-based access control
- Academic-year isolation
- Validation and error handling

All academic data is scoped to the active academic year to reflect realistic school administration workflows.

---

## 📌 Project Status

- ✅ Designed for learning and demonstration
- ✅ Organized into development phases
- ✅ Task-based workflow suitable for teams
- 🚧 Not intended for production use without further hardening

---

## 📄 Documentation

- `DEVELOPMENT_PLAN.md` – full development roadmap and tasks
- Wireframes – simple UI blueprints for all main pages
- GitHub Issues – used to track development progress

---

## 📚 Learning Outcomes

By working on this project, developers gain experience with:
- ASP.NET Core MVC best practices
- Entity Framework Core relationships
- Role-based authorization
- Scheduling and conflict validation
- Academic-year–driven business logic
- Team-based project planning

---

## 🔄 Development Approach

The project is developed using an incremental, phase-based approach.

Development is organized into Epics, Features, and Tasks tracked through GitHub Projects and Issues.

### Workflow

1. Define requirements and acceptance criteria
2. Break work into Features and Tasks
3. Implement functionality in feature branches
4. Review code and perform testing
5. Merge into the main branch
6. Update documentation and project status

### Development Principles

- Keep controllers thin
- Place business logic in services
- Use Entity Framework Core for data access
- Apply role-based authorization throughout the system
- Maintain academic-year data isolation
- Follow consistent coding standards and naming conventions

---

## 🚀 Setup Instructions

### Prerequisites

Install the following software:

- .NET SDK 9.0 (or latest supported version)
- SQL Server
- Visual Studio 2022 / VS Code
- Git

### Clone Repository

```bash
git clone https://github.com/WeCoders-IT/SchoolManagementSystem.git
cd SchoolManagementSystem
```
---

## 📎 License

This project is provided for **educational purposes**.
Feel free to fork, modify, and experiment.

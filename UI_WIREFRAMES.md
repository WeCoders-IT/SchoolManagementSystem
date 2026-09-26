# School Management System - UI Wireframes & Figma Specifications

## 🎨 Global Design Rules (Apply to All Pages)

### Frame
- Desktop frame: **1440 × 900**
- Layout type: **Left navigation + top bar content layout**

### Grid
- 12-column grid
- Margin: 24px
- Gutter: 16px

### Typography
- Page title: 24px, Bold
- Section title: 18px, Semibold
- Body text: 14–16px
- Table header: 14px, Medium

### Component Library (Create Once in Figma)

#### Buttons
- Primary Button
- Secondary Button
- Link Button

#### Form Controls
- Text Input
- Select Dropdown
- Date Picker

#### UI Elements
- Table
- Card
- Status Badge (Active / Inactive)
- Modal Dialog

---

# 🔐 1. Login Page

## Layout
Centered card layout

## Components
- Card (400px width)
- Text: "School Management System"
- Email input
- Password input
- Login button
- Error message placeholder

## Developer Notes
- Uses ASP.NET Identity
- No self-registration
- Redirect user based on role after login

---

# 📊 2. Admin Dashboard

## Layout
Full-width content area

## Components

### Page Title
- Admin Dashboard

### Summary Cards
- Active Academic Year
- Total Students
- Total Teachers
- Total Classes

### Quick Actions
- Manage Academic Years
- Manage Students
- Manage Timetable

## Developer Notes
- Data scoped to active academic year
- Cards should be clickable

---

# 📅 3. Academic Years Management

## Layout
Header + Table

## Components

### Header
- Page Title: Academic Years
- Primary Button: Add Academic Year

### Table Columns
- Name
- Start Date
- End Date
- Status (Active Badge)
- Actions (Edit)

### Modal: Add/Edit Academic Year

#### Fields
- Name (Text)
- Start Date (Date Picker)
- End Date (Date Picker)
- Is Active (Checkbox)

## Rules
- Only one Academic Year can be active
- Past Academic Years are read-only

---

# 👨‍🎓 4. Students Management

## Layout
Header + Table

## Components

### Header
- Page Title: Students
- Button: Add Student

### Table Columns
- Student Number
- Full Name
- Status
- Actions (View / Edit)

## Student Details Page

### Sections
- Profile Card
- Enrollment History
- Parent Links

---

# 👪 5. Parents Management

## Layout
Two-column content area

### Left Column
Parent List Table

#### Columns
- Name
- Phone
- Actions (Assign Students)

### Right Column
Selected Parent Panel

#### Content
- Parent Information
- Linked Students List
- Add Student Link Button

## Notes
- Parents can only view their own children
- Student assignment managed by Admin

---

# 👨‍🏫 6. Teachers Management

## Layout
Header + Table

## Components

### Header
- Page Title: Teachers
- Button: Add Teacher

### Table Columns
- Name
- Subjects (Tags)
- Status
- Actions

---

# 🏫 7. Classes Management

## Layout
Header + Table

## Table Columns
- Grade
- Section
- Enrollment Count

### Actions
- View Enrollments
- View Timetable

## Rules
- Grade + Section must be unique

---

# 🏠 8. Rooms Management

## Layout
Header + Table

## Table Columns
- Room Name
- Type
- Capacity
- Status
- Actions

## Notes
- Disabled rooms cannot be scheduled

---

# 🕘 9. Time Slots (School Hours)

## Layout
Vertical list

## Components

### Header
- Button: Add Time Slot

### Table Columns
- Period Name
- Start Time
- End Time
- Order
- Actions

### Modal

#### Fields
- Period Name
- Start Time
- End Time

## Validation
- No overlapping time slots

---

# 📆 10. Class Timetable (Critical Page)

## Layout
Weekly grid

## Grid Structure

### Columns
- Monday
- Tuesday
- Wednesday
- Thursday
- Friday

### Rows
- Time Slots

## Cell Content
- Subject (Bold)
- Teacher Name
- Room Name

## Filters
- Academic Year
- Class Selector

### Notes
- Academic Year selector becomes read-only for past years

## Behavior
- Click cell to edit schedule
- Display conflict validation inline

---

# 🧾 11. Enrollment Management

## Layout

### Left Side
- Academic Year Selector
- Class Selector

### Right Side
- Student Checklist

## Components
- Academic Year Dropdown
- Class Dropdown
- Student List with Checkboxes
- Save Enrollment Button

---

# ✅ 12. Attendance Page

## Layout
Vertical flow

## Components

### Filters
- Date Picker

### Lesson Information
- Auto-loaded from timetable

### Student Table

#### Columns
- Student Name
- Status

#### Status Options
- Present
- Absent
- Late

### Actions
- Save Attendance Button

## Notes
- Teacher access only
- Attendance can only be recorded for scheduled lessons

---

# 📝 13. Exams & Grades

## Exams Page

### Components
- Exam List Table
- Create Exam Button

---

## Grades Page

### Components
- Student Rows
- Score Inputs
- Total Calculation
- Average Calculation

## Visibility

### Teacher
- Editable

### Student
- Read-only

### Parent
- Read-only

---

# 🎓 14. Student Dashboard

## Layout
Two-column layout

### Left Column
- Weekly Timetable

### Right Column
- Attendance Summary
- Grades Summary

---

# 👨‍👩‍👧 15. Parent Dashboard

## Layout

### Top Section
- Child Selector Dropdown

### Content
- Same structure as Student Dashboard

#### Information Available
- Timetable
- Attendance Summary
- Grades Summary

## Notes
- Read-only access

---

# 🎯 Figma Usage Guidelines

## Frame Structure
- Create one Figma page per application screen
- Name frames exactly as page names

## Design Practices
- Use Auto Layout everywhere
- Reuse shared components
- Maintain consistent spacing
- Follow component library standards

## Developer Handoff
- Export page screenshots
- Attach screenshots to GitHub Issues
- Reference issue IDs in Figma comments
- Keep wireframes focused on functionality rather than visual styling

---

# 📋 Screen List

1. Login Page
2. Admin Dashboard
3. Academic Years Management
4. Students Management
5. Parents Management
6. Teachers Management
7. Classes Management
8. Rooms Management
9. Time Slots
10. Class Timetable
11. Enrollment Management
12. Attendance Page
13. Exams & Grades
14. Student Dashboard
15. Parent Dashboard

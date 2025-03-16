# College ERP System
A command-line based Enterprise Resource Planning (ERP) system built with Java and PostgreSQL.

## Features

### Multi-User Authentication
- Creator (Super Admin) access
- Admin management
- Teacher accounts
- Student accounts

### Core Functionalities
- **Student Management**
  - Enrollment
  - Course registration
  - Section assignment
  - Personal info management
  
- **Teacher Management**
  - Course assignment
  - Section allocation
  - Personal info management

- **Course Management**
  - Course creation
  - Student enrollment
  - Teacher assignment
  - Course information tracking

- **Section Management**
  - Section creation
  - Student grouping
  - Teacher assignment

### Advanced Features
- Automated roll number generation
- Email ID generation
- Data persistence using:
  - File serialization
  - PostgreSQL database
- Activity logging
- Data export to text files

## Technical Stack
- Java (Core)
- PostgreSQL
- Custom data structures (`pavan_dynamic_array.java`)
- File I/O
- JDBC

## Database Schema
The system uses the following tables (defined in TableCreation.sql):
- Students
- Teachers
- Users
- Sections
- Courses
- Teacher_Section
- Student_Course
- Teacher_Course

## Setup Instructions

1. **Database Setup**
   ```sql
   -- Run the TableCreation.sql script
   psql -U postgres -d your_database < TableCreation.sql
   ```

2. **Configure Database Credentials**
   - Update the `credentials.java` file with your PostgreSQL details

3. **Compile and Run**
   ```bash
   javac *.java
   java Main
   ```

## File Structure
- `Main.java` - Entry point and menu system
- `ManagementSystem.java` - Core business logic
- `jdbcStuff.java` - Database operations
- Entity Classes:
  - `Student.java`
  - `Teacher.java`
  - `Course.java`
  - `Section.java`
  - `Admin.java`

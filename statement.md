# Problem Statement

College course registration is a critical administrative process that involves managing thousands of students, hundreds of courses, and complex enrollment workflows. Traditional manual or spreadsheet-based systems are prone to errors, data inconsistencies, and scalability issues. Educational institutions face several challenges:

- **Data Integrity Issues**: Manual entry leads to duplicate enrollments, incorrect student records, and grade discrepancies
- **Credit Limit Management**: No automated validation to prevent students from over-enrolling beyond their credit capacity
- **Lack of Real-time Analytics**: Difficulty in generating student transcripts, calculating GPAs, and analyzing performance distributions
- **Poor Data Persistence**: Risk of data loss without proper backup and recovery mechanisms
- **Time-Consuming Processes**: Manual course enrollment, grade assignment, and transcript generation consume significant administrative time

The College Course Registration Management (CCRM) system addresses these challenges by providing a comprehensive, automated solution that ensures data accuracy, enforces business rules, and streamlines academic operations.

---

# Scope of the Project

## **In Scope:**

The CCRM system provides the following functionalities:

### **Student Management**
- Add new students with unique registration numbers
- Update student information (email addresses)
- Search and filter students by name
- List all registered students

### **Course Management**
- Create courses with code, title, credits, department, and semester information
- Browse complete course catalog
- Filter courses by department
- Builder pattern implementation for flexible course creation

### **Enrollment Management**
- Enroll students in courses with credit limit validation
- Prevent duplicate enrollments
- Assign grades (S/A/B/C/D/F) to enrolled students
- Track and manage ungraded enrollments

### **Analytics & Reporting**
- Generate comprehensive academic transcripts for students
- Calculate weighted GPA based on credits and grade points
- Display GPA distribution across student population
- Performance statistics and analysis

### **Data Management**
- CSV-based import/export functionality
- File-based data persistence
- Automated backup system with directory size calculation
- Configurable data folder location

## **Out of Scope:**

The following features are NOT included in the current version:
- Web-based user interface (CLI only)
- Multi-user concurrent access with authentication
- Payment processing or fee management
- Course scheduling and timetable generation
- Faculty assignment and management
- Student attendance tracking
- Advanced reporting with graphical visualizations
- Integration with external systems (LMS, payment gateways)

---

# Target Users

The CCRM system is designed for the following user groups:

## **1. College Administrators**
- Manage student registrations and course catalog
- Oversee enrollment processes and credit allocations
- Generate reports for institutional decision-making
- Perform system backups and data maintenance

## **2. Academic Staff / Registrar Office**
- Process student enrollments and withdrawals
- Assign grades to students after course completion
- Generate official transcripts for students
- Monitor enrollment statistics and GPA distributions

## **3. Department Coordinators**
- Manage courses within their department
- Review course enrollments and student performance
- Track departmental academic metrics

## **4. System Administrators**
- Configure system settings (data folder, credit limits)
- Perform data imports/exports for system integration
- Maintain data integrity and perform backups
- Troubleshoot system issues

---

# High-level Features

## **Core Functional Features**

### **1. Student Management Module**
- ✓ Add new students with registration number, name, and email
- ✓ Search students by partial name matching
- ✓ Update student contact information
- ✓ View complete student roster
- ✓ Unique registration number validation

### **2. Course Management Module**
- ✓ Create courses using flexible Builder pattern
- ✓ Define course attributes (code, title, credits, department, semester)
- ✓ Browse and search course catalog
- ✓ Filter courses by department
- ✓ Manage course metadata

### **3. Enrollment Management Module**
- ✓ Enroll students in courses with validation checks
- ✓ Credit limit enforcement (prevents over-enrollment)
- ✓ Duplicate enrollment prevention
- ✓ Grade assignment (S/A/B/C/D/F grading system)
- ✓ Track graded and ungraded enrollments
- ✓ Student-course relationship management

### **4. Analytics & Transcript Module**
- ✓ Generate comprehensive student transcripts
- ✓ Weighted GPA calculation (grade points × credits)
- ✓ GPA distribution analysis across all students
- ✓ Performance statistics and insights
- ✓ Academic performance tracking

### **5. Data Persistence & Backup**
- ✓ CSV-based data import/export
- ✓ File-based storage for students, courses, and enrollments
- ✓ Automated backup system with timestamp
- ✓ Recursive directory size calculation
- ✓ Configurable data folder location

## **Technical Features**

- ✓ **Object-Oriented Design**: Clean separation of concerns with domain, service, and CLI layers
- ✓ **Design Patterns**: Builder pattern for course creation, Singleton for configuration
- ✓ **Exception Handling**: Custom exceptions for business rule violations
- ✓ **Stream Processing**: Modern Java 8+ streams for data filtering and aggregation
- ✓ **Optional Handling**: Null-safe programming with Optional class
- ✓ **Immutable Records**: Using Java records for data carriers (Name class)
- ✓ **Assertions**: Runtime validation for debugging and testing
- ✓ **Configuration Management**: Property-based configuration for flexibility

## **User Experience Features**

- ✓ Interactive command-line menu interface
- ✓ Clear input prompts and validation messages
- ✓ Error handling with user-friendly messages
- ✓ Organized output formatting for readability
- ✓ Menu-driven navigation for ease of use

---

# Success Criteria

The CCRM system will be considered successful if it:

1. **Accurately manages** student and course data without duplication or inconsistency
2. **Enforces business rules** such as credit limits and enrollment constraints
3. **Generates reliable** transcripts and GPA calculations
4. **Persists data** safely with backup and recovery capabilities
5. **Provides efficient** search and filtering operations
6. **Maintains code quality** with proper design patterns and best practices
7. **Offers user-friendly** interaction through clear CLI interface
Campus Course & Records Manager (CCRM)
Overview
The Campus Course & Records Manager (CCRM) is a comprehensive, command-line based Java application designed to manage student and course records for an educational institution. It provides a simple, menu-driven interface for administrators to perform essential academic tasks such as student registration, course creation, student enrollment, grading, and data management.

The application uses an in-memory data store for runtime operations and supports data persistence through CSV file import/export and a simple backup system.

Features
Student Management: Add new students with unique registration numbers and list all registered students.

Course Management: Create new courses, specifying details like course code, title, credits, instructor, and semester.

Enrollment System: Enroll students into courses, with built-in validation to prevent duplicate enrollments and to enforce a maximum credit limit (20 credits per student).

Grading & Transcripts: Record marks for a student in a specific course, which automatically calculates the corresponding letter grade. Generate a full academic transcript for any student, including their GPA.

Data Persistence:

Export: Save all student, course, and enrollment data to .csv files in a data/ directory.

Import: Load data from the .csv files back into the application, restoring the previous state.

Backup Functionality: Create a timestamped backup of the entire data/ directory to a backups/ folder for data safety.

Project Structure
The project is organized into logical packages to separate concerns and maintain a clean architecture.

src
└── edu
    └── ccrm
        ├── cli          // Contains the command-line interface (Main.java)
        ├── config       // Application configuration (AppConfig.java)
        ├── domain       // Core data models (Student, Course, Enrollment, etc.)
        ├── exceptions   // Custom exception classes
        ├── io           // Services for file input/output (Import/Export, Backup)
        └── service      // Business logic interfaces and implementations

cli: The entry point of the application and all user-interaction logic.

domain: Defines the core entities of the application, such as Student, Course, and Enrollment.

service: Contains the business logic for managing the domain objects (e.g., StudentServiceImpl, CourseServiceImpl).

io: Handles all file operations, including reading/writing CSV files and creating backups.

exceptions: Defines custom exceptions for specific error scenarios, like DuplicateEnrollmentException.

Getting Started

Prerequisites:
Java Development Kit (JDK) 11 or higher.

How to Compile and Run
Navigate to the Source Directory: Open your terminal or command prompt and navigate to the project's root directory where the src folder is located.

Compile the Project: Run the following command to compile all .java files. This command places the compiled .class files into an out directory.

javac -d out $(find src -name "*.java")

Run the Application: Execute the compiled code by running the Main class.

java -cp out edu.ccrm.cli.Main

Interact with the Menu: Once running, the application will display the main menu. Simply enter the number corresponding to the desired operation.

==== Campus Course & Records Manager ====
1. Add Student
2. List Students
3. Add Course
4. List Courses
5. Enroll Student in Course
6. Record Marks for Enrollment
7. Show Transcript (GPA)
8. Export Data
9. Import Data
10. Backup Data
0. Exit
Enter choice:

Data Storage
Runtime Data: While the application is running, all data is stored in-memory using Java Collections (primarily HashMap).

Persistent Data: To save data between sessions, use the Export Data option (8). This creates the following files:

data/students.csv

data/courses.csv

data/enrollments.csv

Backups: Using the Backup Data option (10) will create a timestamped copy of the data folder inside a backups directory (e.g., backups/backup_20250924_083700).

Key Design Principles
Service-Oriented Architecture: Business logic is encapsulated within service classes (StudentService, CourseService), promoting modularity and separation of concerns.

Builder Pattern: The Course object is constructed using a nested Builder, which provides a clean and readable way to create complex objects.

In-Memory Repository: Service implementations use HashMaps to act as an in-memory database, simplifying data access for this scale of application.

Custom Exceptions: The application uses specific exceptions like DuplicateEnrollmentException and MaxCreditLimitExceededException to handle predictable errors gracefully.
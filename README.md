# Student Academic Management System

**Student:** Amaan Raza Khan  
**Registration No:** 25BAI11152  
**Department:** Computer Science & Engineering (AIML)  
**Course:** Programming in JAVA  
**Institution:** Vellore Institute of Technology (VIT)

---

## 1. Project Overview

The **Student Academic Management System** is a terminal-based Java application developed to manage basic academic information of students.

The system allows users to maintain student details, course marks, attendance records, academic performance, and saved student records through a simple menu-driven interface.

The project demonstrates important Java programming concepts such as:

- Classes and constructors  
- Inheritance and method overriding  
- Method overloading  
- Abstract classes and interfaces  
- Runtime polymorphism  
- Exception handling  
- Multithreading  
- Loops  
- Java I/O streams  

---

## 2. Objectives

- Manage student information efficiently  
- Maintain course marks for students  
- Calculate total and average marks  
- Determine the overall grade of a student  
- Maintain and calculate attendance percentage  
- Generate academic performance reports  
- Save student records into files  
- Read previously saved student records  
- Demonstrate core Java Object-Oriented Programming concepts  
- Provide a simple terminal-based academic management system  

---

## 3. Features

| #  | Feature                                      |
|----|----------------------------------------------|
| 1  | Add a new student                            |
| 2  | Display all students                         |
| 3  | Search for a student using Student ID        |
| 4  | Update student information                   |
| 5  | Delete a student                             |
| 6  | Add course marks                             |
| 7  | Add attendance information                   |
| 8  | Generate an academic performance report      |
| 9  | Save student records into a text file        |
| 10 | Read saved student records                   |
| 11 | Demonstrate runtime polymorphism             |
| 12 | Calculate factorial using a looping statement|
| 13 | Handle invalid user input using exception handling |

---

## 4. Major Functional Modules

### Student Management
Manages basic student information:
- Student ID  
- Student name  
- Department  

Supports adding, displaying, searching, updating, and deleting student records.

### Academic Management
Manages course names and marks. Calculates:
- Total marks  
- Average marks  
- Overall grade  

### Attendance Management
Stores:
- Total classes  
- Attended classes  

Calculates attendance percentage and displays attendance status (e.g., Satisfactory for ≥ 75%).

### Report and File Management
Generates academic reports and allows student records to be saved to and read from text files using multithreading and Java I/O streams.

---

## 5. Java Concepts Demonstrated

| Java Concept           | Implementation                                          |
|------------------------|---------------------------------------------------------|
| Class                  | `Student`, `Course`, `Attendance`, and other classes    |
| Constructor            | Constructors in project classes                         |
| Static Method          | Grade calculation and report generation                 |
| Method Overloading     | `addCourse()` and report/grade methods                  |
| Inheritance            | `Student extends Person`                                |
| Method Overriding      | `Student` overrides `displayInfo()`                     |
| `super` Constructor    | `super(studentId, name)`                                |
| `super` Method         | `super.displayInfo()`                                   |
| Runtime Polymorphism   | `Person person = students.get(0)`                       |
| Abstract Class         | `Person`                                                |
| Interface              | `Printable`                                             |
| Multithreading         | `ReportThread extends Thread`                           |
| Loops                  | Student/course processing and factorial                 |
| Exception Handling     | Input and file operation validation                     |
| Java I/O Streams       | File writing and reading                                |

---

## 6. Technologies Used

- Java  
- Java Standard Library  
- Java I/O  
- VS Code  
- Command-line terminal  

No external framework or database is required to run the current version of the project.

---

## 7. Project Structure

```text
StudentAcademicManagementSystem/
│
├── src/
│   ├── Main.java
│   ├── Person.java
│   ├── Student.java
│   ├── Course.java
│   ├── Attendance.java
│   ├── AcademicReport.java
│   ├── Printable.java
│   ├── ReportThread.java
│   └── FileManager.java
│
├── data/
│   └── student_101.txt
│
├── README.md
└── statement.md
```

The `data` folder contains saved student records generated by the application.

---

## 8. Requirements

- Java Development Kit (JDK)  
- VS Code or another Java-supported editor  
- Windows PowerShell, Command Prompt, or another terminal  

---

## 9. How to Run

Open the project folder in the terminal.

**Compile the Java source files:**

```powershell
javac -d . src\*.java
```

**Run the application:**

```powershell
java -cp . Main
```

The menu-driven application will then start in the terminal.

---

## 10. Example Workflow

```text
Start
  ↓
Add Student
  ↓
Add Course Marks
  ↓
Add Attendance
  ↓
Generate Academic Report
  ↓
Save Student Record
  ↓
Read Saved Record
  ↓
Exit
```

---

## 11. Input Validation and Error Handling

The application validates user input and handles common errors, including:

- Invalid Student ID  
- Non-numeric menu input  
- Empty student name  
- Empty department  
- Invalid marks outside the range 0–100  
- Invalid attendance values  
- Negative factorial input  
- Missing saved student record  
- File input/output errors  

Java exception handling using `try-catch` prevents invalid input from terminating the application unexpectedly.

---

## 12. Testing

### Functional Testing

The following operations were successfully tested:

- Adding a student  
- Adding course marks  
- Calculating total and average marks  
- Calculating grade  
- Adding attendance  
- Calculating attendance percentage  
- Generating academic reports  
- Runtime polymorphism demonstration  
- Saving student records  
- Reading saved records  
- Calculating factorial  

### Validation Testing

Invalid inputs were also tested:

```text
abc          → non-numeric menu input
-8           → negative factorial input
```

The application correctly displayed validation messages without crashing.

---

## 13. Sample Result

For a student with:

```text
Student ID   : 101
Name         : Amaan Raza Khan
Department   : Computer Science And Engineering (AIML)
Java         : 83.0
```

and attendance:

```text
Total Classes    : 40
Classes Attended : 34
```

the system produced:

```text
========================================
       ACADEMIC PERFORMANCE REPORT
========================================
Student ID   : 101
Student Name : Amaan Raza Khan
Department   : Computer Science And Engineering (AIML)

Course Performance:
  Java Programming : 83.0

Total Marks    : 83.0
Average Marks  : 83.0
Overall Grade  : A

Attendance:
  Total Classes    : 40
  Classes Attended : 34
  Percentage       : 85.0%
  Status           : Satisfactory
========================================
[SUCCESS] Record written to data/student_101.txt
```

**Factorial test:**

```text
Enter a non-negative integer: 5
Factorial of 5 = 120
```

---

## 14. Project Limitations

- Active student information is stored in memory while the program is running.  
- Saved student records are stored as text files in the `data` folder.  
- The application does not currently use a database or graphical user interface.  

---

## 15. Future Enhancements

- Database-based student storage (SQLite / PostgreSQL with JDBC)  
- Graphical user interface (JavaFX or Swing)  
- Multiple attendance records for different subjects  
- Additional academic analytics  
- User authentication and role-based access  
- Improved report formatting  
- Expanded search and filtering options  

These enhancements are outside the scope of the current implementation.

---

## 16. Conclusion

The **Student Academic Management System** demonstrates how Java programming concepts can be combined to create a practical terminal-based application.

The project applies object-oriented programming principles, exception handling, file input/output, loops, multithreading, and other Java concepts to solve a basic academic record management problem.

It provides a structured workflow for managing students, academic performance, attendance, reports, and saved records.

---

*Project Report for Flipped Course Evaluation — VITyarthi (Build Your Own Project)*  
*Vellore Institute of Technology (VIT)*

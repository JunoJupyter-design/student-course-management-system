# 📘 Campus Course & Records Manager (CCRM)

[![Java](https://img.shields.io/badge/Java-11%2B-blue.svg)](https://www.oracle.com/java/technologies/downloads/)
[![IDE](https://img.shields.io/badge/IDE-Eclipse-orange.svg)](https://www.eclipse.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Campus Course & Records Manager (CCRM)** is a **command-line Java application** for managing students, courses, enrollments, grading, and academic records at an educational institution.  

It provides a **menu-driven interface** for administrators to handle registrations, create courses, enroll students, record grades, generate transcripts, and back up data.

---

## 🚀 Features

### 👨‍🎓 Student Management
- Add new students with unique registration numbers  
- View and manage all registered students  

### 📚 Course Management
- Create new courses with:  
  - Course Code  
  - Title  
  - Credits  
  - Instructor  
  - Semester  

### 📝 Enrollment System
- Enroll students in courses  
- Prevent duplicate enrollments  
- Enforce a maximum **20-credit limit** per student  

### 🎓 Grading & Transcripts
- Record marks and auto-calculate letter grades  
- Generate academic transcripts including **GPA**  

### 💾 Data Persistence & Backup
- Export data to **CSV files**  
- Create timestamped backups for data safety  

---

## 🛠️ Getting Started

### ✅ Prerequisites
- Java Development Kit (**JDK 11 or higher**)  
- Eclipse IDE (or any Java IDE)  

### 📂 Installation
```bash
# Clone repository
git clone https://github.com/JunoJupyter-design/student-course-management-system.git

### ▶️ Run in Eclipse
1. Open Eclipse → `File > Import...`  
2. Select `General > Existing Projects into Workspace`  
3. Browse to the cloned repo folder → Click **Finish**  
4. In **Package Explorer**, navigate to:  

 src/edu/ccrm/cli/Main.java
5. Right-click `Main.java` → `Run As > Java Application`  

---

## 📖 Java Platform Fundamentals

### 🕰️ A Brief History of Java
| Year | Event |
|------|--------|
| 1991 | Sun Microsystems’ Green Team starts "Oak" |
| 1995 | Java 1.0 released with *Write Once, Run Anywhere* |
| 1998 | Java 2 (J2SE 1.2) introduces Swing & Collections |
| 2004 | J2SE 5.0 adds Generics, Annotations, Autoboxing |
| 2010 | Oracle acquires Sun Microsystems |
| 2014 | Java SE 8 introduces Lambdas & Streams |
| 2021 | Java 17 (LTS) introduces Sealed Classes & Pattern Matching |

---

### 📦 Java Editions
| Edition | Usage | Core API | Example |
|---------|-------|----------|---------|
| **Java ME** | Mobile & IoT | Small subset of Java SE | Feature phone app |
| **Java SE** | Desktop & servers | Core Java language & libraries | This CCRM project |
| **Java EE** | Web & enterprise | Adds APIs for Servlets, JMS, Web services | Online banking app |

---

### 🏗️ Java Architecture
- **JVM (Java Virtual Machine):** Runs Java bytecode on any OS  
- **JRE (Java Runtime Environment):** Provides JVM + core libraries  
- **JDK (Java Development Kit):** Full toolkit with compiler & debugger  

**Flow:**  
`Source Code (.java)` ➝ `JDK compiles to Bytecode (.class)` ➝ `JVM executes`  

---

## 📂 Project Structure

student-course-management-system/
│── src/
│   └── edu/
│       └── ccrm/
│           └── cli/
│               └── Main.java   # Entry point
│── data/                       # CSV storage
│── backup/                     # Timestamped backups
│── README.md                   # Documentation


---

## ⚙️ Development Environment Setup

### 🖥️ Install Java (Windows)
1. Download latest **JDK (17 LTS recommended)**  
2. Install to: `C:\Program Files\Java\jdk-17.x.x`  
3. Set environment variables:  
   - `JAVA_HOME = C:\Program Files\Java\jdk-17.x.x`  
   - Add `%JAVA_HOME%\bin` to `Path`  
4. Verify:
   ```bash
   java -version
   javac -version

   (./Images/Java_Version.png)

   💻 Using Eclipse
	1.	Create new project: File > New > Java Project
	2.	Add class: Right-click src → New > Class → Check public static void main
	3.	Run: Right-click file → Run As > Java Application

⸻

📄 License

This project is licensed under the MIT License – free to use, modify, and distribute.

---


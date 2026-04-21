# 🎯 Quizz System
<a href="https://github.com/ttasc/Quizz"><img src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/Overview.png" width="100%" alt="" /></a>

> A distributed quiz management system for schools and training environments — enabling teachers to create, manage, and distribute exams over LAN with real-time monitoring.

---

## 📌 Table of Contents
- [About The Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture Overview](#-architecture-overview)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [License](#-license)

---

## 📖 About The Project

**Quizz** is a Java-based client-server application designed to simplify the process of organizing and managing multiple-choice exams in educational environments.

The system allows teachers to:
- Create and manage question banks
- Organize exams across multiple subjects
- Distribute tests to students over LAN
- Monitor submissions and analyze results

Built as a **lightweight, cross-platform desktop system**, Quizz focuses on reliability, simplicity, and efficient exam management without requiring internet connectivity.

---

## ✨ Features

### 🖥️ Server (Teacher Side)
- 📚 Multiple workspaces for different classes or use cases
- 📝 Exam management (with question shuffling)
- 👨‍🎓 Student & group management
- 📊 Submission tracking and monitoring
- 📂 Subject & question bank organization
- 🌐 Distribute exams via LAN

---

### 💻 Client (Student Side)
- 🧑 Join exams using server IP + port
- ⏱️ Take exams in a controlled environment
- 📤 Submit answers directly to server

---

## 🧰 Tech Stack

| Category        | Technology |
|----------------|------------|
| Language       | Java 17 |
| Architecture   | Client-Server (LAN-based) |
| Database       | MySQL / MariaDB |
| Build Tool     | Maven |
| UI             | Java Desktop (Swing-based) |

---

## 🏗️ Architecture Overview

The system consists of two main components:

### 🖥️ Quizz Server
- Centralized exam management system
- Handles:
  - Question banks
  - Exam generation
  - Student tracking
  - Submission storage
- Connects to MySQL/MariaDB database

---

### 💻 Quizz Client
- Lightweight application for students
- Connects to server via IP + port
- Provides exam interface and submission flow

---

## 📸 Screenshots

<p align="center">
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/client1.png" title="Students enter ID and server connection info" />
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/client2.png" title="Exam interface for students" /><br/><br/>
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server1.png" title="Monitor student status" />
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server2.png" title="View submissions" /><br/><br/>
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server3.png" title="Create new exam" />
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server4.png" title="Exam management UI" /><br/><br/>
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server5.png" title="Subject management UI" />
  <img width="49%" src="https://raw.githubusercontent.com/ttasc/Quizz/master/assets/server6.png" title="Student management UI" />
</p>

---

## 🚀 Getting Started

### ⚙️ Prerequisites

- Java 17+
- MySQL or MariaDB

Check Java version:
```bash
java -version
````

---

### 🗄️ Database Setup

```sql id="7k2d0a"
-- Default configuration
Username: root
Password: 123456789
Host: localhost
Port: 3306
```

1. Start MySQL/MariaDB
2. Run the SQL script:

   ```
   QuizzServerInitTableMySQL.sql
   ```
3. This will initialize the required database schema

---

### 📦 Download

Download pre-built binaries from:
👉 [https://github.com/ttasc/Quizz/releases](https://github.com/ttasc/Quizz/releases)

---

### 🔨 Build From Source

Requirements:

* Java 17
* Maven

```bash id="b6t3ap"
git clone https://github.com/ttasc/Quizz.git
cd Quizz
```

Build Server:

```bash
cd QuizzServer
mvn package
```

Build Client:

```bash
cd QuizzClient
mvn package
```

Output:

* `QuizzServer.jar`
* `QuizzClient.jar`

---

## ▶️ Usage

### 🖥️ Run Server

```bash id="x2m91s"
java -jar QuizzServer.jar
```

* Ensure database is running before starting server

---

### 💻 Run Client

```bash id="w8n3pl"
java -jar QuizzClient.jar
```

* Enter:

  * Student ID
  * Server IP
  * Port

---

## 📄 License

This project is currently not licensed.
You may consider adding an MIT License for open-source usage.

---

## 🙌 Acknowledgements

* Java & open-source ecosystem
* MySQL / MariaDB community

---

> 💡 This project demonstrates practical experience in building distributed desktop systems, database-driven applications, and LAN-based communication for real-world educational use cases.

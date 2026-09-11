# 📚 Thinky Winky — Your Personal Study Companion
<p align="center">
  <img src="thinky__1_-removebg-preview.png" alt="Thinky Winky Logo" width="150" />
</p>
<p align="center">
  <b>A comprehensive, web-based study platform designed to optimize learning habits, manage schedules, track focus sessions, and organize course materials.</b>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/PHP-7.4%2B-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
  <img src="https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/License-MIT-green.style=for-the-badge" alt="License" />
</p>
---
## 📖 Table of Contents
- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Project Architecture & File Structure](#-project-architecture--file-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation & Local Setup](#installation--local-setup)
  - [Database Configuration](#database-configuration)
- [Database Schema](#-database-schema)
- [Usage Guide](#-usage-guide)
- [Contributing](#-contributing)
- [License](#-license)
---
## 🎯 About The Project
**Thinky Winky** is an all-in-one productivity and study management web application crafted for students. It bridges schedule planning, concentration techniques (Pomodoro), progress analytics, and course summary sharing into a single intuitive dashboard.
Whether you're organizing daily study schedules, tracking focus hours per module, uploading PDF study guides, or exploring scientifically backed study methods (such as Active Recall or Feynman Technique), Thinky Winky provides all the tools needed to boost academic performance.
---
## ✨ Key Features
### ⏱️ 1. Interactive Pomodoro Focus Timer
- Customizable work and break session intervals.
- Integrated task tracker linking study sessions directly to subjects.
- Automatic logging of completed focus sessions to track overall study time.
### 📅 2. Weekly Study Planner & Interactive Calendar
- Plan study sessions with exact start times, target durations, and notes.
- Monthly and daily calendar views to visualize deadlines and study routines.
- One-click task completion status updating real-time analytics.
### 📄 3. Course Summaries & PDF Document Hub
- Organize study summaries by academic subject/module.
- Upload PDF summaries with automated file validation.
- Interactive download counter tracking document downloads.
### 📊 4. Progress Analytics & Visual Stats
- Track total focus time and completed study sessions.
- Module time distribution break-down.
- Visual charts reflecting daily/weekly productivity trends.
### 💡 5. Study Techniques Guide
- Curated methodologies explaining proven techniques:
  - **Pomodoro Technique**
  - **Feynman Technique**
  - **Active Recall**
  - **SQ3R Method**
  - **Leitner System**
### 👤 6. Secure Authentication & Profile Management
- User signup and login with secure password hashing (`password_hash`).
- Profile customization including study field (`filiere`) and avatar upload.
---
## 🛠️ Tech Stack
- **Backend:** PHP (PDO Data Objects)
- **Database:** MySQL / MariaDB
- **Frontend:** HTML5, CSS3 (Modern Flexbox/Grid, CSS Variables), Vanilla JavaScript
- **Icons & Fonts:** FontAwesome 6.4, Google Fonts (Inter, Poppins)
- **Environment:** WAMP Server / XAMPP / LAMP / MAMP
---
## 📁 Project Architecture & File Structure
```
thinkywinky/
├── config.php            # Centralized Database Connection (PDO)
├── index.php             # Main Dashboard & Navigation Portal
├── login.php             # User Registration & Account Creation Page
├── se connecter.php      # User Authentication / Login Form Page
├── account.php           # User Profile Management & Avatar Upload
├── planner.php           # Weekly Planner & Task Manager
├── calend.php            # Interactive Monthly Calendar View
├── pomodoro.php          # Pomodoro Focus Timer & Work Tracker
├── progress.php          # Progress Analytics & Performance Dashboard
├── summaries.php          # Summary PDF Upload & Module Management
├── gestion.php           # Module-based Summary Browser & Downloads
├── stydy methods.php     # Educational Guides for Study Methodologies
├── log_session.php       # AJAX Endpoint for Pomodoro Session Logging
├── log out.php           # Session Termination Handler
├── footer.php            # Shared Footer Component
├── database.sql          # SQL Schema & Table Structure Initialization
├── uploads/              # Directory for User Profile Photos
└── resumes_uploads/      # Directory for Uploaded PDF Course Summaries
```
---
## 🚀 Getting Started
Follow these steps to set up Thinky Winky locally on your machine.
### Prerequisites
Make sure you have a local Web Server environment installed:
- **WAMP** (Windows), **XAMPP** (Cross-platform), or **MAMP** (macOS)
- **PHP** 7.4 or higher
- **MySQL / MariaDB** 5.7 or higher
---
### Installation & Local Setup
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/thinkywinky.git
   ```
2. **Move to Web Server Directory:**
   - **WAMP:** `C:\wamp64\www\thinkywinky`
   - **XAMPP:** `C:\xampp\htdocs\thinkywinky`
3. **Create Upload Directories:**
   Ensure the following directories exist with write permissions:
   ```bash
   mkdir uploads
   mkdir resumes_uploads
   ```
---
### Database Configuration
1. **Start MySQL Server** via WAMP/XAMPP control panel.
2. Open **phpMyAdmin** (`http://localhost/phpmyadmin`) or your preferred MySQL client.
3. Import the included [`database.sql`](database.sql) file or run the query to create database `thinkywinky` and its tables.
4. Update `config.php` if your local MySQL settings differ:
   ```php
   $host = "localhost";
   $dbname = "thinkywinky";
   $username = "root";
   $password = ""; // Your MySQL password if any
   ```
---
## 🗄️ Database Schema
The database consists of 5 main tables:
```sql
CREATE DATABASE IF NOT EXISTS `thinkywinky`;
USE `thinkywinky`;
-- 1. Users Table
CREATE TABLE `users` (
  `id` INT AUTO_INCREMENT PRIMARY KEY,
  `name` VARCHAR(255) NOT NULL,
  `email` VARCHAR(255) NOT NULL UNIQUE,
  `password_hash` VARCHAR(255) NOT NULL,
  `filiere` VARCHAR(255) DEFAULT NULL,
  `photo` VARCHAR(255) DEFAULT NULL,
  `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP
);
-- 2. Modules Table
CREATE TABLE `modules` (
  `module_id` INT AUTO_INCREMENT PRIMARY KEY,
  `name` VARCHAR(255) NOT NULL,
  `user_id` INT DEFAULT NULL,
  `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP
);
-- 3. Summaries Table
CREATE TABLE `summaries` (
  `id` INT AUTO_INCREMENT PRIMARY KEY,
  `user_id` INT NOT NULL,
  `title` VARCHAR(255) NOT NULL,
  `module_id` INT NOT NULL,
  `file_path` VARCHAR(255) NOT NULL,
  `is_public` TINYINT(1) DEFAULT 0,
  `downloads_count` INT DEFAULT 0,
  `upload_date` DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (`module_id`) REFERENCES `modules`(`module_id`) ON DELETE CASCADE
);
-- 4. Weekly Plan / Tasks Table
CREATE TABLE `WeeklyPlan` (
  `id` INT AUTO_INCREMENT PRIMARY KEY,
  `user_id` INT NOT NULL,
  `week_start` DATE NOT NULL,
  `day_of_week` VARCHAR(50) DEFAULT NULL,
  `subject` VARCHAR(255) NOT NULL,
  `start_time` TIME DEFAULT NULL,
  `duration_minutes` INT NOT NULL DEFAULT 0,
  `notes` TEXT DEFAULT NULL,
  `completed` TINYINT(1) DEFAULT 0,
  `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP
);
- 5. Pomodoro Focus Sessions Table
CREATE TABLE `PomodoroSessions` (
  `id` INT AUTO_INCREMENT PRIMARY KEY,
  `user_id` INT NOT NULL,
  `duration_minutes` INT NOT NULL,
  `session_type` VARCHAR(50) DEFAULT 'Work',
  `module_id` VARCHAR(255) DEFAULT 'Général',
  `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP
);
```
---
## 💻 Usage Guide
1. Open your browser and navigate to `http://localhost/thinkywinky/`.
2. Register a new account or log in with your credentials.
3. Access the **Dashboard** to view your study calendar and quick metrics.
4. Go to **Planner** to map out your upcoming weekly subjects and tasks.
5. Launch the **Pomodoro Timer** during study hours to track focus time automatically.
6. Visit **Summaries** to upload or download PDF notes for your courses.
7. Monitor your progress via the **Progress** page to view time spent per subject.
---

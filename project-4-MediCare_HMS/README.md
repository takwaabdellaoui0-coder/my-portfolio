<div align="center">

# 🏥 MediCare HMS
### Modern Hospital Management System & Medical AI Assistant

<img src="https://img.shields.io/badge/Java-17-orange.svg?style=for-the-badge&logo=openjdk" alt="Java" />
<img src="https://img.shields.io/badge/JavaFX-21-blue.svg?style=for-the-badge&logo=javafx" alt="JavaFX" />
<img src="https://img.shields.io/badge/SQLite-3.44-lightgrey.svg?style=for-the-badge&logo=sqlite" alt="SQLite" />
<img src="https://img.shields.io/badge/Maven-3.8+-red.svg?style=for-the-badge&logo=apache-maven" alt="Maven" />
<img src="https://img.shields.io/badge/Architecture-MVC%20%2B%20DAO-brightgreen.svg?style=for-the-badge" alt="Architecture" />

<p>
<b>A full-featured desktop application built with JavaFX, designed to streamline clinical workflows: patient records, appointment scheduling, pharmacy inventory, and an integrated medical assistant.</b>
</p>

🔗 **[Live Demo](#)** &nbsp;•&nbsp; 📩 **Full source available on request**

<sub>Developed by <b>[Your Name]</b> • Academic Year 2025/2026</sub>

</div>

---

## 🌟 Overview

**MediCare HMS** modernizes hospital administration by covering the entire patient care lifecycle — from intake and doctor scheduling to electronic health records (EHR) and pharmacy inventory — in a single desktop application. Built with **JavaFX** and structured around **MVC + DAO** design patterns, it gives doctors and administrative staff a clean, focused interface for day-to-day clinical operations.

The problem it solves: hospital staff often juggle disconnected tools (paper records, spreadsheets, separate scheduling apps) for tasks that are deeply interrelated. MediCare HMS centralizes them so a patient's appointment, medical record, and prescription history are all one click apart.

---

## ✨ Key Features

### 📊 Dashboard
Real-time KPIs — patient count, today's appointments, low-stock medication alerts — giving staff an at-a-glance view of hospital activity.

### 🧑‍⚕️ Patient Management
Full patient records with search, intake forms, and history tracking.

### 🩺 Doctor Directory
Manage doctor profiles, specialties, and availability.

### 📅 Appointment Scheduling
Book, reschedule, and track appointments, linked directly to patient and doctor records.

### 📋 Electronic Health Records (EHR)
Centralized medical history per patient — diagnoses, visit notes, and treatment history.

### 💊 Pharmacy Inventory
Track medication stock levels with alerts for low inventory.

### 🤖 MediBot Assistant
A built-in conversational assistant that helps staff navigate the system and answer common questions — a custom chatbot engine rather than a generic FAQ widget.

---

## 🛠️ Architecture & Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 17 |
| UI | JavaFX 21 |
| Database | SQLite |
| Build tool | Maven |
| Pattern | MVC + DAO |

**Data flow:** JavaFX App → FXML/CSS (views) → Controllers → DAO layer → SQLite

The DAO layer isolates all database access behind a clean interface, so the UI and business logic never touch raw SQL directly — this made it straightforward to add new modules (like the pharmacy inventory) without touching existing data-access code.

*(Full database schema and DAO implementation details are kept in the private repository.)*

---

## 📸 Screenshots

*(Add screenshots of the dashboard, patient records, and MediBot here once uploaded)*

| Dashboard | Appointments | MediBot |
|---|---|---|
| ![](#) | ![](#) | ![](#) |

---

## 📬 Want to see the code?

The full source (DAO implementations, database schema, MediBot engine) is kept in a private repository. Happy to walk through it in an interview or share access on request.

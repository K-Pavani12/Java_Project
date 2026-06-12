# Java_Project
Hospital Management System
# 🏥 Hospital Management System

A simple **Hospital Management System** built using **Java (JDBC)** and **MySQL**.
This project allows users to manage patients, doctors, and appointments through a console-based interface.

---

## 📌 Features

* ➕ Add new patients
* 📋 View patient details
* 👨‍⚕️ View doctor details
* 📅 Book appointments
* ✅ Check doctor availability

---

## 🛠️ Technologies Used

* **Java (JDK 8 or above)**
* **JDBC (Java Database Connectivity)**
* **MySQL Database**
* **IntelliJ IDEA / Eclipse**

---

## 📂 Project Structure

```
HospitalManagementSystems/
│
├── HospitalManagementSystems.java   # Main class
├── Patient.java                     # Patient operations
├── Doctor.java                      # Doctor operations
└── database.sql                     # Database schema (optional)
```

---

## ⚙️ Setup Instructions

### 1️⃣ Install Requirements

* Install Java (JDK 8+)
* Install MySQL Server
* Install IntelliJ IDEA / Eclipse

---

### 2️⃣ Create Database

Run the following SQL in MySQL:

```sql
CREATE DATABASE hospital;

USE hospital;

CREATE TABLE patients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10)
);

CREATE TABLE doctors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE appointments (
    id INT AUTO_INCREMENT PRIMARY KEY,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE
);
```

---

### 3️⃣ Add MySQL Connector (IMPORTANT)

Download MySQL JDBC Driver:
https://dev.mysql.com/downloads/connector/j/

* Extract the ZIP
* Add `.jar` file to your project dependencies

---

### 4️⃣ Configure Database Connection

Update your credentials in:

```java
private static final String url = "jdbc:mysql://localhost:3306/hospital";
private static final String username = "root";
private static final String password = "your_password";
```

---

### 5️⃣ Run the Project

* Open project in IntelliJ/Eclipse
* Build the project
* Run `HospitalManagementSystems.java`

---

## ▶️ Sample Output

### 🟢 Main Menu

```
HOSPITAL MANAGEMENT SYSTEMS
1. Add patient
2. View patients
3. View Doctors
4. Book Appointment
5. Exit
Enter your Choice: 3
```

---

### 👨‍⚕️ View Doctors

```
Doctors:
+------------+-------------+----------------+
| Doctor Id  | Name        | Specialization |
+------------+-------------+----------------+
| 1          | Ravi Kumar  | Cardiologist   |
+------------+-------------+----------------+
| 2          | Anjali Mehta| Neurologist    |
+------------+-------------+----------------+
```

---

### 📋 View Patients

```
Patients:
+------------+-------------+------+--------+
| Patient Id | Name        | Age  | Gender |
+------------+-------------+------+--------+
| 1          | Ramesh      | 45   | Male   |
+------------+-------------+------+--------+
| 2          | Sita        | 30   | Female |
+------------+-------------+------+--------+
```

---

### 📅 Book Appointment

```
Enter Patient Id: 1
Enter Doctor Id: 2
Enter appointment date (YYYY-MM-DD): 2026-06-15

Appointment Booked!
```

---

### ❌ If Doctor Not Available

```
Doctor not available on this date!!!
```

---

## ⚠️ Common Errors & Fixes

### ❌ Error: `ClassNotFoundException: com.mysql.cj.jdbc.Driver`

✔ Fix: Add MySQL Connector JAR to project

---

### ❌ Error: `No suitable driver found`

✔ Fix: Check JDBC URL and ensure driver is added

---

### ❌ SQL Errors

✔ Ensure table names are correct (`appointments`, not misspelled)

---

## 🚀 Future Improvements

* GUI using Java Swing / JavaFX
* Admin login system
* Search & filter functionality
* Online appointment system

---

## 👩‍💻 Author

**Pavani**

---

## 📄 License

This project is for educational purposes.


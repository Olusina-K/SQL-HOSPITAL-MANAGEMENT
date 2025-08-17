# Hospital Management System (SQL)

This project is a **SQL Server database schema** designed to simulate the operations of a hospital management system. It demonstrates how to design tables, apply relationships, enforce constraints, insert sample data, and query information for real-world healthcare workflows.

## Project Contents
- **`SQL HOSPITAL MANAGEMENT.sql`** – the main script that:
  - Creates the database schema  
  - Defines tables with constraints and keys  
  - Inserts sample data  
  - Demonstrates data validation  
  - Runs example queries (joins, loops, updates, etc.)  

## Database Schema
The system includes the following entities:
- **Doctors** – basic doctor records (IDs, names, specialties, etc.)  
- **Patients** – personal details of patients  
- **Appointments** – links patients with doctors by date/time  
- **Prescriptions** – medicines prescribed to patients by doctors  

### Key Features
- **Primary Keys** and **Foreign Keys** for referential integrity  
- **CHECK** and **DEFAULT** constraints for data validation  
- **WHILE loops** for inserting/updating data dynamically  
- Example **JOIN queries** across multiple tables  

## Getting Started
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/hospital-management-sql.git
   cd hospital-management-sql

2. Open SQL HOSPITAL MANAGEMENT.sql in SQL Server Management Studio (SSMS) or another T-SQL compatible client.

3. Run the script step by step:

Create the database & tables

Insert data into tables

Execute queries to test the schema

📖 Example Usage
Join Query

Get all appointments with patient & doctor names:

SELECT a.AppointmentDate, d.DoctorName, p.PatientName
FROM Appointments a
JOIN Doctors d ON a.Doctor_ID = d.Doctor_ID
JOIN Patients p ON a.Patient_ID = p.Patient_ID;

WHILE Loop

Print even numbers between 1 and 50:

DECLARE @i INT = 2;
WHILE @i <= 50
BEGIN
    PRINT @i;
    SET @i = @i + 2;
END

**Future Enhancements**

Add billing & payments module

Implement stored procedures for reusable logic

Add triggers for automatic auditing

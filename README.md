# Advanced_Database_Project

# 🧠 Advanced SQL & Database Projects

### By: Siddharam Javalkoti | MCA

🗕️ Date: 2026

This portfolio showcases two comprehensive projects using **Advanced SQL** for data querying, wrangling, transformation, and reporting. Each project reflects practical applications of relational databases, designed to demonstrate robust database skills for solving real-world problems using PostgreSQL and Microsoft SQL Server.

---

## 🗂️ Project 1: Staff Management and HR Data Reporting

### 🔎 Overview:

This project simulates a **relational HR database** system comprising multiple tables (e.g., staff, department, roles, grade level). Advanced SQL was used to extract operational and strategic insights, such as workforce distribution, salary forecasting, and departmental staff breakdowns.

### 🛠️ Tools & Technologies:

* **Database Engine:** PostgreSQL / SQL Server
* **Key Concepts:** Joins, Views, CASE statements, Aggregations, Nested Queries

### 📌 Key Tasks:

* Created joined views between **staff** and **department** tables to list all employees and roles.
* Counted staff per department using `GROUP BY` and filtered using `HAVING`.
* Used `CASE` statements to segment salary bands (e.g., staff earning above £50,000).
* Generated department-wise headcounts, total salary forecasts, and pay structure views.
* Demonstrated proper use of **aliases**, **ordering**, and **labeling** for reports.

### 📸 Suggested Screenshots (Place in `/Photo/StaffManagement/`)

* Staff by Department Summary
* Salary Band Classification Using CASE
* View Showing Department and Grade Level
* SQL Code for Staff Aggregation

### ✅ Sample Output (SQL Logic Abstracted):

```sql
SELECT d.name AS department, COUNT(s.id) AS total_staff,
       SUM(s.salary) AS total_salary
FROM staff s
JOIN department d ON s.dept_id = d.id
GROUP BY d.name
HAVING COUNT(s.id) > 3
ORDER BY total_salary DESC;
```

### 🌟 Outcomes:

* Demonstrated staff distribution across 5 departments
* Identified high-earning employees and their departments
* Built a salary forecasting query for HR planning

---

## 🗂️ Project 2: Public Health - Disease and Immunization Tracking Database

### 🔎 Overview:

This project used SQL to explore **disease surveillance and immunization data** stored across multiple relational tables. Queries were developed to identify at-risk populations, summarize immunization coverage, and analyze gender-based disease distributions.

### 🛠️ Tools & Technologies:

* **Database Engine:** SQL Server / PostgreSQL
* **Key Concepts:** Inner and Left Joins, Data Cleaning via SQL, Data Aggregation, Logical Filters

### 📌 Key Tasks:

* Combined **patients**, **diseases**, and **immunization** tables for integrated reporting
* Queried counts of immunized vs. non-immunized individuals per region
* Filtered patients under age 5 with incomplete immunization records
* Analyzed gender distribution of reported cases
* Used nested queries to compute counts for endemic disease incidence
* Aggregated disease outbreak data per Local Government Area (LGA)

### 📸 Suggested Screenshots (Place in `/Photo/PublicHealth/`)

* Disease Count by LGA
* Immunization Status Report
* SQL Joins Across Health Tables
* Breakdown by Age Group & Gender

### ✅ Sample Output (SQL Logic Abstracted):

```sql
SELECT l.lga_name, COUNT(d.disease_id) AS disease_cases
FROM disease_cases d
JOIN lga l ON d.lga_id = l.id
WHERE d.year = 2023
GROUP BY l.lga_name;
```

### 🌟 Outcomes:

* Summarized immunization status across 15 regions
* Identified LGAs with highest disease burdens
* Tracked gender disparities in disease reporting
* Enabled actionable insights for public health officials

---

## 🧂 Skills Demonstrated

* Advanced Joins (INNER, LEFT, FULL)
* Use of Views and Aliases
* Logical Filtering with `CASE`, `WHERE`, `HAVING`
* Grouped Aggregations (`COUNT`, `SUM`, `AVG`)
* Parameterized Queries and Nested SELECTs
* Data Cleaning and Filtering Using SQL Logic

---

## 📦 Folder Structure

```plaintext
/Advanced_SQL_Projects/
|
├── README.md
├── /Photo/
│   ├── StaffManagement/
│   │   ├── salary_case_query.png
│   │   ├── staff_by_dept.png
│   └── PublicHealth/
│       ├── disease_by_lga.png
│       ├── immunization_report.png
```

## ✅ Summary

These SQL projects demonstrate:

* **Strong command of database logic**
* **Practical application of joins and aggregates**
* **Industry-relevant datasets (HR & Health)**
* Readiness for roles requiring database querying, BI, and analytics

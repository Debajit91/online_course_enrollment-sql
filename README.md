Online Course Enrollment Database

A relational SQL project that models an online course enrollment platform.
The database supports students, courses, and enrollment transactions with realistic constraints, pricing, progress tracking, and reporting queries.

📦 Project Overview

This project demonstrates:

✔ Relational database design
✔ Foreign key–based table relationships
✔ Data insertion and constraint validation
✔ Aggregations & analytics using SQL
✔ JOIN variations for contextual data
✔ Pagination and filtering
✔ NULL handling & cleanup operations
✔ Practical reporting queries

Designed with real-world database behavior in mind.

🗂 Database Schema

The system contains three core entities:

1. students

Stores student profiles.
Attributes:

student_id (PK)

first_name

last_name

email

phone (nullable)

country

enrollment_date

2. courses

Stores course catalog information.
Attributes:

course_id (PK)

course_title

category

price (DECIMAL)

instructor

published_year

3. enrollments

Bridge table linking students ↔ courses.
Attributes:

enrollment_id (PK)

student_id (FK → students)

course_id (FK → courses)

enrollment_date

progress_percentage (nullable)

paid_amount (DECIMAL)

The schema enforces referential integrity through foreign key constraints.

🧾 Sample Dataset

Inserted data simulates a realistic platform:

✔ 10 students from 5+ countries
✔ 8 courses across 6 categories
✔ 15 enrollments with payment + progress fields
✔ NULL values for incomplete data (phone/progress)

This allows testing analytics, revenue summaries, and behavioral patterns.

🛠 SQL Features Demonstrated

This project utilizes:

Data definition (DDL)
✓ CREATE TABLE
✓ PK / FK / NOT NULL / NULL
✓ DECIMAL precision
✓ VARCHAR sizing

Data manipulation (DML)
✓ INSERT
✓ UPDATE
✓ DELETE

Data querying (DQL)
✓ SELECT with conditions
✓ ORDER BY + LIMIT
✓ Pagination (LIMIT + OFFSET)
✓ GROUP BY + HAVING
✓ COALESCE for NULL substitution
✓ AVG, SUM, COUNT, ROUND
✓ EXTRACT(YEAR) for date analytics

JOIN types
✓ INNER JOIN
✓ LEFT JOIN
✓ RIGHT JOIN
✓ FULL OUTER JOIN

Integrity reasoning
✓ Explanation of FK violations for invalid inserts

📊 Practice Outputs / Query Capabilities

The database supports:

✔ Top courses by price
✔ Yearly enrollment statistics
✔ Category-wise revenue
✔ Course enrollment counts
✔ Average student progress (ignoring NULL)
✔ Students without enrollments (LEFT JOIN)
✔ Courses without enrollments (RIGHT JOIN)
✔ Full student-course matrix (FULL JOIN)

📄 Example Learning Outcomes

By completing this project you can:

✓ Design normalized relational schemas
✓ Apply FK constraints properly
✓ Combine multiple JOINs for contextual insights
✓ Handle NULL data safely
✓ Write analytical SQL for reporting dashboards
✓ Use SQL to implement pagination
✓ Modify and clean data using UPDATE / DELETE
✓ Think like a backend engineer working with relational data

🚀 Running the Project

Import schema.sql to create tables

Run insert_data.sql to populate dataset

Execute queries from queries.sql for analytics & reporting

Compatible with:
• PostgreSQL
• Beekeeper Studio
• psql CLI
• Any SQL-compliant environment

💡 Why This Project Matters

This project mirrors real-world backend scenarios such as:

✔ EdTech platforms (Coursera, Udemy, Skillshare)
✔ Billing & transaction systems
✔ Student information systems
✔ Admin dashboards for course analytics

Engineers routinely perform this kind of reporting, cleanup, and integrity validation in production systems.

🧑‍💻 Tech Stack

PostgreSQL (SQL engine)

Beekeeper Studio (database client)

Git + GitHub (version control)

📁 Repository Structure (suggested)
/schema.sql
/insert_data.sql
/queries.sql
/README.md

📎 Author

Developed by Debajit
SQL • Data Modeling • Backend Logic • Relational Thinking

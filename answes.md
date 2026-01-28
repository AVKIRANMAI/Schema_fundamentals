# Schema Design Fundamentals – Theory

## 1. What is schema design and what does a database schema represent?

Schema design is the process of planning and organizing how data will be stored in a relational database. It defines the structure of the database before any data is added or any backend code is written.

A database schema represents:

* The tables in the database
* The columns in each table
* Data types of the columns
* Rules and constraints on the data
* Relationships between tables

For example, in a student management system, the schema defines a `students` table with columns like `id`, `name`, `email`, and `age`, along with rules such as making `id` unique.

In simple terms, a database schema is the blueprint of the database.

---

## 2. Why schema design is required before writing backend code?

Schema design is required before writing backend code because backend applications depend on the database structure. The backend needs to know what tables exist, what columns they have, and what type of data they store.

If schema design is not done first:

* Backend code may break due to mismatched data types
* Changes in database structure will require rewriting backend logic
* Data validation becomes difficult

Designing the schema first ensures smooth backend development, fewer errors, and better application stability.

---

## 3. How poor schema design impacts data consistency, maintenance, and scalability?

Poor schema design leads to several problems:

### Data Consistency

When the same data is stored in multiple places, updates may not happen everywhere, leading to inconsistent data.

Example: A user’s email stored in multiple tables may differ if updated incorrectly.

### Maintenance

Poorly designed schemas are hard to understand and modify. Even small changes require updates in many places, increasing the risk of errors.

### Scalability

As data grows, poorly designed databases become slow and inefficient. Adding new features or handling more users becomes difficult.

Good schema design avoids these issues and ensures long-term reliability.

---

## 4. What are validations in schema design and why databases enforce them?

Validations are rules applied to database columns to ensure only correct and meaningful data is stored.

Common validations include:

* **NOT NULL**: Ensures a column cannot have empty values
* **UNIQUE**: Prevents duplicate values
* **DEFAULT**: Assigns a default value if none is provided
* **PRIMARY KEY**: Uniquely identifies each record

Databases enforce validations to:

* Maintain data accuracy
* Prevent invalid data entry
* Reduce errors in applications
* Protect data integrity

---

## 5. Difference between a database schema and a database table

A database schema is the overall design of the database, while a database table is a structure that stores actual data.

The schema defines how tables are created and related, whereas tables store rows and columns of real data.

Simply put, schema is the plan and table is the implementation of that plan.

---

## 6. Why should a table represent only one entity?

An entity is a real-world object such as a student, course, or employee.

Each table should represent only one entity because:

* It keeps data organized
* Reduces redundancy
* Makes updates and queries easier
* Follows normalization principles

For example, student details should be stored in a `students` table and course details in a separate `courses` table.

---

## 7. Why should redundant or derived data be avoided in table design?

Redundant data means storing the same data in multiple places, which wastes space and causes inconsistencies.

Derived data is data that can be calculated from existing values, such as total marks from individual subject marks.

Storing redundant or derived data:

* Increases storage usage
* Causes update anomalies
* Leads to incorrect results

Instead, such data should be calculated when needed.

---

## 8. Importance of choosing correct data types while designing tables

Choosing correct data types is essential for efficient database performance and data accuracy.

Examples:

* Use INTEGER for age
* Use TEXT for names
* Use DATE for birthdates
* Use BOOLEAN for true or false values

Correct data types:

* Save storage space
* Improve query performance
* Prevent invalid data
* Ensure compatibility with backend code

---

## Conclusion

Schema design is a fundamental step in relational database development. A well-designed schema ensures data consistency, easy maintenance, scalability, and smooth backend integration. Proper schema design makes databases reliable and efficient for long-term use.

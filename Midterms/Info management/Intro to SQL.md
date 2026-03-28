# 🧾 Introduction to SQL (Structured Query Language)

## 🧠 What is SQL?

**SQL (Structured Query Language)** is a standard language used to:

* 📊 Manage data in relational databases
* 🔍 Retrieve information
* ✍️ Insert, update, and delete data
* 🏗️ Define database structures

In simpler terms:

> SQL is how you *boss around a database politely.*

---

# 🏛️ What is a Database?

A **database** is an organized collection of data stored in tables.

Think:

* 📁 Database = folder
* 📄 Table = spreadsheet
* 🧍 Row = record
* 📌 Column = attribute

---

# 📊 Basic SQL Structure

A typical SQL query looks like:

```sql
SELECT column_name
FROM table_name
WHERE condition;
```

Translation:

> “Give me this data from that table, but only if I feel like it.”

---

# 🧱 Core SQL Commands (CRUD)

## 🟢 1. SELECT (Read data)

```sql
SELECT * FROM students;
```

* Retrieves all data from `students`

```sql
SELECT name FROM students;
```

* Gets only names

---

## 🟡 2. INSERT (Add data)

```sql
INSERT INTO students (name, age)
VALUES ('Ali', 17);
```

👉 Adds a new record into the table

---

## 🟠 3. UPDATE (Modify data)

```sql
UPDATE students
SET age = 18
WHERE name = 'Ali';
```

⚠️ Without `WHERE`, everything gets updated. Yes, everything. Congratulations.

---

## 🔴 4. DELETE (Remove data)

```sql
DELETE FROM students
WHERE name = 'Ali';
```

⚠️ No `WHERE` = table goes bye-bye.

---

# 🧩 SQL Data Types

Common types:

* `INT` → whole numbers
* `VARCHAR(n)` → text
* `DATE` → dates
* `FLOAT` → decimals
* `BOOLEAN` → true/false

Example:

```sql
CREATE TABLE students (
    id INT,
    name VARCHAR(50),
    age INT
);
```

---

# 🏗️ Creating Tables

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
```

### Key idea:

* **PRIMARY KEY** = unique identifier

---

# 🔗 Filtering Data (WHERE)

```sql
SELECT * FROM students
WHERE age > 16;
```

Operators:

* `=` equal
* `>` greater than
* `<` less than
* `!=` not equal

---

# 🔍 Sorting Data (ORDER BY)

```sql
SELECT * FROM students
ORDER BY age ASC;
```

* `ASC` = ascending
* `DESC` = descending

---

# 🧮 Aggregation Functions

Used to summarize data:

| Function | Meaning        |
| -------- | -------------- |
| COUNT()  | number of rows |
| SUM()    | total          |
| AVG()    | average        |
| MAX()    | highest value  |
| MIN()    | lowest value   |

Example:

```sql
SELECT AVG(age) FROM students;
```

---

# 🔄 GROUP BY

Used to group data:

```sql
SELECT age, COUNT(*)
FROM students
GROUP BY age;
```

👉 “How many students per age?”

---

# 🔗 JOINs (Database Social Life)

Used to combine tables.

## INNER JOIN

```sql
SELECT students.name, courses.course_name
FROM students
INNER JOIN courses
ON students.id = courses.student_id;
```

👉 Only matching records show up

---

## LEFT JOIN

* All left table data + matching right table

---

## RIGHT JOIN

* Opposite of LEFT JOIN

---

## FULL JOIN

* Everything from both sides

---

# 🧠 Quick Summary

SQL lets you:

* 📥 Get data → `SELECT`
* ➕ Add data → `INSERT`
* ✏️ Change data → `UPDATE`
* ❌ Remove data → `DELETE`
* 🏗️ Build structure → `CREATE`

---

# 💡 Key Insight

SQL is basically:

> “I will ask nicely for data, and the database will either cooperate or pretend I didn’t ask correctly.”

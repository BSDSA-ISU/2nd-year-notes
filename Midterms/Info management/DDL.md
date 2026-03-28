# 🏗️ SQL DDL (Data Definition Language) — Final Reviewer

---

## 🧠 What is DDL?

**DDL (Data Definition Language)** is used to define and manage database structures like:

* 📦 Tables
* 🧱 Schemas
* 🔑 Constraints
* 🗂️ Indexes

In plain terms:

> DDL is how you design the “containers” before stuffing them with data.

---

# 🧾 Core DDL Commands

## 🏗️ 1. CREATE

Used to create databases, tables, views, etc.

### 📌 Create Database

```sql
CREATE DATABASE school;
```

### 📌 Create Table

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
```

👉 This defines structure, not data.

---

## ✏️ 2. ALTER

Used to modify existing structures.

### 📌 Add a column

```sql
ALTER TABLE students
ADD email VARCHAR(100);
```

### 📌 Modify a column

```sql
ALTER TABLE students
MODIFY age INT;
```

### 📌 Drop a column

```sql
ALTER TABLE students
DROP COLUMN email;
```

Translation:

> “Oops, I changed my mind about the database again.”

---

## ❌ 3. DROP

Used to completely remove a table or database.

### 📌 Drop table

```sql
DROP TABLE students;
```

### 📌 Drop database

```sql
DROP DATABASE school;
```

⚠️ Warning:

> This deletes everything. No recycle bin. No forgiveness. Just regret.

---

## 🧹 4. TRUNCATE

Removes all rows but keeps the structure.

```sql
TRUNCATE TABLE students;
```

### Difference from DELETE:

* `DELETE` → removes row by row (can use WHERE)
* `TRUNCATE` → wipes everything instantly

👉 Think:

> DELETE = careful eraser
> TRUNCATE = factory reset button

---

# 🔐 Constraints (Very Important in DDL)

Constraints define rules for data integrity.

## 📌 PRIMARY KEY

* Uniquely identifies each row
* Cannot be NULL

```sql
id INT PRIMARY KEY
```

---

## 📌 FOREIGN KEY

Links two tables.

```sql
FOREIGN KEY (student_id)
REFERENCES students(id)
```

👉 Ensures relational consistency.

---

## 📌 NOT NULL

Prevents empty values

```sql
name VARCHAR(50) NOT NULL
```

---

## 📌 UNIQUE

No duplicates allowed

```sql
email VARCHAR(100) UNIQUE
```

---

## 📌 DEFAULT

Sets a default value

```sql
status VARCHAR(20) DEFAULT 'active'
```

---

## 📌 CHECK

Adds conditions

```sql
age INT CHECK (age >= 0)
```

---

# 🧠 Summary Table

| Command  | Purpose                      |
| -------- | ---------------------------- |
| CREATE   | Make new structures          |
| ALTER    | Modify existing structures   |
| DROP     | Delete structures completely |
| TRUNCATE | Remove all data only         |

---

# ⚡ DDL vs Other SQL Types

| Type | Purpose                               |
| ---- | ------------------------------------- |
| DDL  | Defines structure                     |
| DML  | Handles data (INSERT, UPDATE, DELETE) |
| DQL  | Queries data (SELECT)                 |
| DCL  | Controls permissions                  |
| TCL  | Manages transactions                  |

---

# 💡 Final Insight

DDL is basically:

> “I decide how the database exists. The data just follows my architectural decisions like it has no choice.”

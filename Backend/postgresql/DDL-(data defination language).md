## 🔹 1. DDL (Data Definition Language)

👉 Defines database structure (tables, schema)

Commands:

- `CREATE`
- `ALTER`
- `DROP`
- `TRUNCATE`
- `RENAME`

---

# 📘 DDL Commands (Detailed with Examples)

---

## 🔹 1. CREATE

👉 Used to create database objects like tables

### ✅ Example: Create Table

```
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  age INT,
  email VARCHAR(100) UNIQUE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 🔍 Explanation:

- `SERIAL` → auto-increment id
- `PRIMARY KEY` → unique identifier
- `NOT NULL` → must have value
- `UNIQUE` → no duplicate emails
- `DEFAULT` → auto insert time

---

## 🔹 2. ALTER

👉 Used to modify table structure

### ✅ Example 1: Add Column

```
ALTER TABLE students
ADD address TEXT;
```

👉 Adds new column `address`

---

### ✅ Example 2: Modify Column Type

```
ALTER TABLE students
ALTER COLUMN age TYPE BIGINT;
```

👉 Changes `age` data type

---

### ✅ Example 3: Drop Column

```
ALTER TABLE students
DROP COLUMN address;
```

👉 Removes column permanently

---

## 🔹 3. DROP

👉 Deletes entire object (table/database)

### ✅ Example:

```
DROP TABLE students;
```

### 🔍 Explanation:

- Table + all data = deleted
- Cannot recover easily

---

## 🔹 4. TRUNCATE

👉 Removes all rows quickly

### ✅ Example:

```
TRUNCATE TABLE students;
```

### 🔍 Explanation:

- Deletes all records
- Faster than `DELETE`
- Structure remains

---

## 🔹 5. RENAME

👉 Change name of table

### ✅ Example:

```
ALTER TABLE students
RENAME TO learners;
```

👉 Table name becomes `learners`

---

# 📘 Full Flow Example (Real Scenario)

```
-- Create table
CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50),
  salary NUMERIC(10,2)
);

-- Add column
ALTER TABLE employees
ADD department VARCHAR(50);

-- Change column type
ALTER TABLE employees
ALTER COLUMN salary TYPE BIGINT;

-- Rename table
ALTER TABLE employees
RENAME TO staff;

-- Delete all data
TRUNCATE TABLE staff;

-- Drop table
DROP TABLE staff;
```

---

# ✅ Key Differences

- `DROP` ❌ removes structure + data
- `TRUNCATE` ❌ removes only data
- `ALTER` ✏️ modifies structure
- `CREATE` ➕ creates new
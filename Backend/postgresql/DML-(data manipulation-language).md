# 📘 DML (Data Manipulation Language)

👉 Used to **insert, update, delete data inside tables**  
👉 Does **NOT change structure**, only data

### 🔹 Main Commands:

- `INSERT`
- `UPDATE`
- `DELETE`

---

## 🔹 1. INSERT

👉 Used to add new data (rows)

### ✅ Example 1: Insert single row

```
INSERT INTO students (name, age, email)
VALUES ('John', 20, 'john@gmail.com');
```

### 🔍 Explanation:

- Adds one new record
- Column order must match values

---

### ✅ Example 2: Insert multiple rows

```
INSERT INTO students (name, age)
VALUES 
('Alice', 22),
('Bob', 25);
```

👉 Inserts multiple rows at once

---

### ✅ Example 3: Insert without column names

```
INSERT INTO students
VALUES (1, 'Sam', 21, 'sam@gmail.com');
```

👉 Must follow exact table column order

---

## 🔹 2. UPDATE

👉 Used to modify existing data

### ✅ Example 1: Update specific row

```
UPDATE students
SET age = 23
WHERE name = 'Alice';
```

### 🔍 Explanation:

- `WHERE` is important
- Updates only matching row

---

### ✅ Example 2: Update multiple columns

```
UPDATE students
SET age = 24, email = 'alice_new@gmail.com'
WHERE id = 2;
```

---

### ⚠️ Without WHERE

```
UPDATE students
SET age = 30;
```

👉 Updates **ALL rows** (dangerous)

---

## 🔹 3. DELETE

👉 Used to remove data (rows)

### ✅ Example 1: Delete specific row

```
DELETE FROM students
WHERE id = 1;
```

👉 Deletes only that row

---

### ⚠️ Delete all rows

```
DELETE FROM students;
```

👉 Removes all records (but table remains)

---

# 📘 Full Flow Example

```
-- Insert data
INSERT INTO students (name, age)
VALUES ('John', 20), ('Alice', 22);

-- Update data
UPDATE students
SET age = 21
WHERE name = 'John';

-- Delete data
DELETE FROM students
WHERE name = 'Alice';
```

---

# ✅ Key Points

- `INSERT` ➕ add data
- `UPDATE` ✏️ change data
- `DELETE` ❌ remove data
- `WHERE` ⚠️ controls which rows affected
# 📘 SQL Constraints (PostgreSQL)

👉 Constraints are rules applied on table columns  
👉 Ensure **data accuracy, integrity, and consistency**

---

# 🔹 Types of Constraints

- `NOT NULL`
- `UNIQUE`
- `PRIMARY KEY`
- `FOREIGN KEY`
- `CHECK`
- `DEFAULT`

---

## 🔹 1. NOT NULL

👉 Column cannot store NULL values

### ✅ Example:

```
CREATE TABLE users (
  name VARCHAR(50) NOT NULL
);
```

🔍 👉 Every row must have `name`

---

## 🔹 2. UNIQUE

👉 No duplicate values allowed

### ✅ Example:

```
CREATE TABLE users (
  email VARCHAR(100) UNIQUE
);
```

🔍 👉 Same email cannot be inserted twice

---

## 🔹 3. PRIMARY KEY

👉 Unique + NOT NULL (combined)

### ✅ Example:

```
CREATE TABLE users (
  id SERIAL PRIMARY KEY
);
```

🔍 👉 Identifies each row uniquely

---

## 🔹 4. FOREIGN KEY

👉 Links two tables

### ✅ Example:

```
CREATE TABLE orders (
  id SERIAL PRIMARY KEY,
  user_id INT,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
```

🔍 👉 `user_id` must exist in `users` table

---

## 🔹 5. CHECK

👉 Adds custom condition

### ✅ Example:

```
CREATE TABLE students (
  age INT CHECK (age >= 18)
);
```

🔍 👉 Only age ≥ 18 allowed

---

## 🔹 6. DEFAULT

👉 Sets default value

### ✅ Example:

```
CREATE TABLE users (
  is_active BOOLEAN DEFAULT TRUE
);
```

🔍 👉 If no value given → TRUE

---

# 📘 Combined Example

```
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(100) UNIQUE,
  age INT CHECK (age >= 18),
  is_active BOOLEAN DEFAULT TRUE
);
```

👉 Multiple constraints used together

---

# 📘 Add Constraint (ALTER)

```
ALTER TABLE students
ADD CONSTRAINT unique_email UNIQUE (email);
```

👉 Add constraint later

---

# 📘 Remove Constraint

```
ALTER TABLE students
DROP CONSTRAINT unique_email;
```

👉 Delete constraint

---

# ✅ Key Points

- `NOT NULL` → must have value
- `UNIQUE` → no duplicates
- `PRIMARY KEY` → unique identity
- `FOREIGN KEY` → relation between tables
- `CHECK` → custom rule
- `DEFAULT` → auto value

# ⚡ Simple Idea

👉 Constraints = **“rules for clean data”**
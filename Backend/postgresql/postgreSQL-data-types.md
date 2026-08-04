# 📘 PostgreSQL Data Types

## 🔹 1. Numeric Types

Used to store numbers.

- `INT` → whole numbers
- `BIGINT` → large integers
- `SERIAL` → auto-increment
- `NUMERIC(p,s)` → exact decimal

**Example:**

```
CREATE TABLE marks (
  id SERIAL,
  score INT,
  price NUMERIC(10,2)
);
```

👉 `SERIAL` auto increases  
👉 `NUMERIC` used for money (no rounding error)

---

## 🔹 2. Character Types

Used for text.

- `CHAR(n)` → fixed length
- `VARCHAR(n)` → limited text
- `TEXT` → unlimited

**Example:**

```
CREATE TABLE users (
  name VARCHAR(50),
  bio TEXT
);
```

👉 `VARCHAR` saves space  
👉 `TEXT` has no limit

---

## 🔹 3. Boolean Type

Stores true/false.

- `BOOLEAN`

**Example:**

```
CREATE TABLE status (
  is_active BOOLEAN
);
```

👉 Values: `TRUE`, `FALSE`, `NULL`

---

## 🔹 4. Date & Time Types

Used for date/time.

- `DATE`
- `TIME`
- `TIMESTAMP`

**Example:**

```
CREATE TABLE events (
  event_date DATE,
  created_at TIMESTAMP
);
```

👉 `TIMESTAMP` stores both date + time

---

## 🔹 5. UUID Type

Stores unique IDs.

- `UUID`

**Example:**

```
CREATE TABLE orders (
  id UUID
);
```

👉 Used for secure unique identifiers

---

## 🔹 6. JSON Types

Stores JSON data.

- `JSON`
- `JSONB` (better performance)

**Example:**

```
CREATE TABLE products (
  info JSONB
);
```

👉 `JSONB` is faster and indexed

---

## 🔹 7. Array Type

Stores multiple values in one column.

**Example:**

```
CREATE TABLE students (
  marks INT[]
);
```

👉 Can store: `{80, 90, 100}`

---

## 🔹 8. ENUM Type

Custom fixed values.

**Example:**

```
CREATE TYPE mood AS ENUM ('happy', 'sad');

CREATE TABLE person (
  feeling mood
);
```

👉 Only allowed values can be inserted

---

## 🔹 9. Binary Data

Stores files/data.

- `BYTEA`

**Example:**

```
CREATE TABLE files (
  data BYTEA
);
```

👉 Used for images, files

---

## 🔹 10. Special Types

Advanced use.

- `INET` → IP address
- `TSVECTOR` → full-text search

**Example:**

```
CREATE TABLE logs (
  ip INET
);
```

---

# ✅ Quick Summary

- Numbers → `INT`, `NUMERIC`
- Text → `VARCHAR`, `TEXT`
- Boolean → `TRUE/FALSE`
- Date → `DATE`, `TIMESTAMP`
- Advanced → `JSONB`, `ARRAY`, `UUID`
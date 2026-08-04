# 📘 DQL (Data Query Language)

👉 Used to **retrieve/fetch data from database**  
👉 Main command: **`SELECT`**

---

# 📘 SELECT (Basic Syntax)

```
SELECT column_name
FROM table_name;
```

👉 Fetch specific column(s)

---

## 🔹 1. Select All Data

```
SELECT * FROM students;
```

🔍 👉 `*` means all columns

---

## 🔹 2. Select Specific Columns

```
SELECT name, age FROM students;
```

👉 Only shows selected columns

---

## 🔹 3. WHERE (Filtering)

```
SELECT * FROM students
WHERE age > 20;
```

🔍 👉 Filters rows based on condition

---

## 🔹 4. AND / OR

```
SELECT * FROM students
WHERE age > 20 AND name = 'John';
```

👉 Combine conditions

---

## 🔹 5. ORDER BY (Sorting)

```
SELECT * FROM students
ORDER BY age DESC;
```

👉 `ASC` (default) / `DESC`

---

## 🔹 6. LIMIT

```
SELECT * FROM students
LIMIT 5;
```

👉 Returns first 5 rows

---

## 🔹 7. DISTINCT

```
SELECT DISTINCT age FROM students;
```

👉 Removes duplicate values

---

## 🔹 8. Aggregate Functions

- `COUNT()`
- `SUM()`
- `AVG()`
- `MAX()`
- `MIN()`

```
SELECT COUNT(*) FROM students;
```

👉 Counts rows

---

## 🔹 9. GROUP BY

```
SELECT age, COUNT(*)
FROM students
GROUP BY age;
```

👉 Groups same values

---

## 🔹 10. HAVING

```
SELECT age, COUNT(*)
FROM students
GROUP BY age
HAVING COUNT(*) > 2;
```

👉 Filter grouped data

---

# 📘 JOIN (Very Important)

👉 Used to combine multiple tables

---

## 🔹 11. INNER JOIN

```
SELECT s.name, c.course_name
FROM students s
INNER JOIN courses c
ON s.id = c.student_id;
```

👉 Only matching data

---

## 🔹 12. LEFT JOIN

```
SELECT s.name, c.course_name
FROM students s
LEFT JOIN courses c
ON s.id = c.student_id;
```

👉 All students + matching courses

---

## 🔹 13. RIGHT JOIN

```
SELECT s.name, c.course_name
FROM students s
RIGHT JOIN courses c
ON s.id = c.student_id;
```

👉 All courses + matching students

---

# 📘 Full Example

```
SELECT name, age
FROM students
WHERE age > 18
ORDER BY age DESC
LIMIT 5;
```

👉 Filter + sort + limit combined

---

# ✅ Key Points

- `SELECT` → fetch data
- `WHERE` → filter
- `ORDER BY` → sort
- `GROUP BY` → group
- `JOIN` → combine tables

---

# ⚡ Simple Idea

👉 DQL = **“Ask database questions”**  
Example:

- Who are students above 20?
- How many students?
- Which course belongs to whom?
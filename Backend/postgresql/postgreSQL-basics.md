## ✅ PostgreSQL Basic Complete List

Let’s go step-by-step from the very beginning of PostgreSQL 🔥

---

# 🧠 Step 0: CREATE DATABASE

## ✅ Code

```
CREATE DATABASE mydb;
```

## 🔍 Explanation

👉 This creates a new database

## 📦 Real-life analogy

👉 Like creating a project folder

---

## 🔌 Connect to Database

```
\c mydb;
```

👉 Entered into the database

---

# 🧠 Step 1: CREATE TABLE

## ✅ Code

```
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT
);
```

## 🔍 Explanation

👉 Created a table named `users`

## 📦 Real-life analogy

👉 Like creating an Excel sheet

---

# 🧠 Step 2: INSERT DATA

## ✅ Code

```
INSERT INTO users (name, age)
VALUES ('Pobi', 20);
```

## 🔍 Explanation

👉 Inserted new data

## 📦 Result

|id|name|age|
|---|---|---|
|1|Pobi|20|

---

# 🧠 Step 3: SELECT (View Data)

## ✅ Code

```
SELECT * FROM users;
```

## 🔍 Explanation

👉 Shows all data

---

## 🎯 Specific Column

```
SELECT name FROM users;
```

👉 Shows only the `name` column

---

# 🧠 Step 4: INSERT Multiple Data

## ✅ Code

```
INSERT INTO users (name, age)
VALUES 
('Rahim', 25),
('Karim', 30);
```

## 🔍 Explanation

👉 Insert multiple rows at once

---

# 🧠 Step 5: WHERE (Filter)

## ✅ Code

```
SELECT * FROM users
WHERE age > 22;
```

## 🔍 Explanation

👉 Shows users whose age is greater than 22

---

# 🧠 Step 6: UPDATE

## ✅ Code

```
UPDATE users
SET age = 26
WHERE name = 'Rahim';
```

## 🔍 Explanation

👉 Updates Rahim’s age

---

# 🧠 Step 7: DELETE

## ✅ Code

```
DELETE FROM users
WHERE name = 'Karim';
```

## 🔍 Explanation

👉 Deletes Karim

---

# 🧠 Step 8: ORDER BY

## ✅ Code

```
SELECT * FROM users
ORDER BY age DESC;
```

## 🔍 Explanation

👉 Shows highest age first

---

# 🧠 Step 9: LIMIT

## ✅ Code

```
SELECT * FROM users
LIMIT 2;
```

## 🔍 Explanation

👉 Shows only 2 rows

---

# 🧠 Step 10: DROP TABLE

## ✅ Code

```
DROP TABLE users;
```

## 🔍 Explanation

👉 Deletes the table

---

# ⚡ Final Simple Map

👉 CREATE DATABASE → Create a project  
👉 CREATE TABLE → Define structure  
👉 INSERT → Add data  
👉 SELECT → View data  
👉 UPDATE → Modify data  
👉 DELETE → Remove data
# 🧠 psql Must-Use Commands

---

### `\l` → List Databases

👉 Shows all databases in your PostgreSQL server  
👉 Useful when you want to choose or confirm DB name before connecting

---

### `\c mydb` → Connect Database

👉 Switches your session to `mydb`  
👉 After this, all queries run inside this database

---

### `\conninfo` → Connection Info

👉 Displays current database, user, host, port  
👉 Good for checking “am I in the right DB?”

---

### `\dt` → List Tables

👉 Shows all tables inside current database (usually in `public` schema)  
👉 Helps you quickly see what tables exist

---

### `\d users` → Table Structure

👉 Shows columns, data types, primary key, indexes  
👉 Very important to understand table design before writing queries

---

### `SELECT * FROM users;` → View Data

👉 Fetches all rows and columns from `users` table  
👉 Most used command to check or debug data

---

### `\x` → Expanded View

👉 Displays each row vertically instead of horizontally  
👉 Useful when rows have many columns or long text

---

### `\timing` → Query Time

👉 Turns ON/OFF execution time display  
👉 Helps detect slow queries

---

### `\du` → Roles / Users

👉 Lists all roles (users) and their permissions  
👉 Useful for access control checking

---

### `\i file.sql` → Run SQL File

👉 Executes all SQL commands from a file  
👉 Commonly used for setup, migrations, or bulk queries

---

### `\q` → Exit

👉 Quits the psql terminal  
👉 Ends your session safely

---

# ⚡ Daily Workflow (Real Use)

👉 Typical flow while working:

```
\l → \c mydb → \dt → \d users → SELECT * FROM users;
```

👉 Meaning:

- choose DB
- enter DB
- check tables
- understand structure
- read data
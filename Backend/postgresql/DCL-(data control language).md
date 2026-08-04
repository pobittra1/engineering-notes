# 📘 DCL (Data Control Language)

👉 Used to **control access/permissions** in database  
👉 Works with **users & roles**

### 🔹 Main Commands:

- `GRANT`
- `REVOKE`

---

## 🔹 1. GRANT

👉 Gives permission to a user/role

### ✅ Example 1: Grant SELECT permission

```
GRANT SELECT ON students TO user1;
```

### 🔍 Explanation:

- `user1` can now read data
- Cannot modify data

---

### ✅ Example 2: Grant multiple permissions

```
GRANT INSERT, UPDATE ON students TO user1;
```

👉 User can now add & modify data

---

### ✅ Example 3: Grant all permissions

```
GRANT ALL PRIVILEGES ON students TO user1;
```

👉 Full access to table

---

### ✅ Example 4: Grant on all tables

```
GRANT SELECT ON ALL TABLES IN SCHEMA public TO user1;
```

👉 Access to all tables in schema

---

## 🔹 2. REVOKE

👉 Removes permission

### ✅ Example 1: Revoke SELECT

```
REVOKE SELECT ON students FROM user1;
```

👉 User can no longer read data

---

### ✅ Example 2: Revoke all permissions

```
REVOKE ALL PRIVILEGES ON students FROM user1;
```

👉 Removes everything

---

# 📘 Full Flow Example

```
-- Give permissions
GRANT SELECT, INSERT ON students TO user1;

-- Remove one permission
REVOKE INSERT ON students FROM user1;

-- Remove all permissions
REVOKE ALL PRIVILEGES ON students FROM user1;
```

---

# 📘 Common Privileges

- `SELECT` → read data
- `INSERT` → add data
- `UPDATE` → modify data
- `DELETE` → remove data
- `ALL PRIVILEGES` → full access

---

# ✅ Key Points

- `GRANT` ➕ give access
- `REVOKE` ❌ remove access
- Works with users/roles
- Controls database security
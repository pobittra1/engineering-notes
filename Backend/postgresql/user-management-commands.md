# 🧠 🔐 USER / ROLE COMMANDS (Complete Practical Set)

---

# 🔹 1. Create

### Create user

```
CREATE USER pobi WITH PASSWORD '1234';
```

👉 Basic user create

---

### Create role (advanced)

```
CREATE ROLE dev WITH LOGIN PASSWORD '1234';
```

👉 Same as user, but more flexible

---

# 🔹 2. View

### List users

```
\du
```

👉 See all roles + permissions

---

# 🔹 3. Grant Permissions

### DB access

```
GRANT ALL PRIVILEGES ON DATABASE mydb TO pobi;
```

👉 Full DB access

---

### Table access

```
GRANT SELECT, INSERT, UPDATE ON users TO pobi;
```

👉 Specific permissions

---

### All tables (important 🔥)

```
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO pobi;
```

👉 Future + existing tables access

---

# 🔹 4. Revoke

```
REVOKE ALL ON DATABASE mydb FROM pobi;
```

👉 Remove access

---

# 🔹 5. Role Modify

### Make admin

```
ALTER ROLE pobi WITH SUPERUSER;
```

---

### Remove admin

```
ALTER ROLE pobi WITH NOSUPERUSER;
```

---

### Change password

```
ALTER USER pobi WITH PASSWORD 'newpass';
```

---

# 🔹 6. Delete

```
DROP USER pobi;
```

👉 Remove user

---

# 🔹 7. Role Membership (VERY IMPORTANT 🔥)

### Create group role

```
CREATE ROLE dev_team;
```

---

### Add user to role

```
GRANT dev_team TO pobi;
```

👉 pobi inherits permissions

---

### Remove from role

```
REVOKE dev_team FROM pobi;
```

---

# 🔹 8. Login Test

```
psql -U pobi -d mydb
```

👉 check login works

---

# ⚡ 🔥 Real World Setup

```
CREATE USER pobi WITH PASSWORD '1234';
GRANT ALL PRIVILEGES ON DATABASE mydb TO pobi;
GRANT ALL ON ALL TABLES IN SCHEMA public TO pobi;
```

👉 fully working user setup

---

# 🧠 Final Answer

👉 **Yes — 90% work ends with these:**

- CREATE USER / ROLE
- GRANT
- ALTER ROLE
- DROP USER
- \du

👉 Extra (pro level):

- role groups (`GRANT role TO user`)
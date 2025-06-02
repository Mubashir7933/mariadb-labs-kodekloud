# Day 02 – Creating Database, User, and Granting Permissions

**Module:** [Creating Database, User and Granting Permissions]

## 🧠 What I Learned
- How to create a new MariaDB database using SQL.
- Adding new users and defining access rules.
- Understanding `GRANT` and `FLUSH PRIVILEGES`.

## 🧪 Commands Practiced
```sql
CREATE DATABASE sales_data;
GRANT ALL PRIVILEGES ON sales_data.* TO 'lab_user'@'localhost' IDENTIFIED BY 'test123';
FLUSH PRIVILEGES;

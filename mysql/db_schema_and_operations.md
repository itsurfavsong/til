# 🧩 Database Setup and Operations

1. Database Operations <br>

1-1. Create Database
```sql
CREATE DATABASE mydb;
```
1-2. Select Database
```sql
USE mydb;
```
1-3. Drop Database
```sql
DROP DATABASE mydb;
```
---
2. Schema: CREATE, ALTER, DROP

```sql
CREATE TABLE users(
    id BIGINT unsigned PRIMARY KEY auto_increment,
    `name` VARCHAR(50) NOT NULL COMMENT 'Name',
    gender CHAR(1) NOT NULL COMMENT 'F for female, M for male (uppercase), N for not selected',
    created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(),
    updated_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP(),
    deleted_at DATETIME
);
```
---
3. Alter Table Operations

---
4. Delete Tables

4-1. Drop Table
4-2. Truncate Table (Delete All Data)

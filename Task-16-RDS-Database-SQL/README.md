# Task 16: RDS Database + SQL Workbench Connection & Queries

##  Objective
To create and connect to an AWS RDS MySQL database and execute basic SQL queries using MySQL Workbench.

---

## 🛠 Services Used
- Amazon RDS (MySQL)
- EC2 Security Groups
- MySQL Workbench
- AWS VPC (Default)

---

##  Step 1: Create RDS Database

1. Open AWS Console → RDS → Create Database
2. Selected:
   - Engine: MySQL Community
   - Instance type: db.t4g.micro (Free Tier)
   - Public access: Enabled
3. Created master username and password
4. Launched database

Database status changed to **Available**

---

##  Step 2: Configure Security Group

1. Open EC2 → Security Groups
2. Edit inbound rules
3. Added rule:
   - Type: MySQL / Custom TCP
   - Port: 3306
   - Source: My IP

Saved rules successfully.

---

##  Step 3: Connect Using MySQL Workbench

1. Open MySQL Workbench
2. Create new connection
3. Enter:
   - Hostname: RDS Endpoint
   - Port: 3306
   - Username: sujan
4. Enter password and connect successfully

---

## Step 4: Execute SQL Queries

```sql
CREATE DATABASE studentdb;
USE studentdb;

CREATE TABLE students (
  id INT PRIMARY KEY,
  name VARCHAR(50),
  age INT
);

INSERT INTO students VALUES (1,'Rahul',22);
INSERT INTO students VALUES (2,'Anita',23);

SELECT * FROM students;

# Task 17: DynamoDB Table Creation (Basic)

##  Objective
To create a NoSQL table using Amazon DynamoDB and insert sample items to understand serverless database basics.

---

##  Services Used
- Amazon DynamoDB
- AWS Management Console

---

##  Step 1: Create DynamoDB Table

1. Open AWS Console
2. Navigate to DynamoDB → Tables
3. Click "Create table"
4. Enter the following details:

   - Table name: StudentsTable
   - Partition key: StudentID (String)
   - Capacity mode: On-demand (Default settings)

5. Click "Create table"

The table status changed to **Active**.

---

##  Step 2: Insert Sample Items

1. Open StudentsTable
2. Click "Explore items"
3. Click "Create item"
4. Add the following items:

### Item 1
- StudentID: S1
- Name: Rahul
- Age: 20

### Item 2
- StudentID: S2
- Name: Anita
- Age: 19

Both items were successfully inserted into the table.

---

## Proof of Work

1. Screenshot showing table status as Active.
2. Screenshot showing inserted items (S1 and S2).

---

##  Outcome

Successfully created a DynamoDB table and inserted sample records using AWS Management Console.

---

##  Cleanup

The DynamoDB table was deleted after completion to avoid unnecessary billing.

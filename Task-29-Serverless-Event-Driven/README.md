# Task 5 – Serverless + Event Driven Architecture (AWS + Azure)

## Objective

The objective of this task is to implement an event-driven serverless architecture using:

* Storage triggers
* Serverless compute services
* Managed NoSQL databases
* Monitoring services

This project demonstrates how cloud-native event-driven systems work across **AWS and Azure platforms**.

---

# AWS Implementation

##  Architecture Overview

S3 Bucket → Lambda Function → DynamoDB → CloudWatch Logs

When a file is uploaded to S3:

1. S3 triggers a Lambda function.
2. Lambda processes the event.
3. Data is stored in DynamoDB.
4. Logs are recorded in CloudWatch.

---

##  AWS Services Used

* Amazon S3
* AWS Lambda
* Amazon DynamoDB
* Amazon CloudWatch

---

## Implementation Steps

### Created S3 Bucket

* Bucket configured for event notifications.
* Upload action triggers Lambda.

###  Created Lambda Function

* Runtime: Python
* IAM Role attached with:

  * DynamoDB write permissions
  * CloudWatch logging permissions

###  Configured S3 Trigger

* Event type: Object Created (PUT)
* Linked to Lambda function.

###  DynamoDB Table

* Table Name: `task5-table`
* Partition Key: `id (String)`
* Capacity Mode: On-demand

### Monitoring

* Verified execution logs inside CloudWatch.
* Confirmed successful execution and duration metrics.

---

## AWS Verification

--> File upload successfully triggered Lambda
--> CloudWatch logs generated
--> Items inserted into DynamoDB
--> No execution errors

---

#  Azure Implementation

##  Architecture Overview

Azure Blob Storage → Azure Function → Cosmos DB

When a blob is uploaded:

1. Blob Storage triggers Azure Function.
2. Function processes the file.
3. Data is stored in Azure Cosmos DB.

---

##  Azure Services Used

* Azure Storage Account (Blob)
* Azure Function (Blob Trigger)
* Azure Cosmos DB (NoSQL API)

---

##  Implementation Steps

### Created Storage Account

* Blob storage enabled
* Public access configured for testing

###  Created Blob Container

* Used for uploading test files

###  Created Azure Function

* Trigger type: Blob Trigger
* Runtime: Python
* Connected to Storage Account

### Created Cosmos DB Account

* API: Azure Cosmos DB for NoSQL
* Capacity Mode: Serverless
* Backup Policy: Periodic
* Key-based authentication enabled

### Connected Function to Cosmos DB

* Used connection string from Cosmos DB
* Inserted JSON document upon file upload

---

## Azure Verification

--> Blob upload triggered Azure Function
--> Function execution successful
--> Documents inserted into Cosmos DB
--> No runtime errors

---

# Cost Consideration

This implementation uses:

* AWS Free Tier eligible services
* Azure Free Trial / Serverless mode
* On-demand billing models
* No provisioned throughput

All services were configured to avoid unnecessary charges.

---


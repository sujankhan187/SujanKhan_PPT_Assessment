# Task 11: S3 Upload Email Notification (Lambda + SNS)

## Objective
Trigger email notification when file is uploaded to S3.

## Services Used
- Amazon S3
- AWS Lambda
- Amazon SNS

## Architecture
S3 → Lambda → SNS → Email

## Steps
1. Created SNS topic
2. Confirmed email subscription
3. Created Lambda function
4. Attached SNS & S3 IAM permissions
5. Added SNS publish code
6. Created S3 bucket
7. Added S3 trigger
8. Uploaded file

## Result
Email notification is successfully received when file is uploaded to S3.

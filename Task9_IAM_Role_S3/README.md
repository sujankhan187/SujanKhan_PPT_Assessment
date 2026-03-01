# Task 9: Access S3 from Ubuntu using IAM Role

## Objective
To securely access Amazon S3 from EC2 using IAM Role instead of access keys.

## Services Used
- IAM
- EC2
- S3
- AWS CLI

## Steps Performed
1. Created IAM role for EC2.
2. Attached AmazonS3FullAccess policy.
3. Attached role to EC2 instance.
4. Installed AWS CLI on Ubuntu.
5. Verified S3 access using `aws s3 ls`.

## Verification
- IAM role attached successfully.
- No access keys configured.
- S3 buckets listed from EC2 terminal.

## Outcome
Successfully accessed S3 from EC2 using IAM Role following AWS best practices.

# Task 10: VPC 3-Tier Architecture

## Objective
To design and implement a secure 3-tier architecture in AWS using public and private subnets, Internet Gateway, NAT Gateway, route tables, and EC2 instances.

## Services Used
- Amazon VPC
- Internet Gateway
- NAT Gateway
- Route Tables
- Amazon EC2

## Steps Performed

### 1. Created VPC
- Created VPC with CIDR block: 10.0.0.0/16
- Enabled DNS support

### 2. Created Subnets
- Public Subnets (for Web Tier)
- Private Subnets (for App Tier)

### 3. Internet Gateway
- Created and attached Internet Gateway to VPC
- Public route table configured:
  0.0.0.0/0 → Internet Gateway

### 4. NAT Gateway
- Created NAT Gateway in public subnet
- Private route table configured:
  0.0.0.0/0 → NAT Gateway

### 5. EC2 Instances

#### Web Tier
- Launched in public subnet
- Public IP enabled
- Security group allows SSH and HTTP from internet

#### App Tier
- Launched in private subnet
- No public IP assigned
- Security group allows SSH only from Web Tier

## Result
Successfully implemented secure 3-tier architecture with proper public and private subnet isolation and controlled access using route tables and security groups.

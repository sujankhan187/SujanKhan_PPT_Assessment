# Task 13: Start/Stop EC2 using Lambda + API Gateway

##  Objective
Automate EC2 instance start and stop using AWS Lambda triggered via API Gateway.

---

##  Services Used
- AWS Lambda
- Amazon API Gateway
- Amazon EC2
- IAM

---

##  Architecture
API Gateway → Lambda Function → EC2 Instance

---

##  How It Works

1. API Gateway exposes endpoint:
   ```
   /ec2
   ```

2. Query parameter controls action:
   ```
   ?action=start
   ?action=stop
   ```

3. Lambda function reads query parameter and:
   - Starts EC2 instance
   - Stops EC2 instance

---

##  API Endpoint Example

Start Instance:
```
https://your-api-id.execute-api.us-east-1.amazonaws.com/ec2?action=start
```

Stop Instance:
```
https://your-api-id.execute-api.us-east-1.amazonaws.com/ec2?action=stop
```

---

## Result
Successfully automated EC2 instance control using serverless architecture.

# Task 14: CloudWatch Alarm (70% CPU → Auto Stop + Email)

## Objective
To create a CloudWatch alarm that monitors EC2 CPU utilization.
If CPU usage exceeds 70%, the instance will:
- Send email notification (SNS)
- Automatically stop the EC2 instance

## Services Used
- EC2
- CloudWatch
- SNS

## Configuration Details
- Metric: CPUUtilization
- Threshold: Greater than 70%
- Evaluation Period: 1 minute
- SNS Topic: cpualerttopic
- EC2 Action: Stop this instance
- Region: us-east-1 (N. Virginia)

## Proof
- Screenshot 1: Alarm state showing OK
- Screenshot 2: Alarm configuration showing threshold, SNS, and EC2 stop action

## Result
The alarm successfully monitors CPU usage and is configured to send email and stop the instance when CPU exceeds 70%.

# Task 12 – CloudWatch Website Monitoring using Synthetics Canary

## Objective
To monitor a website using Amazon CloudWatch Synthetics Canary and configure a CloudWatch Alarm to send email notifications using Amazon SNS when failures occur.

---

## Services Used
- Amazon CloudWatch Synthetics
- CloudWatch Alarms
- Amazon SNS
- IAM

---

## Implementation Steps

1. Created a Synthetics Canary named `website-monitor-canary`
2. Configured runtime as `syn-nodejs-puppeteer-14.0`
3. Enabled screenshot capture
4. Configured the canary to monitor a website endpoint
5. Created a CloudWatch Alarm:
   - Namespace: CloudWatchSynthetics
   - Metric: Failed Requests
   - Threshold: Greater than 0
6. Configured SNS topic for email notification
7. Confirmed email subscription
8. Verified alarm state (OK)

---


Successfully implemented website monitoring using CloudWatch Synthetics Canary with automated alerting through CloudWatch Alarm and SNS email notifications.

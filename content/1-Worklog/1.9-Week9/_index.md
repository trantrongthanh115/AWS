---
title: "Week 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

**Weekly objectives:**
- Create a Python-based AWS Lambda function to generate sales predictions.
- Load model parameters dynamically from S3 inside the serverless runtime.
- Deploy API Gateway mappings to expose inference routes as a REST API.
- Set up an Amazon EventBridge schedule to automate daily batch forecasts.
- Verify execution triggers and output logging in CloudWatch.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Created the `forecast-lambda` function and associated IAM policies for S3 read access. | Jun 15 |
| Tuesday | Developed the Lambda inference logic to load `model.pkl` from S3 and run predictions. | Jun 16 |
| Wednesday | Integrated API Gateway to map HTTP routes (e.g., `/predict`) to the Lambda function. | Jun 17 |
| Thursday | Configured an Amazon EventBridge cron trigger to automate daily batch forecasts at 12:00 AM UTC. | Jun 18 |
| Friday | Executed end-to-end serverless inference integration tests and audited CloudWatch logs. | Jun 19 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Deployed Lambda infrastructure and attached secure S3 read policies.
  - Lesson: Implementing least-privilege IAM policies prevents unauthorized read/write access to model repositories.
- **Tuesday:**
  - Result Achieved: Coded and deployed python prediction handler, optimizing memory limits.
  - Lesson: Loading model weights outside the main handler loop eliminates redundant S3 calls during concurrent executions.
- **Wednesday:**
  - Result Achieved: API Gateway endpoint active. Verified response payloads using cURL.
  - Lesson: API Gateway simplifies serverless integration, providing automated CORS and request throttling configurations.
- **Thursday:**
  - Result Achieved: EventBridge Scheduler cron successfully registered and active.
  - Lesson: Automating cron jobs using EventBridge eliminates the need to run and patch cron servers, cutting cloud expenses.
- **Friday:**
  - Result Achieved: Monitored successful triggers and verified that daily batch forecast outputs populate tables.
  - Lesson: CloudWatch Logs provide detailed execution timings, allowing developers to optimize Lambda memory and runtime allocations.

---
title: "Week 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

**Weekly objectives:**
- Register and configure a new AWS account, obtaining $100 in initial credits from the program.
- Complete 5 practical tasks on the AWS Console to earn an extra $100 promotional credit ($20 per task).
- Gain initial familiarity with 5 foundational AWS services: EC2, Bedrock, Budgets, Lambda, and RDS.
- Understand the basics of AWS billing controls, security configurations, and resource cleanup.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Account Registration & Security setup. Configured Multi-Factor Authentication (MFA) for root account, created IAM admin user and group. | Apr 20 |
| Tuesday | Task 1: Deployed, verified, and terminated a test Amazon EC2 Virtual Machine (`FCA-Test-Server`) using custom RSA Key Pairs. | Apr 21 |
| Wednesday | Task 2: Configured model access for Claude 3 Haiku in Amazon Bedrock and executed prompts inside the Text Playground. | Apr 22 |
| Thursday | Task 3: Configured cost budget warning thresholds ($20 budget limit, alert at 80% actual spend) in AWS Budgets. | Apr 23 |
| Friday | Task 4 & 5: Deployed a serverless web app using AWS Lambda HTTP blueprint, and provisioned a managed PostgreSQL database in Amazon RDS. Completed teardown of all test instances. | Apr 24 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: AWS account activated, secured with MFA. Configured IAM users, assigning them to developer and admin groups with least-privilege permissions.
  - Lesson: Securing root access and using granular IAM users is the first line of defense in cloud security.
- **Tuesday:**
  - Result Achieved: Successfully launched and verified the status of a t3.micro EC2 instance, followed by immediate termination.
  - Lesson: Gained hands-on familiarity with the AWS Console interface and established the critical rule of immediately cleaning up practice resources to avoid billing surprises.
- **Wednesday:**
  - Result Achieved: Gained access to Claude 3 Haiku. Successfully verified text generation using the Bedrock text playground.
  - Lesson: Access to advanced AI models is governed by AWS's Responsible AI policies. Managed AI services abstract infrastructure complexity.
- **Thursday:**
  - Result Achieved: Configured billing warnings and automated cost notifications sent via Amazon SNS email alerts.
  - Lesson: Setting up a budget is the first line of defense in any cloud project, alerting you before costs accumulate over a month.
- **Friday:**
  - Result Achieved: Deployed a serverless Lambda HTTP function, verified the Function URL, provisioned a PostgreSQL database, and completed cleanup of both resources.
  - Lesson: Serverless scale-to-zero model keeps costs at $0 when inactive. RDS PostgreSQL databases have strict dependency chains and must have their instances removed before the cluster can be deleted.

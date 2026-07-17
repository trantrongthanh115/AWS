---
title: "Week 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

**Weekly objectives:**
- Implement a Multi-Level Monitoring System including three-tier Budgets and CloudWatch Billing Alarms.
- Configure AWS Cost Anomaly Detection and establish a resource tagging policy.
- Write and test CLI scripts to audit and clean up active, high-cost cloud resources.
- Study core cloud architecture models, global infrastructure, and security best practices.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Configured three-tier budgets (Monthly, Warning, Daily Safeguard) and set up CloudWatch Billing Alarms mapped to SNS email/SMS routing. | Apr 27 |
| Tuesday | Activated AWS Cost Anomaly Detection ($5 threshold) and established a standard Resource Tagging Scheme (`Project`, `Environment`, `Author`). | Apr 28 |
| Wednesday | Practiced AWS CLI commands to audit resources: identifying running EC2/RDS instances, unattached EBS volumes, and idle Elastic IPs. | Apr 29 |
| Thursday | Studied Cloud Computing characteristics (elasticity, OpEx vs. CapEx), compared service models (IaaS, PaaS, SaaS) and global infrastructure (Regions, AZs, Edge). | Apr 30 |
| Friday | Reviewed the AWS Shared Responsibility Model, IAM best practices (least privilege, MFA, JSON policies), and core storage concepts (S3 durability & classes). | May 01 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Active warning thresholds ($20 limit) and a daily $5 budget guardrail. CloudWatch alarms configured for multiple cost tiers.
  - Lesson: A daily budget alert acts as a rapid response checkpoint, detecting runaway resources within 24 hours.
- **Tuesday:**
  - Result Achieved: Enabled anomaly monitor targeting all AWS services. Applied resource tagging across test compute resources.
  - Lesson: Resource tagging ensures cost allocation reports in Cost Explorer remain clean, making tracking anomalies by project or author easy.
- **Wednesday:**
  - Result Achieved: Successfully ran CLI scripts using `aws ec2` and `aws rds` commands to discover idle or unattached billable resources.
  - Lesson: Developing an emergency runbook and knowing command line tools are essential for fast system restoration and cost-containment.
- **Thursday:**
  - Result Achieved: Completed service model documentation mapping AWS services to IaaS/PaaS/SaaS architectures.
  - Lesson: Deploying resources across different Availability Zones (AZs) guarantees high availability and disaster tolerance.
- **Friday:**
  - Result Achieved: Drafted a custom JSON IAM policy adhering to the principle of least privilege.
  - Lesson: Customer security IN the cloud (credential management, security groups) is a critical developer responsibility.

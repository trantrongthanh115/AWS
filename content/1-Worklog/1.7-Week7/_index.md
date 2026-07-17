---
title: "Week 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

**Weekly objectives:**
- Establish an automated big data ETL pipeline using AWS Glue.
- Create an IAM service execution role for AWS Glue with VPC routing policies.
- Configure and run the `Raw Ingestion` Glue Job to ingest transaction files into RDS.
- Configure and run the `Feature Engineering` Glue Job to extract time-series lag and rolling statistics.
- Verify job execution states and audit performance in CloudWatch.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday (Office visit) | Created an IAM service role for AWS Glue enabling access to S3, RDS, and CloudWatch log groups. | Jun 01 |
| Tuesday | Created Amazon S3 buckets to store raw CSV transactional data files. | Jun 02 |
| Wednesday | Configured the `Raw Ingestion` AWS Glue job, writing a PySpark script to load CSV data into `fashion-rds`. | Jun 03 |
| Thursday | Configured the `Feature Engineering` Glue job, writing PySpark logic to calculate 7-day lags and rolling averages. | Jun 04 |
| Friday | Executed the ETL pipeline jobs from the AWS Console and verified data population in the target databases. | Jun 05 |

**Weekly results achieved:**
- **Monday ( Office visit ):**
  - Result Achieved: Glue IAM role created. Configured permissions for VPC database subnet access.
  - Lesson: Glue jobs require explicit security policies to run network interfaces (ENIs) inside a private VPC.
- **Tuesday:**
  - Result Achieved: Landing zone buckets created. Verified upload of raw transaction logs.
  - Lesson: Using S3 as a landing zone decouples raw ingestion storage from transactional relational databases.
- **Wednesday:**
  - Result Achieved: Populated the operational database using PySpark Spark SQL JDBC connectors.
  - Lesson: Glue's PySpark scripts scale data processing workloads automatically, distributing records across cluster nodes.
- **Thursday:**
  - Result Achieved: Populated ML training tables with calculated lag columns and rolling transaction quantities.
  - Lesson: Pre-computing time-series features in Glue reduces model training times and keeps the ML compute instance efficient.
- **Friday:**
  - Result Achieved: Confirmed successful run states on the Glue Console and reviewed the Spark driver logs.
  - Lesson: Analyzing CloudWatch Logs is crucial for troubleshooting memory errors or connection issues in Spark jobs.

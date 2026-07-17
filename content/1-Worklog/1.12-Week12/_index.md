---
title: "Week 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

**Weekly objectives:**
- Conduct comprehensive end-to-end system testing of the retail portal.
- Record the live project walkthrough demo video and compile report media.
- Decommission all EC2 compute nodes, ASGs, Target Groups, and Load Balancers.
- Terminate all RDS PostgreSQL instances and clean up VPC subnet groups.
- Empty and delete S3 buckets, Glue ETL jobs, and Lambda functions to complete cleanup.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday | Tested all user scenarios (Admin, Manager, Associate) and verified that the prediction dashboards update correctly. | Jul 06 |
| Tuesday | Recorded the live project demo video and uploaded it to the shared repository. | Jul 07 |
| Wednesday | Initiated EC2 Cleanup: terminated instances, removed target groups, disabled ASGs, and deleted ALB routing rules. | Jul 08 |
| Thursday | Initiated RDS Cleanup: deleted database instances (`fashion-rds`, `training-db`) and deleted subnet group configurations. | Jul 09 |
| Friday | Cleared Amazon S3 buckets, deleted AWS Glue ETL job definitions, removed the Lambda API endpoints, and drafted the final report. | Jul 10 |

**Weekly results achieved:**
- **Monday:**
  - Result Achieved: Confirmed that authentication, user roles, and interactive predictive charts work without errors.
  - Lesson: End-to-end testing verifies that all decoupled systems integrate correctly before decommissioning.
- **Tuesday:**
  - Result Achieved: Compiled the demo video walk-through showing real-time forecasting.
  - Lesson: Documenting the functional system through videos provides lasting evidence of system execution.
- **Wednesday:**
  - Result Achieved: Compute resources removed, verified that no orphan EC2 instances remain.
  - Lesson: Disabling Auto Scaling groups before terminating instances prevents the group from launching new replacement VMs.
- **Thursday:**
  - Result Achieved: Relational database clusters terminated successfully, skipping final snapshots to avoid extra storage costs.
  - Lesson: Relational database instances continue to incur storage fees until they are completely deleted.
- **Friday:**
  - Result Achieved: Emptied and removed S3 buckets, Glue pipelines, and Lambda APIs. Completed the final internship report.
  - Lesson: Practicing complete infrastructure teardown is a key Cloud FinOps skill, preventing unexpected credit consumption.

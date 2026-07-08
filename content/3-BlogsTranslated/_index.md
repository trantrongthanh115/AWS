---
title: "Translated Blogs"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---



During my internship, I translated and summarized 5 AWS technical blogs covering key topics in data engineering, cloud storage, and database management. Each blog was selected because it aligns directly with the technologies and services I worked with throughout the program.

---

### [Blog 1 - Building a Real-time CDC Pipeline: From Amazon Aurora to Amazon S3 Tables with Debezium and Firehose](3.1-Blog1/)

This blog explores how to build a real-time Change Data Capture (CDC) pipeline that moves data from Amazon Aurora PostgreSQL to Amazon S3 Tables in Apache Iceberg format. It explains why separating OLTP and OLAP workloads is critical, how Debezium on MSK Connect captures database changes with minimal performance overhead, and how AWS Lambda acts as the transformation layer that maps Debezium operation codes to Firehose insert/update/delete actions. The article also introduces how S3 Tables automates snapshot management and compaction, enabling near-real-time analytics without impacting the source database.

---

### [Blog 2 - Data Governance on AWS: Ending the "Two-Place Permission" Headache for S3 and Lake Formation](3.2-Blog2/)

This blog introduces a new AWS feature that allows data scientists and ML engineers to access raw S3 files directly using their existing AWS Lake Formation permissions - eliminating the need to maintain separate IAM/S3 bucket policies alongside Lake Formation table permissions. The article covers how the new `GetTemporaryDataLocationCredentials()` API works, how a dedicated Java plugin automates credential issuance, and why this is a game-changer for Generative AI and ML training pipelines that need governed, direct access to data lake files.

---

### [Blog 3 - Migrating Data and Saving Costs at Scale with Amazon S3 File Gateway](3.3-Blog3/)

This blog addresses a common but often overlooked problem in cloud migrations: when files are moved from on-premises storage to Amazon S3 via S3 File Gateway, their original creation timestamps get reset - which breaks S3 Lifecycle Policies that depend on file age. The article presents an automated solution combining Robocopy, S3 File Gateway, and AWS Lambda to preserve original file metadata (timestamps, NTFS permissions) and automatically route files into the correct low-cost storage class (e.g., Glacier Deep Archive) based on their true age - optimizing storage costs at scale while supporting hybrid cloud access via SMB and NFS.


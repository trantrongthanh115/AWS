---
title: "Week 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

**Weekly objectives:**
- Launch a dedicated EC2 instance for machine learning training workloads.
- Write a Python ML training script connecting to `training-db` feature tables.
- Train and evaluate a regression-based fashion sales forecasting model.
- Measure validation metrics (MAE, RMSE) and export model parameters.
- Establish automated model export and storage in Amazon S3.

**Tasks to be deployed this week:**

| Day | Task | Date |
|---|---|---|
| Monday (Office visit) | Provisioned the `ML-Training-Server` EC2 instance, installing Python 3.10 and database drivers. | Jun 08 |
| Tuesday | Installed and configured the machine learning runtime library dependencies (Psycopg2, Pandas, Scikit-Learn). | Jun 09 |
| Wednesday | Wrote `train.py` to extract time-series feature variables from the PostgreSQL `training-db`. | Jun 10 |
| Thursday | Executed the training pipeline using a Scikit-Learn Random Forest Regressor, verifying MAE metrics. | Jun 11 |
| Friday | Added boto3 scripts to export the trained model (`model.pkl`) directly into the secure S3 model repository. | Jun 12 |

**Weekly results achieved:**
- **Monday ( Office visit ):**
  - Result Achieved: ML compute node running in VPC.
  - Lesson: Heavy mathematical computation should be confined to compute-optimized servers to protect production systems from CPU starvation.
- **Tuesday:**
  - Result Achieved: Configured python environment. Verified DB driver connections.
  - Lesson: Pinning library versions inside `requirements.txt` avoids dependency breakages during automated build steps.
- **Wednesday:**
  - Result Achieved: Built efficient database extraction queries, loading data batches into memory.
  - Lesson: Using indexed timestamp column filters minimizes database load and speeds up data ingestion.
- **Thursday:**
  - Result Achieved: Trained model successfully, achieving a Mean Absolute Error (MAE) within acceptable business thresholds.
  - Lesson: Evaluating models on split validation sets is critical to detect overfitting before production deployments.
- **Friday:**
  - Result Achieved: Verified model upload to S3, with object permissions configured for serverless access.
  - Lesson: Storing model files in S3 enables decoupled microservices to dynamically load models, eliminating compile dependencies.

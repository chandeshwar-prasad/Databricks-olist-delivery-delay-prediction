# Databricks-olist-delivery-delay-prediction
End-to-end Databricks Lakehouse project to predict e-commerce delivery delays using Medallion architecture, Delta Lake, and MLflow

## Databricks Lakehouse Project: Delivery Delay Prediction

## 📌 Problem Statement
Predict whether an e-commerce order will be delivered late using historical order, customer, and logistics data.

This helps businesses proactively communicate with customers and improve seller performance.

---

## Architecture
Implemented a Databricks **Medallion Architecture**:

- **Bronze**: Raw CSV ingestion into Delta tables
- **Silver**: Data cleaning, deduplication, joins, and business logic
- **Gold**: Analytics aggregates and ML feature tables

Unity Catalog is used for governance and lineage tracking.

---

## Data Engineering
- Apache Spark (PySpark)
- Delta Lake with ACID transactions
- Schema enforcement
- Delivery delay business logic:
  - `delivery_delay_days`
  - `is_delayed`

---

## Machine Learning
- ML task: Binary classification (delivery delayed or not)
- Model: Logistic Regression
- Feature engineering from Silver & Gold tables
- Experiment tracking using **MLflow**
- Predictions written back to Delta tables
- Model evaluation metrics: accuracy, precision, recall

---

## Orchestration
- End-to-end pipeline automated using **Databricks Jobs**
- Bronze → Silver → Gold → ML workflow

---

## Business Impact
- Predict delayed deliveries in advance
- Improve customer satisfaction
- Enable seller-level performance analysis

---

## Tech Stack
- Databricks
- Apache Spark
- Delta Lake
- Unity Catalog
- MLflow
- Python

---

## Notes
This project was built as part of the **Build With Databricks – Resume Project Challenge** by Codebasics & Indian Data Club.

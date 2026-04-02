# AWS Glue ETL Pipeline – Freelancers Dataset

## 📌 Overview

This project demonstrates a basic end-to-end ETL (Extract, Transform, Load) pipeline using AWS services. The pipeline ingests raw freelancer data from Amazon S3, processes it using AWS Glue (PySpark), and stores the transformed data back in S3 in an optimized format.

---

##  Architecture

S3 (Raw Data) → AWS Glue ETL Job → S3 (Processed Data)

---

## 🧰 Tech Stack

* AWS Glue (PySpark)
* Amazon S3
* AWS IAM
* Python

---

## 📂 Project Structure

```
aws-glue-etl-project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── glue/
│   └── freelancers_etl_job.py
│
├── notebooks/
│   └── exploration.ipynb
│
├── docs/
│   └── architecture.png
│
└── README.md
```

---

## 🔄 ETL Pipeline Flow

### 1. Extract

* Raw CSV data is stored in S3 (`raw-data/` folder)

### 2. Transform

* Handle missing values
* Rename columns
* Filter invalid records
* Add derived columns (e.g., `is_high_earner`)

### 3. Load

* Transformed data is written back to S3 in Parquet format (`processed-data/`)

---

## ⚙️ Setup Instructions

### Prerequisites

* AWS Account
* S3 bucket created
* IAM role with:

  * S3 access
  * Glue permissions
  * `iam:PassRole` permission

### Steps

1. Upload raw dataset to S3
2. Create a Glue job
3. Attach IAM role to Glue job
4. Upload ETL script to S3
5. Run the Glue job

---

## 📊 Sample Output

* Cleaned and transformed dataset stored in Parquet format
* Optimized for analytics workloads

---

## 🚧 Work in Progress

* Add partitioning for performance optimization
* Automate pipeline with triggers
* Add data quality checks

---

## 📚 Learnings

* Working with AWS Glue and PySpark
* Managing IAM roles and permissions
* Structuring data in S3 for ETL workflows

---

## 📎 Notes

This is a beginner-friendly project aimed at building foundational data engineering skills using AWS.


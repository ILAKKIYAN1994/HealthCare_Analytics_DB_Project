# 🏥 Databricks Lakehouse ML Project – End-to-End Readmission Prediction

This repository contains an **end-to-end Databricks Lakehouse project** that demonstrates how to design, build, and operationalize a **real-world analytics + machine learning solution** for **hospital readmission prediction**.

The project follows a **modern Lakehouse architecture** and has been **enhanced to support future predictions (risk scoring)**, making it suitable for **proactive decision-making**, not just historical analysis.

```
Configuration → Bronze → Silver → Gold → ML Model (Training + Future Scoring) → Dashboards (Historical + Predictive)
```

---

## 📂 Repository Structure

| Notebook                     | Purpose                                                  |
| ---------------------------- | -------------------------------------------------------- |
| `1. Configuration.ipynb`     | Environment setup and shared configurations              |
| `2. Bronze.ipynb`            | Raw data ingestion layer                                 |
| `3. Silver.ipynb`            | Cleaned and validated data layer                         |
| `4. Gold.ipynb`              | Business aggregates & ML-ready datasets                  |
| `5. ML Model.ipynb`          | Model training, evaluation **and future risk scoring**   |
| `6. Dashboard Queries.ipynb` | SQL analytics for **historical + predictive dashboards** |

---

## 1️⃣ Configuration Notebook

### 🎯 Objective

Provide a **centralized configuration layer** for catalogs, schemas, and reusable variables across the project.

### 🔑 Key Responsibilities

* Select catalog and schema
* Define table names and reusable paths
* Validate execution context

### ✅ Outcome

Consistent execution environment across all layers.

---

## 2️⃣ Bronze Layer – Raw Ingestion

### 🎯 Objective

Ingest raw source data into the Lakehouse **without altering business meaning**.

### 🔑 Key Responsibilities

* Read raw source data
* Append ingestion metadata
* Write Delta tables
* Maintain auditability

### 🧠 Design Principle

> Bronze data is raw, immutable, and replayable.

---

## 3️⃣ Silver Layer – Data Cleaning & Validation

### 🎯 Objective

Prepare **high-quality, trusted datasets** for analytics and machine learning.

### 🔑 Key Responsibilities

* Data type standardization
* Null handling and validation
* Deduplication
* Business rule enforcement
* Feature-ready transformations

### 🧠 Design Principle

> Silver data represents the analytical source of truth.

---

## 4️⃣ Gold Layer – Business & ML-Ready Data

### 🎯 Objective

Create **consumption-ready datasets** for reporting and ML.

### 🔑 Key Responsibilities

* Business aggregations
* Metric calculations
* ML-friendly feature tables
* Optimized schemas for performance

### 🧠 Design Principle

> Gold data directly answers business questions.

---

## 5️⃣ ML Model Notebook – Training & Future Risk Prediction (Updated)

### 🎯 Objective

Build, evaluate, and **apply machine learning models to both historical and future data**.

### 🔑 Key Responsibilities

* Feature engineering using Spark ML Pipelines
* Train/Test split
* Model training (Random Forest, Gradient Boosted Trees)
* Model evaluation using AUC, accuracy, precision, recall
* MLflow experiment tracking
* **Risk score inference using prediction probabilities**
* **Scoring future/unseen records**

### 🧠 Key Enhancements

* Extracted `risk_score` from model probability (`P(label = 1)`)
* Categorized risk levels (High / Medium / Low)
* Persisted prediction outputs as Gold tables

### ✅ Outcome

A **production-ready predictive model** capable of scoring new patient encounters and generating actionable risk insights.

---

## 6️⃣ Dashboard Queries – Historical & Predictive Insights (Updated)

### 🎯 Objective

Expose **both historical metrics and future ML predictions** through SQL analytics and dashboards.

### 🔑 Key Responsibilities

* Historical KPIs (readmission trends, volumes)
* Predictive KPIs (risk score distributions)
* High-risk patient identification
* SQL queries for dashboards
* Support filters and drill-downs

### 🧠 Example Predictive Insights

* Top high-risk patients
* Risk distribution by admission type
* Predicted vs actual readmissions
* Risk trends over time

### ✅ Outcome

Dashboards that support **proactive clinical and operational decision-making**.

---

## 🧠 End-to-End Architecture Summary

```
Raw Data
   ↓
Bronze (Raw Delta)
   ↓
Silver (Cleaned & Validated)
   ↓
Gold (Aggregates & ML Features)
   ↓
ML Models (Training + Risk Scoring)
   ↓
Dashboards (Historical + Predictive)
```

---

## 🚀 How Machine Learning Enhances This Project

* Moves analytics from descriptive → predictive
* Identifies high-risk patients before readmission occurs
* Generates probabilistic risk scores instead of binary outcomes
* Enables prioritization and early intervention
* Integrates seamlessly with Lakehouse architecture

---

## 📌 Key Skills Demonstrated

* Databricks Lakehouse Architecture
* Delta Lake & Spark SQL
* PySpark Data Engineering
* Spark ML Pipelines
* MLflow experiment tracking
* Predictive analytics & risk scoring
* SQL dashboards with ML insights

---

## ✨ Final Notes

This project now represents a **full decision intelligence system**:

* Historical reporting
* Predictive modeling
* Risk-based insights
* Dashboard-driven consumption

---

✨ *Built with Databricks, Spark, Delta Lake, MLflow, and SQL Analytics*

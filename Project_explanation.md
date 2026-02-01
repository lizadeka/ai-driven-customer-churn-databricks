## 🚀 AI-Driven Customer Churn Risk & Retention Decision System

Built on Databricks Lakehouse (Community Edition)

### 📌 Project Overview

This project demonstrates an end-to-end, real-world decision intelligence system built on the Databricks Lakehouse to identify customers at risk of churning and convert data insights into clear, explainable retention decisions.

Instead of focusing only on predictive modeling, the project emphasizes data engineering, analytics, and explainable decision logic — reflecting how many real organizations design churn systems before or alongside machine learning models.

---

### 🎯 Business Problem

Customer churn directly impacts revenue, growth, and customer lifetime value.
The key challenge is not just identifying churned customers after the fact, but proactively identifying high-risk customers early and deciding what action to take.

This project answers:

Which customers are at risk of churn?

What behavioral signals contribute to that risk?

How can churn risk be translated into actionable business decisions?

---

### 🧱 Architecture: Databricks Lakehouse Design

The solution follows a Bronze → Silver → Gold Lakehouse architecture.

#### 🟫 Bronze Layer — Raw Data Ingestion

Ingested raw telecom customer data from CSV

Preserved original schema and values

No transformations applied

Ensures traceability, auditability, and reprocessing capability

#### 🥈 Silver Layer — Cleaned & Standardized Data

Handled missing and malformed values (e.g. TotalCharges)

Corrected data types for analytics readiness

Standardized categorical values for consistency

Maintained row-level customer granularity

This layer serves as the single trusted source for both analytics and decision logic.

#### 🥇 Gold Layer — Decision & Insight Models

Instead of a single Gold table, the project implements multiple purpose-driven Gold layers.

#### 🔹 Gold Layer 1: Churn Risk Scoring (Explainable AI Logic)
📊 Rule-Based Churn Risk Model

An explainable churn risk scoring system was designed using business logic and domain knowledge.

Each customer receives a churn risk score based on behavioral and contractual signals such as:

Short tenure

Month-to-month contracts

High monthly charges

Fiber optic internet usage

Electronic payment methods

churn_risk_score =
    tenure risk +
    contract risk +
    service risk +
    payment risk +
    billing risk

#### 🔹 Gold Layer 2: Decision-Ready Risk Categorization

Risk scores are converted into business-ready churn segments:

HIGH_RISK

MEDIUM_RISK

LOW_RISK

This layer enables immediate operational decisions, not just analysis.

--- 

### 🧠 Decision Intelligence (Not Just Prediction)

This project intentionally focuses on decision logic over black-box prediction.

Why rule-based risk scoring?

High explainability and transparency

Easy validation by business stakeholders

Faster adoption in real organizations

Auditable and adjustable logic

Strong foundation for future ML integration

Many real churn systems use rule-based decision engines before or alongside machine learning models.

---

### 📈 Key Business Insights Generated

Distribution of customers across churn risk categories

Average tenure and billing behavior by risk group

Clear segmentation for targeted retention strategies

Identification of high-impact churn drivers

These insights directly support:

Retention campaigns

Pricing reviews

Contract strategy optimization

---

### 🛠️ Tools & Technologies Used

Databricks Community Edition

Delta Lake

Databricks SQL

PySpark

Lakehouse Architecture (Bronze / Silver / Gold)

---

### 🧠 Skills Demonstrated

End-to-end Lakehouse design

Data cleaning and transformation

SQL-based decision modeling

Explainable AI-inspired logic

Business-oriented data engineering

Analytics-to-decision pipeline design

---

### 🔮 Future Enhancements

This system is ML-ready by design. Future iterations can include:

Replacing rule-based scoring with predictive ML models

Spark ML or MLflow integration

Model explainability using SHAP or feature importance

Generative AI for churn insight summarization

Automated retention recommendation systems

--- 

### 💡 Key Takeaway

This project highlights that effective AI systems start with strong data engineering and clear decision logic.
By combining Lakehouse architecture with explainable churn risk modeling, the solution demonstrates how raw customer data can be transformed into trusted, actionable business decisions.

# AI-Driven Customer Churn Risk & Retention Decision System

## Overview

The project implements an AI-driven, explainable decision system using rule-based intelligence. The architecture is designed to be extensible to machine learning models in a full Databricks environment.
This project demonstrates an end-to-end, AI-driven customer churn risk and retention decision system built using the **Databricks Lakehouse architecture**.

---

## Business Problem
Customer churn is a critical challenge for subscription-based businesses. Reacting after customers leave is costly, so early and explainable risk detection is essential.

**Objective:**
- Identify customers at risk of churn
- Translate churn risk into actionable retention strategies

---

## Dataset
- **Telecom Customer Churn Dataset** (public dataset from Kaggle)
- Contains customer demographics, services, contract details, billing information, and churn labels

> Raw data is not included in this repository.

---

## Architecture
The solution follows the **Databricks Lakehouse** pattern:

**Bronze → Silver → Gold → Decision Layer**

- **Bronze:** Raw data ingestion (Delta format, no transformations)
- **Silver:** Data cleaning, type handling, and business-friendly structure
- **Gold (Analytics):** Churn KPIs and behavioral insights
- **Gold (Decision Layer):** AI-driven churn risk scoring and decision logic

---

## AI-Driven Decision Logic
Instead of relying only on black-box models, this project implements an **explainable, rule-based churn risk scoring system**.

Risk factors include:
- Customer tenure
- Contract type
- Internet service
- Payment method
- Monthly charges

Customers are categorized into:
- **High Risk**
- **Medium Risk**
- **Low Risk**

Each category maps directly to a retention action.

---

## Technologies Used
- Databricks Community Edition
- Apache Spark (PySpark & SQL)
- Delta Lake
- Lakehouse architecture principles

---

## Key Learnings
- Importance of strong data foundations before AI
- Value of explainable decision systems
- Designing AI solutions around business workflows
- Adapting solutions to platform constraints

---

## Design Considerations
This project was built using Databricks Community Edition, which has limited support for large Spark ML pipelines on serverless compute.

To ensure stability, explainability, and a complete end-to-end solution, the project implements an AI-driven, rule-based churn risk scoring system. This approach mirrors real-world industry practices where transparent decision logic is often used before or alongside machine learning models.

🔹 Lightweight ML Extension (Churn Prediction)

As an extension to the decision-first churn system, a lightweight churn prediction model was implemented using Spark ML.

Due to resource constraints in Databricks Community Edition, feature selection was intentionally applied to reduce categorical dimensionality.

A Logistic Regression model was trained using a reduced feature set and achieved an ROC-AUC of ~0.84, demonstrating strong predictive performance while maintaining pipeline stability.

---

## Future Enhancements
- Integrate machine learning models in a full Databricks environment
- Track experiments using MLflow
- Enable real-time churn scoring

---

## Folder Structure 

```sql

ai-driven-customer-churn-databricks/
│
├── notebooks/
│   |__ Bronze layer.ipynb
|   |__ Silver layer.ipynb
|   |__ Gold layer.ipynb
|   └── churn_risk_decision_logic.ipynb
│
├── presentation/
│   └── AI_Driven_Customer_Churn_System.pdf
│
├── images/
│   ├── architecture.png
│   └── churn_risk_flow.png
│
└── README.md

```

---

## Author
Built as a self-directed project to demonstrate real-world data engineering and AI decision system design.

# Carrier Performance & SLA Risk Intelligence Platform

## Project Overview
This project focuses on building a predictive decision-support system for Apex Manufacturing Ltd., a global B2B enterprise managing a 50M–200M annual logistics spend. The platform shifts logistics operations from reactive monitoring (identifying failures after they happen) to predictive intelligence (identifying risks before shipments are executed).
## Business Requirements & Context

Apex Manufacturing relies on multiple third-party logistics (3PL) carriers to ship goods across APAC, EMEA, and AMER. Each carrier operates under a Service Level Agreement (SLA) that specifies contractual delivery times.
The Problem
Rising Costs: SLA breaches result in 10%–20% penalty costs and customer churn.
Reactive Operations: Current monitoring relies on monthly scorecards that are backward-looking and poor at detecting early performance degradation.
Core Question: "Which carrier is likely to breach SLA in upcoming shipments, on which routes, and why?".
Expected Impact
SLA Breaches: Targeted reduction of 15–30%.
Penalty Costs: Targeted reduction of 10–20%.
## Project Objectives
The primary goal is to implement a predictive, explainable, and scalable platform that:
Evaluates carrier performance at the shipment, route, and regional levels.
Predicts SLA breach risk before a shipment is executed.
Provides actionable insights to the Head of Supply Chain, Procurement, and Finance teams to support evidence-based carrier selection.
## Tech Stack
Programming: Python (Pandas, NumPy) for data manipulation.

Analysis & ML: Scikit-learn (XGBoost, Random Forest), SHAP for model explainability.

Database: SQL for advanced querying and data extraction.

Visualization: Power BI (DAX, Power Query), Matplotlib, Seaborn, and Plotly.
## Project Roadmap (Steps Followed)
#### Phase 1: Data Preprocessing & Foundation (Completed)
Data Cleaning: Processed 200,000 shipment records, handling missing values, duplicates, and outliers (IQR method) to ensure a "trustworthy" dataset.
Target Creation: Engineered the  (1 if  > , else 0)sla_breach_flagactual_daysplanned_days.
Encoding: Applied One-Hot Encoding to categorical variables (Vendor, Mode, Region, etc.) to prepare for Machine Learning.
#### Phase 2: Exploratory Data Analysis (EDA) & Executive Dashboarding (completed )
EDA: Identifying high-risk routes, problematic transport modes, and carrier-specific breach patterns.
Dashboard 1 (Executive Overview): Developing a Power BI dashboard focused on the "Cost vs. Reliability" trade-off and high-level SLA health.
#### Phase 3: Feature Engineering & Risk Logic
Risk Signals: Engineering advanced features like Carrier Rolling SLA Breach Rates (30/60/90 days) and Route Volatility Indices to detect patterns of failure over time.
#### Phase 4: Machine Learning & Explainability
Modeling: Training and evaluating classification models (Random Forest, XGBoost) to predict the probability of a breach.
Trustable AI: Utilizing SHAP values to provide business-friendly reasoning for every prediction, ensuring stakeholders understand the "why" behind the risk.
#  Dataset Overview
The platform utilizes a structurally realistic dataset mirroring enterprise Transportation Management System (TMS) exports:
Granularity: Shipment-level (One row = One shipment).
Coverage: 7 Carriers, 4 Modes (Air, Sea, Road, Rail), 40+ Global Routes.
Volume: 200,000 records.

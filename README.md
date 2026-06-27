# IT-Ticket-SLA-Breach-Prediction-Risk-Analytics

## Overview
Service Level Agreement (SLA) compliance is a critical performance metric for IT service desks. Delayed ticket resolution can negatively impact business operations, customer satisfaction, and service quality..

This project develops a predictive analytics solution that identifies tickets at risk of breaching SLA targets before resolution. Using historical service desk data, multiple classification models—including Logistic Regression, Random Forest, and XGBoost—are trained to predict breach likelihood and generate risk scores for incoming tickets.

The solution combines machine learning, model explainability, and business intelligence reporting to help service desk teams proactively manage workload, prioritize high-risk incidents, and improve overall SLA performance.

## Dataset

The dataset contains service desk tickets with information including:

- Category
- Priority
- Impact
- Status
- Department
- Assigned Analyst
- SLA Hours
- Ticket Open Times

## Feature Engineering

Features created include:

- Resolution Hours
- Hour Opened
- Day of Week
- Ticket Age
- SLA Utilization Ratio
- Analyst Workload

## Models Evaluated
- Logistic Regression
- Random Forest
- XGBoost

## Evaluation Metrics
- Precision
- Recall
- F1 Score
- ROC_AUC_sc0re
- Confusion matrix

## Explainable AI

SHAP was used to explain model predictions and identify key drivers of SLA breaches.

## Dashboard Features
- High-Risk Ticket Monitoring
- Breach Probability Scoring
- Feature Importance Visualization
- SLA Performance Metrics

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- SHAP
- Streamlit
- Matplotlib
- Seaborn

## Results

The best-performing model achieved strong recall and precision, enabling proactive identification of tickets at risk of SLA breach.







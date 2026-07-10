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
- ROC_AUC_score
- Confusion matrix

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

## Metric-by-metric analysis
### 1. Accuracy
Logistic Regression has the highest accuracy

### 2. Precision
Logistic Regression has the highest precision, meaning it produces fewer false alarms than the other models.

### 3. Recall

Recall measures how many actual SLA breaches the model successfully identifies.
This is particularly important if missing an SLA breach is costly. Logistic Regression detects the largest proportion of breached tickets. (71%)

### 4. F1 Score

The F1 Score balances precision and recall.
Again, Logistic Regression provides the best balance between identifying breaches and avoiding false positives.

### 5. ROC-AUC

ROC-AUC measures the model's ability to distinguish between breached and non-breached tickets across different decision thresholds.
A ROC-AUC of 0.78 indicates that Logistic Regression has the strongest ability among the three models to rank breached tickets ahead of non-breached tickets.

## Explanation

Although three classification models were evaluated, Logistic Regression demonstrated the best overall predictive performance. It achieved the highest Precision (0.68), Recall (0.71), F1 Score (0.69), and ROC-AUC (0.78), indicating the strongest balance between correctly identifying SLA breaches and minimizing false predictions. While Random Forest and XGBoost are more complex ensemble algorithms, neither outperformed Logistic Regression on this dataset. Therefore, Logistic Regression was selected as the final model because it consistently provided the best performance across all key evaluation metrics, rather than being chosen solely based on accuracy.

## Conclusion
To improve the interpretability of the selected Logistic Regression model, the model coefficients were examined. **Positive**  coefficients
 indicate that a feature increases the likelihood of an SLA breach, while **negative** coefficients indicate that it reduces the likelihood.
The magnitude of the coefficient reflects the strength of the feature's influence.

The analysis showed that **Category Breach Rate** was the most influential predictor (coefficient = 0.868), indicating that tickets 
belonging to service categories with historically high breach rates were substantially more likely to breach their SLA. **SLA Hours** 
had the largest negative coefficient (-0.358), suggesting that longer resolution windows reduce the likelihood of an SLA breach. 
Among the categorical variables, **Password Reset** tickets and tickets assigned to the **Risk & Compliance department** were associated 
with an increased probability of breach, whereas **Application Performance Issues**, **Branch Connectivity Issues**, and **Access Requests** 
were associated with a lower probability relative to their respective reference categories. These findings demonstrate that both 
historical performance metrics and ticket characteristics contribute to predicting SLA breaches.




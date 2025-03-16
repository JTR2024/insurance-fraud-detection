# insurance-fraud-detection
Predicting Insurance Fraud with GLMs and GBMs
# Predicting Insurance Fraud with GLMs and GBMs

## Business Motivation
Insurance fraud leads to billions in losses annually, increasing premiums and harming customer trust. Improving fraud detection reduces financial losses, increases efficiency, and enhances customer satisfaction by lowering unnecessary costs. This project explicitly compares traditional Generalized Linear Models (GLM) and modern Gradient Boosting Machines (GBM) to detect fraudulent auto insurance claims.

## Technical Comparison

### GLM (Logistic Regression)
- Accuracy: **55%**
- Precision (fraud): **29%**
- Recall (fraud): **45%**
- ROC-AUC: **57%**

The GLM provided a baseline but showed limited predictive capability, largely due to data imbalance and linear constraints.

## Gradient Boosting Machine (GBM - XGBoost)
We implemented a GBM model, explicitly handling class imbalance via the `scale_pos_weight` parameter. This significantly improved fraud detection:

- **Accuracy:** **80%**
- **Precision (fraud):** 60%
- **Recall (fraud detection rate):** 60%
- **ROC-AUC:** **86%**

## Technical Comparison & Insights
GBMs clearly outperformed GLMs in this scenario due to their ability to model complex, non-linear relationships and better handle imbalanced datasets. Key advantages clearly demonstrated by GBMs include significantly higher ROC-AUC, precision, recall, and accuracy.

## Key Model Insights
Feature importance analysis (next step) can clearly identify the most influential factors driving fraud detection, aiding business stakeholders in targeting resources effectively.

## Next Steps
- Visualizing feature importance clearly.
- Adding model interpretability using SHAP values.
- Potential deployment as an API for real-time prediction (optional).

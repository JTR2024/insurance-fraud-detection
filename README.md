## Getting Started

- **Dataset source**: [Auto Insurance Claims Fraud Detection (Kaggle)](https://www.kaggle.com/code/buntyshah/insurance-fraud-claims-detection)

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

The GBM feature importance clearly highlights specific factors strongly associated with fraudulent claims:

- **Hobbies:** Activities like cross-fit, paintball, or skydiving may correlate with higher-risk behaviors.
- **Incident severity:** Total loss or minor damage incidents appear important in predicting fraud.
- **Vehicle Models:** Certain vehicle models (e.g., Pathfinder, Neon, Civic) may be targeted or associated with higher risk.
- **Occupation:** Individuals with occupations like armed forces may have different risk profiles affecting claims.
- **Total claim amount:** Higher claim amounts could potentially indicate fraudulent behavior.

These insights allow stakeholders to better understand and manage insurance fraud risk clearly and effectively.

![feature_importance](https://github.com/user-attachments/assets/2e3eb76f-3a2a-46d7-9c7e-fe95223853e2)

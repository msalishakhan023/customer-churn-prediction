# customer-churn-prediction
Applied AI Lab 2: Customer Churn Prediction using Logistic Regression and Random Forest
# Customer Churn Prediction (Applied AI - Lab 2)

This project focuses on predicting customer churn using Logistic Regression, Decision Trees, and Random Forest models.

## Week 2: Building ML Models
- Baseline (always "stay"): accuracy 0.735
- Best model: Logistic Regression (balanced), AUC 0.841, recall 0.781 at threshold 0.50 (or ~0.35 default probability threshold)
- Top churn drivers (permutation importance): tenure, TotalCharges, Contract_Two year
- Threshold chosen: 0.35-0.50, because catching churners (high recall) is financially more critical than avoiding minor false alarms
- Engineered features: n_services, is_new, charge_per_mo, price_jump; effect on AUC: 0.8422 -> 0.8420
- Biggest lesson: Tree-based models can inherently capture non-linear feature relationships, rendering basic ratio feature engineering redundant for AUC improvements.

## Key Takeaways & Model Insights
- **Accuracy vs. Recall:** A baseline model predicting no churn achieves ~74% accuracy but is useless in practice. Optimizing recall helps catch true churners before they leave.
- **Model Explainability:** Logistic Regression offers equivalent AUC performance (~0.841) compared to Random Forest while remaining fully interpretable for business stakeholders.

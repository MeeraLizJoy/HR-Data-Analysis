***

```markdown
# HR Attrition Analysis

Predicting and Understanding Employee Attrition with EDA, Machine Learning & Business Insights

---

## Overview

This project analyzes employee attrition using HR data and applies advanced machine learning models to predict risk, uncover drivers, and deliver actionable business recommendations. Attrition—the process by which employees leave a company—can have major impacts on operational cost, morale, and performance. The goal is to empower HR teams with data-driven insights and predictive tools for smarter workforce management.

---

## Objectives & KPIs

- Accurately predict employee attrition using historical features
- Identify top drivers behind employee departures
- Achieve ROC AUC of 0.80+ with test set classification
- Provide actionable HR recommendations for retention

---

## Dataset

- **Source:** IBM HR Analytics Employee Attrition & Performance Dataset (Kaggle)
- **Samples/Features:** ~1500 employees, 40+ features (demographics, compensation, role, satisfaction, performance, etc.)
- **Target Variable:** Attrition (`Yes` or `No`)

---

## Workflow & Structure

### 1. Data Exploration & Preparation
- Data overview, cleaning, and summary stats
- Univariate and bivariate EDA with plots
- Statistical significance testing (t-test, Mann-Whitney, Chi-squared)
- Feature selection based on EDA & significance

### 2. Feature Engineering
- One-hot encoding for categorical variables
- Scaling of numerical features
- Train/test split for model validation

### 3. Model Building & Evaluation
- Logistic Regression: baseline and interpretability
- Random Forest: feature importance, cross-validation, performance
- XGBoost: hyperparameter tuning (grid search), final metrics
- Performance metrics: Accuracy, Precision, Recall, F1, ROC AUC

### 4. Model Interpretation
- Feature importances and coefficients
- ROC curve visualization
- Error analysis (false positives/negatives inspection)

### 5. Insights & Recommendations
- Business interpretation of top predictors
- Targeted retention/intervention strategies for HR
- Limitations and next steps

---

## Results

- **Best XGBoost Parameters:** `learning_rate=0.1, max_depth=5, n_estimators=200, subsample=0.8`
- **Best ROC AUC:** 0.80 (test set)
- **Precision/Recall (Attrition):** Precision 0.63, Recall 0.36
- **Key Drivers Identified:** Education field, Job role, OverTime, Working years, Sales/HR department, Stock options

> Despite strong overall discrimination, recall for leavers remains moderate—reflecting real-world HR complexity and class imbalance.

---

## Recommendations

- Focus retention efforts on high-risk roles, departments, and overtime groups
- Monitor satisfaction, working years, and compensation signals for early intervention
- Use output dashboard for ongoing attrition-risk tracking
- Refine models periodically as more data becomes available

---

## Project Structure

```
notebook.ipynb         # Complete analysis workflow
README.md              # Project summary and instructions
data/                  # Raw and processed datasets
plots/                 # Key figures and visualizations
models/                # Saved trained model objects
```

---

## How to Run

1. Place dataset CSV in `data/` directory
2. Run cells in `notebook.ipynb` step by step (requires Python 3, scikit-learn, pandas, matplotlib, xgboost)
3. Review outputs and plots; tune parameters or expand as needed

---

## References

- [IBM HR Analytics Employee Attrition & Performance Dataset (Kaggle)](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- scikit-learn documentation
- xgboost Python API
- HR Analytics best practices

---

## Author

- Meera Liz Joy

```

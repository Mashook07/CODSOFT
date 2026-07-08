# Credit Card Fraud Detection - Model Results

## Evaluation Metrics

Since the dataset is highly imbalanced, we prioritize **Precision**, **Recall**, and **F1-Score** 
over plain Accuracy.

## Results Summary

| Model | Accuracy | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Random Forest** | 99.95% | 96.2% | 82.1% | 88.6% | 0.981 |
| **XGBoost** | 99.94% | 94.8% | 80.6% | 87.1% | 0.978 |
| **LightGBM** | 99.93% | 93.5% | 79.4% | 85.9% | 0.975 |
| **Logistic Regression** | 97.80% | 6.2% | 91.8% | 11.6% | 0.948 |

## Key Observations

- **Random Forest** achieves the best overall F1-Score and ROC-AUC for the fraud class.
- **Logistic Regression** has very high Recall but extremely low Precision — too many false alarms.
- **SMOTE** (Synthetic Minority Over-sampling) was applied on the training set only to avoid data leakage.
- Threshold tuning was applied to optimize the Precision-Recall trade-off.

## Best Model: Random Forest Classifier

- **Confusion Matrix highlights**: Very few false negatives (missed frauds)
- **Feature Importance**: `V14`, `V17`, `V12`, `V10`, and `Amount` are top predictors

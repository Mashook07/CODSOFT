# Credit Card Fraud Detection - Dataset Info

## Source
The dataset used for this task is the **Credit Card Fraud Detection** dataset, 
widely available on Kaggle.

## Description
- **Total Transactions**: 284,807
- **Fraudulent Transactions**: 492 (0.172% of total)
- **Genuine Transactions**: 284,315 (99.828% of total)

## Features
- **Time**: Number of seconds elapsed between this transaction and the first transaction
- **V1 - V28**: Result of PCA transformation (anonymized due to confidentiality)
- **Amount**: Transaction amount
- **Class**: Response variable (1 = Fraud, 0 = Genuine)

## Class Imbalance
The dataset is **highly imbalanced**. We use SMOTE (Synthetic Minority Over-sampling Technique)
to balance the classes before training the models.

## Key Challenge
- Maximize **Recall** for the fraud class (minimize false negatives)
- Maintain acceptable **Precision** to avoid too many false alarms

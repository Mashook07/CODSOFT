# Titanic Survival Prediction (Codsoft Internship - Task 1)

This repository contains the implementation for **Task 1: Titanic Survival Prediction** as part of the Codsoft Internship. The project aims to build a machine learning model that predicts whether a passenger survived the Titanic disaster based on features like gender, age, socio-economic class (Pclass), and family relationships.

## Project Structure

```
├── .gitignore                          # Standard git ignore rules (checkpoints, pycache, etc.)
├── Titanic Survival Prediction.ipynb   # Main Jupyter Notebook containing analysis, bug fixes, and models
├── test.csv                            # Titanic passenger dataset
└── confusion_matrices.png              # Generated evaluation plots for model comparison
```


## Model Comparison

We trained and compared two different models on the cleaned dataset:
1. **Logistic Regression** (baseline)
2. **Random Forest Classifier**

### Classification Reports & Metrics

Both models achieved perfect precision, recall, and accuracy on the training and test sets due to the deterministic nature of the target variable in the dataset:

* **Training Accuracy:** 100% (1.0)
* **Testing Accuracy:** 100% (1.0)

## Getting Started

To run the notebook locally, ensure you have Python installed with the necessary dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Open the Jupyter Notebook:

```bash
jupyter notebook "Titanic Survival Prediction.ipynb"
```

# CODSOFT Internship Tasks

This repository contains the implementations for the tasks assigned during the CODSOFT Internship.

## Project Structure

```
├── .gitignore                                     # Standard git ignore rules (checkpoints, pycache, etc.)
├── README.md                                      # Project documentation
│
└── Task 1 - Titanic Survival Prediction/          # Task 1: Titanic Survival Prediction
    ├── Titanic Survival Prediction.ipynb          # Jupyter Notebook containing analysis and models
    └── test.csv                                   # Titanic passenger dataset
```

## Task 1: Titanic Survival Prediction

The project aims to build a machine learning model that predicts whether a passenger survived the Titanic disaster based on features like gender, age, socio-economic class (Pclass), and family relationships.

### Model Comparison

We trained and compared two different models on the cleaned dataset:
1. **Logistic Regression** (baseline)
2. **Random Forest Classifier**

### Classification Reports & Metrics

Both models achieved perfect precision, recall, and accuracy on the training and test sets due to the deterministic nature of the target variable in the dataset:

* **Training Accuracy:** 100% (1.0)
* **Testing Accuracy:** 100% (1.0)

### Getting Started

To run the notebook locally, ensure you have Python installed with the necessary dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Open the Jupyter Notebook:

```bash
cd "Task 1 - Titanic Survival Prediction"
jupyter notebook "Titanic Survival Prediction.ipynb"
```

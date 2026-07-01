# Titanic Survival Prediction (Codsoft Internship - Task 1)

This repository contains the implementation for **Task 1: Titanic Survival Prediction** as part of the Codsoft Internship. The project aims to build a machine learning model that predicts whether a passenger survived the Titanic disaster based on features like gender, age, socio-economic class (Pclass), and family relationships.

## Project Structure

```
├── .gitignore                          # Standard git ignore rules (checkpoints, pycache, etc.)
├── Titanic Survival Prediction.ipynb   # Main Jupyter Notebook containing analysis, bug fixes, and models
├── test.csv                            # Titanic passenger dataset
└── confusion_matrices.png              # Generated evaluation plots for model comparison
```

## Key Findings & Data Insight

During the exploratory data analysis, we uncovered a critical detail about this specific dataset (`test.csv`):
* **Deterministic Survival Pattern:** The target label `Survived` is a simple deterministic function of the passenger's gender (`Sex`).
  * **All females survived** (152/152)
  * **All males did not survive** (266/266)
* Consequently, any standard classifier can easily achieve **100% accuracy** on this dataset by learning this simple gender rule. However, our model evaluation confirmed this relationship holds true for both Logistic Regression and Random Forest models when evaluated properly.

## Important Bug Fixes & Refactoring

The initial code contained a few issues that were resolved in this project:
1. **Data Leakage Fix:** The feature matrix `X` originally included the target label `Survived`. This was a major data leakage bug where the model had direct access to the correct answers during training. We fixed this by explicitly dropping the `Survived` column from `X`.
2. **Pandas Deprecation Warnings:** Replaced deprecated `inplace=True` operations on `.fillna()` and `.replace()` calls with clean, direct variable assignments (e.g. using `.map()` on categorical fields like `Sex` and `Embarked`).
3. **Logistic Regression Convergence Warning:** Increased `max_iter` parameter in `LogisticRegression` to `1000` to allow the optimization algorithm to converge correctly.

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

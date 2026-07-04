# CODSOFT Internship Tasks

This repository contains the implementations for the tasks assigned during the CODSOFT Internship.

## Project Structure

```
├── .gitignore                                     # Standard git ignore rules (checkpoints, pycache, etc.)
├── README.md                                      # Project documentation
│
├── Task 1 - Titanic Survival Prediction/          # Task 1: Titanic Survival Prediction
│   ├── Titanic Survival Prediction.ipynb          # Jupyter Notebook containing analysis and models
│   └── test.csv                                   # Titanic passenger dataset
│
└── Task 2 - Movie Rating Prediction/              # Task 2: Movie Rating Prediction
    ├── Movie Rating Prediction.ipynb              # Jupyter Notebook containing EDA and regressor models
    ├── prediction.csv                             # IMDb India movies dataset
    ├── catboost_training.json                     # CatBoost training metadata
    ├── learn_error.tsv                            # CatBoost learn error logs
    └── time_left.tsv                              # CatBoost time estimation logs
```

---

## Task 1: Titanic Survival Prediction

The project aims to build a machine learning model that predicts whether a passenger survived the Titanic disaster based on features like gender, age, socio-economic class (Pclass), and family relationships.

### Model Comparison & Results

We trained and compared two different models:
1. **Logistic Regression** (baseline)
2. **Random Forest Classifier**

* **Training Accuracy:** 100%
* **Testing Accuracy:** 100%

### Getting Started

```bash
cd "Task 1 - Titanic Survival Prediction"
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook "Titanic Survival Prediction.ipynb"
```

---

## Task 2: Movie Rating Prediction

The objective of this task is to build a machine learning model that estimates the rating of a movie based on historical data. Using regression techniques, the project analyzes factors like genre, director, and cast to predict IMDb movie ratings.

### Dataset Features

The dataset (`prediction.csv`) contains movies with features:
* **Name**: Title of the movie
* **Year**: Release year
* **Duration**: Running time of the movie
* **Genre**: Category/Genre classification
* **Director**: Director of the movie
* **Actor 1, Actor 2, Actor 3**: Main cast members
* **Votes**: Number of votes received on IMDb
* **Rating**: The target variable (IMDb Rating)

### Models Evaluated & Metrics

We compared several regression algorithms using $R^2$ Score (Coefficient of Determination) and Root Mean Squared Error (RMSE):

| Regression Model | $R^2$ Score | RMSE (Lower is Better) |
| :--- | :--- | :--- |
| **Light Gradient Boosting (LGBM)** | **38.16%** | **1.06** |
| **Gradient Boosting Regressor** | **38.04%** | **1.06** |
| **CatBoost Regressor** | **35.86%** | **1.08** |
| **Random Forest Regressor** | **35.41%** | **1.09** |
| **XGBoost Regressor** | **34.81%** | **1.09** |
| **K-Nearest Neighbors** | **3.03%** | **1.33** |
| **Linear Regression** | -6.45% (Underfitting) | 1.39 |
| **Decision Tree Regressor** | -27.77% (Overfitting) | 1.53 |

### Getting Started

Install the required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly wordcloud xgboost lightgbm catboost
```

Navigate to the task folder and open the notebook:

```bash
cd "Task 2 - Movie Rating Prediction"
jupyter notebook "Movie Rating Prediction.ipynb"
```

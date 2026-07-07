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
├── Task 2 - Movie Rating Prediction/              # Task 2: Movie Rating Prediction
│   ├── Movie Rating Prediction.ipynb              # Jupyter Notebook containing EDA and regressor models
│   ├── prediction.csv                             # IMDb India movies dataset
│   ├── catboost_training.json                     # CatBoost training metadata
│   ├── learn_error.tsv                            # CatBoost learn error logs
│   └── time_left.tsv                              # CatBoost time estimation logs
│
├── Task 3/                                        # Task 3: Iris Flower Classification
│   ├── Task 3.ipynb                               # Jupyter Notebook containing EDA and classifier models
│   └── Task 3.csv                                 # Iris flower dataset
│
└── Task 4 - Sales Prediction/                     # Task 4: Sales Prediction
    ├── Sales Prediction .ipynb                    # Jupyter Notebook containing EDA and regression models
    ├── car_purchasing.csv                         # Car purchasing dataset with customer demographics
    └── sales data file.csv                        # Sales transactions dataset
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

---

## Task 3: Iris Flower Classification

The objective of this task is to build a machine learning model that classifies iris flowers into one of three species — *Iris-setosa*, *Iris-versicolor*, and *Iris-virginica* — based on their sepal and petal measurements.

### Dataset Features

The dataset (`Task 3.csv`) contains 150 iris flower samples with the following features:
* **sepal_length**: Length of the sepal (cm)
* **sepal_width**: Width of the sepal (cm)
* **petal_length**: Length of the petal (cm)
* **petal_width**: Width of the petal (cm)
* **species**: Target variable — Iris-setosa, Iris-versicolor, or Iris-virginica

### Models Evaluated & Results

We trained and compared three classification algorithms:

| Classifier | Description |
| :--- | :--- |
| **Logistic Regression** | Linear baseline classifier |
| **K-Nearest Neighbors (KNN)** | Distance-based classifier |
| **Decision Tree Classifier** | Tree-based non-linear classifier |

### Getting Started

Install the required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Navigate to the task folder and open the notebook:

```bash
cd "Task 3"
jupyter notebook "Task 3.ipynb"
```

---

## Task 4: Sales Prediction

The objective of this task is to build a machine learning model that predicts the amount of sales based on advertising expenditure across multiple channels (TV, Radio, Newspaper) and customer demographics (age, salary, etc.). Using regression techniques, the project analyzes the impact of various marketing inputs on product sales.

### Dataset Features

**Sales Data File (`sales data file.csv`)** — Advertising spend vs. sales:
* **TV**: Advertising spend on TV (in $1000s)
* **Radio**: Advertising spend on Radio (in $1000s)
* **Newspaper**: Advertising spend on Newspaper (in $1000s)
* **Sales**: Target variable — product sales (in 1000 units)

**Car Purchasing Dataset (`car_purchasing.csv`)** — Customer demographics vs. purchase amount:
* **Customer Name**: Name of the customer
* **Customer e-mail**: Customer email address
* **Country**: Country of residence
* **Gender**: Gender of the customer
* **Age**: Age of the customer
* **Annual Salary**: Annual salary of the customer
* **Credit Card Debt**: Credit card debt of the customer
* **Net Worth**: Net worth of the customer
* **Car Purchase Amount**: Target variable — amount spent on car purchase

### Models Evaluated & Results

We trained and compared multiple regression algorithms:

| Regression Model | Description |
| :--- | :--- |
| **Linear Regression** | Baseline linear model |
| **Random Forest Regressor** | Ensemble tree-based model |
| **Gradient Boosting Regressor** | Sequential boosting model |
| **Support Vector Regressor (SVR)** | Kernel-based regression |

### Getting Started

Install the required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Navigate to the task folder and open the notebook:

```bash
cd "Task 4 - Sales Prediction"
jupyter notebook "Sales Prediction .ipynb"
```

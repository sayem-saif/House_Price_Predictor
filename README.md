# House Price Prediction using Machine Learning

## Overview

This project develops a machine learning pipeline to predict residential property prices using the Ames Housing dataset from the Kaggle House Prices: Advanced Regression Techniques competition.

The objective is to estimate the sale price of a house based on its structural, geographical, and quality-related attributes. The project covers the complete machine learning workflow, including exploratory data analysis, data preprocessing, feature engineering, model training, evaluation, and competition submission.

---

## Problem Statement

Predict the final sale price of residential properties using historical housing data containing numerical and categorical features.

Target Variable:

```text
SalePrice
```

---

## Dataset

Source:

House Prices: Advanced Regression Techniques (Kaggle)

Dataset Characteristics:

* 1460 training samples
* 1459 testing samples
* 80 input features
* 1 target variable (SalePrice)

The dataset contains:

* Property size information
* Building quality metrics
* Garage information
* Basement information
* Construction details
* Neighborhood information
* Sale-related attributes

---

## Project Workflow

### 1. Data Exploration

Performed exploratory data analysis to understand:

* Feature distributions
* Missing values
* Feature correlations
* Important predictors of house prices

### 2. Data Preprocessing

Implemented preprocessing using Scikit-Learn Pipelines and Column Transformers.

#### Numerical Features

* Missing value handling using Median Imputation

#### Categorical Features

* Missing value handling using Constant Imputation
* One-Hot Encoding

### 3. Feature Engineering

Created additional informative features including:

* HouseAge
* TotalBathrooms
* TotalSF

These features provide a more meaningful representation of the property characteristics.

### 4. Model Development

Models evaluated:

#### Random Forest Regressor

Used as the initial baseline model.

#### XGBoost Regressor

Used as the final model due to superior predictive performance.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Joblib
* Google Colab

---

## Model Pipeline

```text
Raw Data
   │
   ▼
Missing Value Handling
   │
   ▼
Categorical Encoding
   │
   ▼
Feature Engineering
   │
   ▼
XGBoost Regressor
   │
   ▼
Price Prediction
```

---

## Evaluation Results

### Random Forest

| Metric   | Value  |
| -------- | ------ |
| MAE      | 19,432 |
| R² Score | 0.8816 |

### XGBoost Pipeline

| Metric   | Value  |
| -------- | ------ |
| MAE      | 15,790 |
| R² Score | 0.9173 |

### Kaggle Submission Score

| Metric | Value   |
| ------ | ------- |
| RMSLE  | 0.13799 |

---

## Key Features Identified

The most influential features contributing to price prediction were:

* OverallQual
* GrLivArea
* TotalBsmtSF
* YearBuilt
* GarageArea
* GarageCars
* FullBath

Feature importance analysis showed that overall house quality had the strongest impact on property valuation.

---

## Repository Structure

```text
House-Price-Prediction/
│
├── house_price_model.ipynb
├── house_price_model.pkl
├── submission.csv
├── requirements.txt
├── README.md
│
├── images/
│   ├── correlation_heatmap.png
│   └── feature_importance.png
│
└── data/
```

---

## Running the Project

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

Open:

```text
house_price_model.ipynb
```

and execute all cells.

---

## Future Improvements

* Advanced feature engineering
* Hyperparameter optimization
* CatBoost implementation
* LightGBM implementation
* Ensemble learning
* Automated cross-validation pipeline

---

## Author

MD Sayem Saif

Machine Learning | Embedded Systems | IoT | AI Applications

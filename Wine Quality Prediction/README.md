# 🍷 Wine Quality Prediction

## 📌 Project Description

This project explores a classic regression problem using the UCI Wine Quality Dataset. The goal is to predict wine quality based on physicochemical features and understand which features contribute most to wine scoring. The workflow includes exploratory data analysis, outlier handling, feature scaling, and model comparison (Linear Regression, Random Forest, and XGBoost).

---

## 📊 Dataset Overview

* **Source**: UCI Machine Learning Repository
* **Samples**: 1,599 red wine samples
* **Target**: `quality` (integer score between 3 and 8)
* **Features**:

  * fixed acidity
  * volatile acidity
  * citric acid
  * residual sugar
  * chlorides
  * free sulfur dioxide
  * total sulfur dioxide
  * density
  * pH
  * sulphates
  * alcohol

---

## 🔍 Key Steps

### 1. Exploratory Data Analysis

* Distribution of quality scores visualized using countplots.
* Boxplots used to detect outliers, especially for sulfur dioxide variables.
* Correlation heatmap created using a lower-triangle mask to reveal inter-feature relationships.

### 2. Outlier Removal

* IQR method applied to remove outliers from `free sulfur dioxide` and `total sulfur dioxide`.

### 3. Feature Selection

* Initially tested prediction using a subset of features: `citric acid`, `density`, and `fixed acidity`.
* Later added `free sulfur dioxide` and `total sulfur dioxide` for improved accuracy.

### 4. Modeling & Evaluation

* Applied log transformation to `quality` for better distribution.
* Evaluated models using 5-fold cross-validation with Mean Squared Error (MSE) and R².
* Models tested:

  * Linear Regression
  * Random Forest Regressor
  * XGBoost Regressor

### 5. Feature Importance

* Extracted from Random Forest and visualized using a horizontal bar chart.

---

## 🏆 Results

| Model             | MSE   | R²    |
| ----------------- | ----- | ----- |
| Linear Regression | 0.577 | 0.121 |
| Random Forest     | 0.450 | 0.320 |
| XGBoost           | 0.498 | 0.247 |

Random Forest performed the best overall with the highest R² and lowest MSE.

---

## 📈 Visualization Highlights

* Lower-triangle heatmap to avoid redundant correlation.
* Bar plot comparison of model performance.
* Feature importance plot for interpretability.

---

## 📦 Tools Used

* Python (pandas, numpy, matplotlib, seaborn)
* scikit-learn
* xgboost
* Jupyter Notebook

---

## 🤔 Reflections

This project reinforced the importance of:

* Preprocessing steps like outlier removal and log transformation
* Trying multiple models to find the best fit
* Visual storytelling to enhance interpretation

---

## 📁 Folder Structure

```
/Wine Quality Prediction
|-- EDA.ipynb
|-- modeling.ipynb
|-- heatmap.png
|-- feature_importance.png
|-- README.md
```

---

## 🔗 Reference

* [UCI Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality)




# 📊 Project Success Prediction with Machine Learning Models

A Machine Learning project that predicts whether a project is likely to be successful based on key project characteristics such as **team experience, project budget, development methodology, and risk score**.

The project compares multiple Machine Learning algorithms and configurations to evaluate their ability to classify projects as successful or unsuccessful.

---

## 🎯 Project Overview

Project success can be influenced by several factors, including the experience of the project team, available budget, development methodology, and the level of project risk.

This project applies Machine Learning classification techniques to identify patterns between these factors and the final project outcome.

The main objective is to:

- Analyze project-related characteristics
- Preprocess and transform the dataset
- Train multiple Machine Learning classification models
- Compare model performance
- Evaluate models using accuracy
- Identify the models that perform best on the test dataset

---

## 📌 Prediction Target

The target variable is:

`Project_Success`

| Value | Meaning |
|---|---|
| `1` | Project Successful |
| `0` | Project Unsuccessful |

The model learns from historical project data and predicts the success classification based on the available project characteristics.

---

## 📊 Dataset

The dataset contains the following features:

| Feature | Description |
|---|---|
| `Team_Experience_Years` | Experience of the project team in years |
| `Budget_USD_Thousands` | Project budget in thousands of USD |
| `Methodology` | Project development methodology |
| `Risk_Score` | Risk level associated with the project |
| `Project_Success` | Target variable indicating project success |

### Methodology

The `Methodology` feature contains categorical values such as:

- Agile
- Waterfall

Categorical data is converted into numerical form using **one-hot encoding** before model training.

---

## 🤖 Machine Learning Models

The project evaluates **15 different model configurations** across five Machine Learning algorithms.

### K-Nearest Neighbors (KNN)

- KNN with `k = 1`
- KNN with `k = 3`
- KNN with `k = 7`

### Decision Tree

- Decision Tree with maximum depth `2`
- Decision Tree with maximum depth `4`
- Decision Tree with unlimited depth

### Logistic Regression

- Logistic Regression with `C = 0.1`
- Logistic Regression with `C = 1.0`

### Support Vector Machine (SVM)

- Linear SVM with `C = 1.0`
- RBF SVM with `C = 1.0`
- RBF SVM with `C = 10.0`

### Random Forest

- 10 trees with maximum depth `3`
- 50 trees with maximum depth `3`
- 50 trees with unlimited depth
- 100 trees with unlimited depth

These configurations allow different algorithms and hyperparameter settings to be compared using the same dataset and evaluation process. :contentReference[oaicite:1]{index=1}

---

## 🔄 Machine Learning Workflow

The project follows this workflow:

```text
Project Dataset
      │
      ▼
Data Loading
      │
      ▼
Feature Selection
      │
      ▼
Categorical Encoding
      │
      ▼
Train / Test Split
      │
      ▼
Feature Scaling
      │
      ▼
Train Multiple ML Models
      │
      ▼
Generate Predictions
      │
      ▼
Calculate Accuracy
      │
      ▼
Compare Model Performance
      │
      ▼
Export Results

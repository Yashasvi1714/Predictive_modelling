# 🧠 Income Classification with Census Data

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Modeling-orange?logo=scikit-learn)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

This project implements predictive models to classify adult income based on the U.S. Census Bureau data. The goal is to predict whether a person earns more than $50K per year using machine learning techniques.

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `FinalProject.ipynb` | Jupyter Notebook with complete code and outputs |
| `README.md` | Project overview and usage instructions |
| `adult-dataset.csv` | *(Not included)* Original data file from UCI repository |


---

## 📊 Dataset Overview

The dataset contains demographic and employment-related attributes for U.S. adults. The target variable is `Income`:

- `<=50K` or `>50K`

### Features include:
- Age (int)
- Work Class (categorical)
- Education (categorical)
- Marital Status (categorical)
- Occupation (categorical)
- Race (categorical)
- Sex (binary)
- Hours per week (int)

---

## 🧹 Part A: Data Cleaning

- Handled missing data by removing or imputing invalid entries
- Converted categorical variables using **one-hot encoding**
- Removed irrelevant columns
- Ensured numeric data for model compatibility

---

## 📉 Part B: Dimensionality Reduction

Applied both **SVD** and **PCA** to reduce dataset dimensions.

### ✅ Results:
- **Explained Variance**: PCA components capturing >90% of varianc

## 🤖 Part C: Model Training & Evaluation

### 1. Multi-Layer Perceptron (Neural Network)
- Built with `MLPClassifier`
- Evaluated using Confusion Matrix & Classification Report

### 2. Logistic Regression
- Applied using Scikit-learn
- Good baseline model

### 3. Naïve Bayes (GaussianNB)
- Fast and interpretable model

### 4. K-Means Clustering
- Unsupervised clustering excluding `Income`

---

## 🧪 Results Summary

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| MLP | ✅ High | ✅ High | ✅ High | ✅ High |
| Logistic Regression | Moderate | Moderate | Moderate | Moderate |
| Naïve Bayes | Moderate | Lower | Moderate | Moderate |
| K-Means | - | - | - | - (unsupervised) |

---

## 🚀 Getting Started

### 🔧 Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn

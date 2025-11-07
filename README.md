# Titanic-Survival-Prediction

This project builds a **Logistic Regression** model to predict passenger survival on the **RMS Titanic**.  
The analysis is based on the Kaggle dataset: [_Titanic: Machine Learning from Disaster_](https://www.kaggle.com/c/titanic).

---

## 📋 Table of Contents
- [Introduction](#-introduction)
- [Methodology](#-methodology)
- [Results](#-results)
- [Potential Improvements](#-potential-improvements)
- [How to Run](#️-how-to-run)
- [Dependencies](#-dependencies)
- [Code](#-code)

---

## 📖 Introduction

The goal of this project is to apply **machine learning** techniques to a real-world dataset.  
We use passenger data — such as **age**, **gender**, and **class (Pclass)** — to predict whether a passenger survived the Titanic disaster.

---

## 🛠️ Methodology

### 1. Data Exploration & Visualization
- Loaded dataset and explored key features (`Pclass`, `Sex`, `Age`, `Fare`, etc.).
- Identified missing values in **Age**, **Cabin**, and **Embarked**.
- Visualized relationships showing that **gender** and **class** are strong predictors of survival.

### 2. Data Preprocessing
- **Missing Values:** Filled missing `Age` with the median age for that `Pclass`.
- **Dropped Columns:** Removed `Cabin`, `Ticket`, and `Name` (low predictive value).
- **Encoding:** Converted categorical columns (`Sex`, `Embarked`) using one-hot encoding.

### 3. Model Training
- Split data into **80% training** and **20% testing** sets.
- Trained a **Logistic Regression** model from `scikit-learn`.

---

## 📊 Results

The model was evaluated on the unseen test set with the following performance:

### **Overall Accuracy:** 82%

| Class | Precision | Recall | F1-Score | Support |
|:------|:-----------|:--------|:----------|:----------|
| 0 (Did not survive) | 0.83 | 0.87 | 0.85 | 105 |
| 1 (Survived) | 0.80 | 0.74 | 0.77 | 74 |


✅ The model correctly identified **91 non-survivors** and **55 survivors**.

---

## 🚀 Potential Improvements
- **Feature Engineering:** Add features like `FamilySize = SibSp + Parch` or `IsAlone`.
- **Advanced Imputation:** Use `KNNImputer` or regression-based filling for `Age`.
- **Model Exploration:** Try **Random Forest**, **Gradient Boosting**, or **SVM** to improve accuracy.

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/tanishkagupta2207/APR_Assignment1.git
   cd APR_Assignment1
2. Run the Python file or open the notebook:

`python titanic_survival.py`

# Credit Card Fraud Detection Using Machine Learning

## 📌 Project Overview

This project focuses on detecting fraudulent credit card transactions using Machine Learning classification algorithms.

The primary objective is to identify fraudulent transactions from legitimate ones while addressing the highly imbalanced nature of the dataset.

Multiple classification algorithms were evaluated, along with different class-imbalance handling techniques, to compare their performance using Precision, Recall, F1-Score, and ROC-AUC.

---

## 📊 Dataset

The dataset contains credit card transactions made by European cardholders.

### Features:

- **Time:** Time elapsed between transactions
- **V1–V28:** PCA-transformed numerical features
- **Amount:** Transaction amount
- **Class:** Target variable
  - `0` – Legitimate transaction
  - `1` – Fraudulent transaction

The dataset is highly imbalanced, with fraudulent transactions representing a very small proportion of all transactions.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn
- Jupyter Notebook

---

## 🔍 Project Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Data Cleaning and Missing Value Analysis
4. Feature Engineering
5. Feature Scaling
6. Train-Test Split
7. Baseline Model Development
8. Model Comparison
9. Class Imbalance Handling
10. Model Evaluation
11. Hyperparameter Tuning
12. Final Model Selection

---

## 🤖 Machine Learning Models

The following classification algorithms were implemented and evaluated:

- Logistic Regression (L1 Regularization)
- Logistic Regression (L2 Regularization)
- K-Nearest Neighbors (KNN)
- Decision Tree (Gini)
- Decision Tree (Entropy)
- Random Forest
- Support Vector Machine (SVM)
- XGBoost

---

## ⚖️ Handling Class Imbalance

Due to the highly imbalanced distribution of fraudulent and legitimate transactions, multiple resampling techniques were explored:

- Random Oversampling
- SMOTE (Synthetic Minority Over-sampling Technique)
- ADASYN (Adaptive Synthetic Sampling)

These techniques were used to investigate their impact on minority-class detection performance.

---

## 🔧 Hyperparameter Tuning

Hyperparameter tuning was performed on XGBoost to optimize model performance by experimenting with different model configurations.

The objective was to improve fraud detection performance while balancing Precision and Recall.

---

## 📈 Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

Particular emphasis was placed on Recall and F1-Score because missing fraudulent transactions can result in financial losses, while excessive false positives can inconvenience legitimate customers.

---

## 🏆 Results

The XGBoost model demonstrated strong fraud detection performance.

The best reported XGBoost + SMOTE experiment achieved:

- **ROC-AUC:** 98.21%
- **Precision:** 92.86%
- **Recall:** 78.79%
- **F1-Score:** 85.25%

Hyperparameter-tuned XGBoost was also evaluated on the original imbalanced dataset.

---

## 📁 Project Structure

```text
Credit-Card-Fraud-Detection/
│
├── Credit_Card_Fraud_Detection.ipynb
├── creditcard.csv
├── README.md
└── requirements.txt
```

---

## 🔮 Future Improvements

- Implement a robust cross-validation pipeline
- Apply resampling techniques exclusively to training folds
- Perform systematic hyperparameter optimization
- Compare additional models such as LightGBM and CatBoost
- Evaluate models using PR-AUC
- Optimize classification thresholds based on business costs
- Improve probability calibration
- Deploy the model using Streamlit or Flask

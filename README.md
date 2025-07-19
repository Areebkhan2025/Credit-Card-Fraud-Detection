# 💳 Credit Card Fraud Detection

This project is focused on detecting fraudulent credit card transactions using machine learning techniques. The dataset used is highly imbalanced, with the majority of transactions being non-fraudulent. To effectively tackle this challenge, various machine learning models and resampling techniques were explored to improve performance, especially on the minority class.

---

## 📁 Project Overview

- **Problem**: Classify transactions as fraudulent or non-fraudulent.
- **Dataset**: Public credit card transactions dataset (highly imbalanced).
- **Objective**: Build a high-performing model that can detect fraud with high precision and recall on the minority class.

---

## ⚙️ Methodology

### 🔄 Resampling Techniques Explored
- **Random Oversampling**
- **SMOTE (Synthetic Minority Over-sampling Technique)**
- **ADASYN (Adaptive Synthetic Sampling)**

### 🔬 Cross-Validation Strategies
- **StratifiedKFold**
- **RepeatedStratifiedKFold**
- **Train-Test Split (as baseline)**

### 🤖 Machine Learning Models Tried
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. K-Nearest Neighbors (KNN)
5. XGBoost
6. Support Vector Machine (SVM)

---

## 📌 Final Model Selection Conclusion

After evaluating multiple combinations of models, oversampling techniques, and cross-validation strategies, the following insights were obtained:

### 🔹 **Best Performing Oversampled Model**
- **Model**: XGBoost
- **Validation Strategy**: Random Oversampling with RepeatedStratifiedKFold
- **Before Hyperparameter Tuning**:
  - ROC AUC: **0.9799**
  - Accuracy: **0.9991**
  - Optimal Threshold: **0.0176**
- **After Hyperparameter Tuning**:
  - ✅ Accuracy: **0.9998**
  - ✅ ROC AUC: **0.9944**
  - ✅ Optimal Threshold: **0.0172**

### 🔹 **Best Performing Model Without Resampling**
- **Model**: Logistic Regression with L1 Regularization
- **Validation Strategy**: StratifiedKFold (No Oversampling)
- **Performance**:
  - ROC AUC: **0.8837**
  - Accuracy: **0.9990**

✅ While XGBoost with oversampling performed best overall, Logistic Regression offered high interpretability and good performance without additional sampling techniques.

---

## 📊 Feature Importance (XGBoost)

A feature importance plot was generated using the trained XGBoost model, showing the top contributing features for fraud detection.

---

## 🧪 Evaluation Metrics Used

- Accuracy
- ROC AUC Score
- F1 Score
- Precision & Recall
- Confusion Matrix
- Optimal Classification Threshold

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn
- XGBoost
- Matplotlib, Seaborn

---

## 🧠 Key Learnings

- Handling imbalanced data is crucial for fraud detection.
- RepeatedStratifiedKFold provides more robust validation for imbalanced datasets.
- XGBoost is a powerful model for fraud detection when tuned and combined with oversampling.
- Simpler models like Logistic Regression can also perform well without resampling.

---

## 📁 Folder Structure (Optional)


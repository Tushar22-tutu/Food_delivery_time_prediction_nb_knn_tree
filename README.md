# 🚚 Food Delivery Time Prediction

## 🎯 Objective
The objective is to predict whether a food delivery will be **"Fast"** or **"Delayed"** using machine learning models. This is a **binary classification problem** based on features like:
- Customer location
- Restaurant location
- Weather conditions
- Traffic status
- Distance
- Vehicle type

---

## 📊 Phase 1: Data Preprocessing

### 🔹 Data Import and Cleaning
- Load dataset: `Food_Delivery_Time_Prediction.csv`
- Handle missing values using **mean/median imputation**
- Encode categorical features (weather, traffic, vehicle type) using **LabelEncoder**
- Normalize continuous features like `Distance` and `Delivery Time` using `StandardScaler`

### 🔹 Feature Engineering
- Compute **geographical distance** using latitude and longitude (Haversine formula)
- Convert delivery time into binary class:
  - **1 = Delayed**, **0 = Fast** (threshold based on average or median delivery time)

---

## 🧠 Phase 2: Classification Models

### ✅ 1. Naive Bayes Classifier
- **Model Used**: Gaussian Naive Bayes (suitable for continuous features)
- **Target**: `Delivery_Status` (Fast = 0, Delayed = 1)
- **Evaluation Metrics**:
  - Accuracy
  - Confusion Matrix
  - Precision
  - Recall
  - F1-Score

### ✅ 2. K-Nearest Neighbors (KNN)
- **Model**: KNN Classifier with `n_neighbors = K`
- **Tuning**:
  - Use GridSearchCV or cross-validation to find optimal `K`
- **Evaluation Metrics**:
  - Accuracy
  - Confusion Matrix
  - Precision
  - Recall
  - F1-Score

### ✅ 3. Decision Tree Classifier
- **Model**: Decision Tree Classifier (`sklearn.tree.DecisionTreeClassifier`)
- **Tuning**:
  - `max_depth` to limit tree depth
  - `min_samples_split` to control split threshold
- **Evaluation Metrics**:
  - Accuracy
  - Confusion Matrix
  - Precision
  - Recall
  - F1-Score

---

## 📌 Summary
This project builds a robust **binary classification pipeline** using data preprocessing, feature engineering, and three classification algorithms — Naive Bayes, KNN, and Decision Tree. It aims to support **delivery optimization** and **customer satisfaction** through data-driven decision making.

📦 **Future Enhancements**: Model deployment via Flask API, dashboard visualization, or integration with food delivery platforms.

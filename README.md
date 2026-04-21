# Loan-default-prediction-ml
Built an end-to-end loan default prediction model using Random Forest, SMOTE, and threshold tuning to identify high-risk customers and reduce financial risk.

## 📌 Problem Statement

The goal of this project is to predict whether a customer will default on a loan using machine learning techniques.
👉 This project aims to:

- Identify high-risk customers
- Improve loan approval decisions
- Reduce default rates


## 📊 Dataset

* Contains customer financial and demographic details
* Target variable: `Default` (0 = No, 1 = Yes)

## Project Workflow

### 1. Data Preprocessing

* Handled missing values
* Encoded categorical variables
* Feature scaling using StandardScaler

### 2. Exploratory Data Analysis (EDA)
* Distribution analysis
* Correlation heatmap
* Class imbalance identification

### 3. Handling Imbalanced Data

* Used `class_weight='balanced'`
* Applied SMOTE for better minority class learning

### 4. Model Building

* Logistic Regression (baseline)
* Random Forest (improved model)

### 5. Evaluation Metrics

* Precision
* Recall
* F1-score
* Confusion Matrix

### 6. Threshold Tuning

* Adjusted probability threshold to balance precision and recall


## 📈 Results

| Metric              | Value      |
| ------------------- | ---------- |
| Accuracy            | ~0.78      |
| Recall (Default)    | ~0.60      |
| Precision (Default) | ~0.25–0.30 |


## 💡 Key Insights

* Model successfully identifies majority of defaulters
* Trade-off observed between precision and recall
* Random Forest performed better than Logistic Regression


## 🚀 Business Impact

This model can help financial institutions:

* Identify high-risk customers
* Reduce loan defaults
* Improve credit decision-making


## 🔮 Future Improvements

* Use XGBoost for better performance
* Feature engineering
* Hyperparameter tuning using GridSearchCV


## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

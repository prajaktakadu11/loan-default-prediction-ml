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

| Metric              | Value    |
| ------------------- | -------- |
| Accuracy            | ~0.68    |
| Recall (Default)    | **0.70** |
| Precision (Default) | ~0.22    |


## 💡 Key Insights

* Dataset is imbalanced (~11.5% defaulters)

### Logistic Regression (Final Model)

* Recall: **70% (4,109 / 5,900 defaulters detected)**
* False Negatives: **1,791 (lowest)**
* False Positives: **14,625**

### Random Forest (Comparison Model)

* Recall: **63% (3,721 / 5,900 detected)**
* False Negatives: **2,179**
* False Positives: **11,805**


## ⚖️ Trade-off Observed

* Logistic Regression detects **388 more defaulters** than Random Forest
* However, it produces **~2,800 more false positives**
* Reducing false positives leads to **higher missed defaulters (risk)**


## ✅ Final Model Selection

* Selected **Logistic Regression (default threshold = 0.5)**
* Reason: **Higher recall and lowest false negatives**, which is critical for this problem


## 🚀 Business Impact

This solution helps financial institutions:

* Identify **more high-risk customers** before loan approval
* Reduce **financial losses by minimizing missed defaulters**
* Support **better credit risk decision-making**, even with higher false alerts (manageable via manual review)


## 🔮 Future Improvements

- Implement advanced models (XGBoost, LightGBM)
- Perform feature engineering for better predictive power
- Use GridSearchCV for systematic hyperparameter tuning
- Deploy the model using Flask or Streamlit

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

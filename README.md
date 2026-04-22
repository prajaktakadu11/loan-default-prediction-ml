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

- Dataset is imbalanced (~11.5% defaulters)
- Baseline Model (threshold = 0.6):
     - Recall: 63% (3,721/5,900 detected)
     - False Negatives: 2,179
     - False Positives: 11,805
- Tuned Model (threshold = 0.55):
     - Precision: 37% (↑ from 24%)
     - False Positives: 3,014 (↓ significantly)
     - Recall: 29% (↓ from 63%)
     - False Negatives: 4,163
- Trade-off Observed:
     - Increasing threshold reduces false alarms
     - But significantly increases missed defaulters

The final model was selected based on business impact rather than accuracy.

Higher recall was prioritized to minimize False Negatives (missed defaulters)
False positives were considered acceptable as they can be reviewed manually


## 🚀 Business Impact

This solution can help financial institutions:

- Identify high-risk customers before loan approval.
- Reduce default-related financial losses.
- Improve overall credit risk management.


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

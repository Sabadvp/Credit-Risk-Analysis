# Credit Risk Analysis using Machine Learning

## 1. Project Overview

This project aims to develop a predictive model for identifying loan default risk using the Home Credit Default Risk dataset. The objective is to apply machine learning techniques to classify applicants based on their likelihood of experiencing payment difficulties.

The analysis follows a structured approach, including data preprocessing, feature engineering, model development, and performance evaluation. Emphasis is placed on both predictive accuracy and the interpretability of results in the context of financial risk assessment.

---

## 2. Dataset Description

* **Source:** Home Credit Default Risk (Kaggle)
* **Link:** https://www.kaggle.com/competitions/home-credit-default-risk/data

The dataset contains financial, demographic, and behavioral information related to loan applicants. Key attributes include:

* Income and credit-related variables
* Loan characteristics
* Demographic and household information

The target variable is defined as:

* **TARGET = 1**: Client with payment difficulty
* **TARGET = 0**: Client without payment difficulty

### Class Imbalance

The dataset is highly imbalanced:

* Approximately 92% non-default cases
* Approximately 8% default cases

This imbalance requires careful selection of evaluation metrics beyond accuracy.

> Note: The dataset is not included in this repository due to size and licensing restrictions. A reference link is provided.

---

## 3. Project Structure

```
Credit-Risk-Analysis/
│
├── README.md
├── notebooks/
│   └── credit_risk_analysis.ipynb
│
├── data/
│   └── data_link.txt
│
├── outputs/
│   ├── model_comparison_results.csv
│   └── cross_validation_results.csv
│
├── reports/
│   └── milestone2.pdf
```

---

## 4. Methodology

### 4.1 Data Preprocessing

The following preprocessing steps were applied:

* Removal of duplicate records
* Handling missing values:

  * Numerical variables were imputed using the median
  * Categorical variables were imputed using the mode
* Correction of abnormal values (e.g., unrealistic employment duration values)
* Feature scaling using standardization techniques

These steps ensured data quality and improved model performance.

---

### 4.2 Feature Engineering

To enhance predictive capability, additional variables were constructed based on domain knowledge:

* **Credit-to-Income Ratio**
* **Annuity-to-Income Ratio**
* **Credit-to-Annuity Ratio**

These features capture borrower affordability and repayment burden, which are critical factors in credit risk assessment.

---

## 5. Model Development

Three machine learning models were implemented:

### Logistic Regression

A baseline model used for its simplicity and interpretability.

### Random Forest

An ensemble model capable of capturing nonlinear relationships and interactions between variables.

### XGBoost

A gradient boosting model known for its strong predictive performance and ability to handle complex data patterns.

---

## 6. Model Evaluation

Given the class imbalance, multiple evaluation metrics were considered:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

Particular emphasis was placed on **recall** and **ROC-AUC**, as they provide better insight into model performance for imbalanced classification problems.

### Cross-Validation

A 5-fold cross-validation approach was used to assess model stability and generalizability. This reduces the risk of overfitting and ensures consistent performance across different data partitions.

---

## 7. Results

### 7.1 Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| XGBoost             | ~0.71    | ~0.15     | ~0.56  | ~0.24    | ~0.70   |
| Random Forest       | ~0.72    | ~0.15     | ~0.51  | ~0.23    | ~0.68   |
| Logistic Regression | ~0.61    | ~0.12     | ~0.60  | ~0.20    | ~0.64   |

---

### 7.2 Interpretation

* XGBoost achieved the highest ROC-AUC, indicating the strongest overall classification performance
* Logistic Regression achieved the highest recall, identifying the largest proportion of default cases
* Random Forest achieved the highest accuracy but demonstrated lower effectiveness in detecting default cases

These results highlight the importance of selecting evaluation metrics appropriate for imbalanced datasets.

---

## 8. Feature Importance Analysis

Feature importance analysis revealed that the most influential predictors include:

* Credit-to-Income Ratio
* Annuity-related financial ratios
* Employment duration
* Applicant age

These findings suggest that repayment burden and financial capacity are primary drivers of default risk.

---

## 9. Conclusion

The results demonstrate that machine learning models can effectively identify high-risk loan applicants. Among the models tested, XGBoost provided the best overall performance based on ROC-AUC, while Logistic Regression performed well in terms of recall.

The study emphasizes the importance of:

* Addressing class imbalance
* Using appropriate evaluation metrics
* Interpreting model outputs in a financial context

---

## 10. Tools and Technologies

* Python (Pandas, NumPy)
* Scikit-learn
* XGBoost
* Matplotlib and Seaborn
* Google Colab
* GitHub

---

## 11. Future Work

* Hyperparameter tuning for improved performance
* Integration of additional relational datasets
* Exploration of advanced models such as LightGBM
* Deployment of the model for real-time prediction

---

## Author

Saba Divanpour
Technical Business Systems Analyst | Data and Banking Systems

---

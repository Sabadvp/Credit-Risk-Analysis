# Credit Risk Analysis using Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--learn-orange)
![Model](https://img.shields.io/badge/Model-XGBoost-green)
![Status](https://img.shields.io/badge/Status-Completed-success)


## 📌 Project Overview

This project develops a **credit risk prediction system** using the Home Credit dataset to identify borrowers who are likely to default on their loans.

The goal is to support **data-driven decision-making** in lending by combining:

* financial feature engineering
* machine learning models
* interpretable insights

---

## 🧠 Key Highlights

✔ Built and compared **3 machine learning models**
✔ Handled **highly imbalanced dataset (~92% vs 8%)**
✔ Applied **cross-validation for model stability**
✔ Engineered **domain-driven financial features**
✔ Delivered **interpretable business insights**

---

## 📊 Dataset

* **Source:** Home Credit Default Risk (Kaggle)
* 🔗 https://www.kaggle.com/competitions/home-credit-default-risk/data

The dataset includes:

* applicant financial information
* demographic data
* loan attributes

> ⚠️ Dataset not included due to size and licensing constraints.

---

## 🏗️ Project Structure

```bash
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

## ⚙️ Methodology

### 🔹 Data Preparation

* Missing values handled (median / mode imputation)
* Outliers and abnormal values corrected (e.g., employment days)
* Feature scaling applied for model stability

---

### 🔹 Feature Engineering

To capture **real-world credit behavior**, the following features were created:

* **Credit-to-Income Ratio** → repayment burden
* **Annuity-to-Income Ratio** → affordability
* **Credit-to-Annuity Ratio** → loan structure

These features significantly improved model performance.

---

## 🤖 Models Developed

| Model               | Purpose                         |
| ------------------- | ------------------------------- |
| Logistic Regression | Baseline & interpretability     |
| Random Forest       | Non-linear relationships        |
| **XGBoost**         | High-performance boosting model |

---

## 📈 Model Evaluation

Due to class imbalance, multiple metrics were used:

* Accuracy
* Precision
* **Recall (critical for risk detection)**
* F1 Score
* **ROC-AUC (primary metric)**

Cross-validation ensured consistent performance across data splits.

---

## 🏆 Results Summary

| Model               | Accuracy | Recall    | ROC-AUC   |
| ------------------- | -------- | --------- | --------- |
| **XGBoost**         | ~0.71    | ~0.56     | **~0.70** |
| Random Forest       | ~0.72    | ~0.51     | ~0.68     |
| Logistic Regression | ~0.61    | **~0.60** | ~0.64     |

---

## 🔍 Key Insights

* **XGBoost achieved the best overall performance** based on ROC-AUC
* Logistic Regression captured the **highest number of risky customers**
* Financial ratios were the **strongest predictors of default risk**

👉 This confirms that **repayment burden is a critical factor in credit risk**

---

## 📊 Feature Importance

The model identified the following as most influential:

* Credit-to-Income Ratio
* Annuity-based features
* Applicant age and employment duration

These findings align with **real-world banking risk models**

---

## 💡 Business Impact

This model can support:

* Risk-based loan approval
* Early detection of high-risk applicants
* Improved credit scoring strategies

---

## 🛠️ Tech Stack

* Python (Pandas, NumPy)
* Scikit-learn
* XGBoost
* Matplotlib / Seaborn
* Google Colab
* GitHub

---

## 🚀 Future Improvements

* Hyperparameter tuning
* Advanced models (LightGBM, Neural Networks)
* Full dataset integration (all tables)
* Deployment as a web application

---

## 👤 Author

**Saba Divanpour**
Technical Business Systems Analyst | Data & Banking Systems

---

> ⭐ If you find this project useful, feel free to explore the notebook and results!

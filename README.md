# Machine-Learning-Internship# 🏦 Machine Learning Internship — Credit Scoring Model

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Data-green?style=for-the-badge&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

This project is part of a **Machine Learning Internship** focused on building a **Credit Scoring Model** that predicts whether a loan applicant should be approved or rejected based on their financial history and personal data.

The goal is to assist financial institutions in making faster, data-driven lending decisions using classification algorithms.

---

## 🎯 Objective

> Predict an individual's **creditworthiness** using past financial data by applying supervised machine learning classification techniques.

---

## 📁 Dataset

The dataset contains financial and personal information about loan applicants.

| Feature | Description |
|---|---|
| `Gender` | Male / Female |
| `Married` | Applicant marital status |
| `Dependents` | Number of dependents |
| `Education` | Graduate / Not Graduate |
| `Self_Employed` | Self-employed or not |
| `ApplicantIncome` | Income of the applicant |
| `CoapplicantIncome` | Income of the co-applicant |
| `LoanAmount` | Loan amount requested |
| `Loan_Amount_Term` | Term of loan in months |
| `Credit_History` | Credit history record |
| `Property_Area` | Rural / Semiurban / Urban |
| `Loan_Status` | ✅ Target Variable (Y/N) |

---

## ⚙️ Project Pipeline

```
Raw Data
   │
   ▼
Data Preprocessing
   ├── Handle Missing Values (Mode / Median)
   ├── Label Encoding (Binary Columns)
   └── Ordinal Encoding (Property Area)
   │
   ▼
Feature Engineering
   ├── Total_Income = ApplicantIncome + CoapplicantIncome
   ├── Income_Loan_Ratio = Total_Income / LoanAmount
   └── EMI = LoanAmount / Loan_Amount_Term
   │
   ▼
Train / Test Split (80/20) with Stratification
   │
   ▼
Feature Scaling (StandardScaler)
   │
   ▼
Model Training
   ├── Logistic Regression
   ├── Random Forest Classifier
   └── Gradient Boosting Classifier
   │
   ▼
Evaluation & Visualization
```

---

## 🧪 Models Used

| Model | Type | Notes |
|---|---|---|
| **Logistic Regression** | Linear Classifier | Baseline model |
| **Random Forest** | Ensemble (Bagging) | 100 decision trees voting |
| **Gradient Boosting** | Ensemble (Boosting) | Trees learn from previous errors |

---

## 📊 Evaluation Metrics

The following metrics are used to assess model performance:

- ✅ **Accuracy** — Overall correct predictions
- ✅ **Precision** — Of predicted approvals, how many were correct
- ✅ **Recall** — Of actual approvals, how many were caught
- ✅ **F1-Score** — Balance between Precision and Recall
- ✅ **ROC-AUC** — Model's ability to distinguish between classes
- ✅ **Confusion Matrix** — Visual breakdown of predictions

---

## 🔧 Feature Engineering

Three new features were engineered to improve model performance:

### 1. `Total_Income`
```python
Total_Income = ApplicantIncome + CoapplicantIncome
```
Combines both incomes to reflect the true financial capacity of the household.

### 2. `Income_Loan_Ratio`
```python
Income_Loan_Ratio = Total_Income / (LoanAmount + 1)
```
Measures affordability — higher ratio means loan is easier to repay.

### 3. `EMI`
```python
EMI = LoanAmount / (Loan_Amount_Term + 1)
```
Estimates the monthly installment burden on the applicant.

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/MuhammadSaadibnMaqsood/CodeAlpha-ML-Internhip-task-1
cd CodeAlpha-ML-Internhip-task-1
```


### 2. Add Dataset
Place your `train.csv` file in the root directory.

### 3. Run the Notebook
```bash
jupyter task1.ipynb
```

---

## 📦 Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter
```

Or install all at once:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

---

## 📂 Project Structure

```
Machine-Learning-Internship/
│
├── 📓 task1.ipynb     # Main Jupyter Notebook
├── 📄 train.csv                # Dataset (add manually)
└── 📄 README.md                # Project documentation
```

---

## 📈 Results

| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | ~83% | ~0.85 |
| Random Forest | ~85% | ~0.88 |
| Gradient Boosting | ~87% | ~0.90 |

> 📌 *Results may vary slightly depending on dataset version and random state.*

---

## 💡 Key Learnings

- Importance of **handling missing values** before encoding
- How **data leakage** can inflate model performance falsely
- Power of **feature engineering** in boosting accuracy
- Difference between **bagging vs boosting** ensemble methods
- Using **stratified splits** for imbalanced classification datasets

---

## 👨‍💻 Author

**Muhammad Saad**
Machine Learning Intern
📧 muhammadsaady0100@gmail.com

---

## 📜 License

This project is for **educational and internship purposes only.**

---

*Made with ❤️ during ML Internship*
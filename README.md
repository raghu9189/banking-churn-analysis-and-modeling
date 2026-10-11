# Banking Churn Analysis & Modeling

A machine learning and data analysis project designed to analyze customer churn patterns, uncover key drivers of customer attrition, and build predictive classification models to assist banks in proactive retention strategies.

---

## 📌 Problem Statement

Customer churn is a critical challenge in the banking industry. Acquiring new customers typically costs significantly more than retaining existing ones, and high attrition rates directly hurt recurring revenue and customer lifetime value.

Understanding **why**, **when**, and **which** customers leave empowers banks to intervene early with targeted retention campaigns, personalized offers, and service improvements.

---

## 🎯 Project Objectives

- **Pattern Discovery:** Conduct thorough exploratory data analysis to identify demographic and financial characteristics associated with customer churn.
- **Data Wrangling & Preprocessing:** Clean raw data, treat inconsistencies, address class imbalance (via SMOTE), and prepare feature matrices for machine learning algorithms.
- **Predictive Modeling:** Train and evaluate multiple classification algorithms (e.g., Logistic Regression, Random Forest, Gradient Boosting).
- **Model Interpretation:** Assess performance using Precision, Recall, F1-Score, and ROC-AUC, and interpret feature importances to provide actionable business recommendations.

---

## 📊 Dataset Overview

The dataset (`Churn-Data.csv`) contains records for **10,000 bank customers** with demographic, account, and transactional attributes.

### Data Dictionary

| S.No. | Column Name | Data Type | Description / Analytical Role |
|:---:|:---|:---:|:---|
| 1 | `RowNumber` | Integer | Sequential identifier for records (dropped). |
| 2 | `CustomerId` | Integer | Unique identifier for individual customers (dropped). |
| 3 | `Surname` | Object | Customer's surname with high cardinality (dropped). |
| 4 | `CreditScore` | Integer | Numerical credit score representing customer creditworthiness. |
| 5 | `Geography` | Object | Customer's country of residence (`France`, `Spain`, `Germany`). |
| 6 | `Gender` | Object | Customer's gender (`Male`, `Female`). |
| 7 | `Age` | Integer | Age of customer in years. |
| 8 | `Tenure` | Integer | Number of years the customer has banked with the institution. |
| 9 | `Balance` | Float | Current account balance. |
| 10 | `NumOfProducts` | Integer | Number of bank products/services utilized (1–4). |
| 11 | `HasCrCard` | Binary (`0`/`1`) | Indicates whether the customer holds a credit card. |
| 12 | `IsActiveMember` | Binary (`0`/`1`) | Indicates whether the customer is an active member. |
| 13 | `EstimatedSalary` | Float | Estimated annual salary/income. |
| 14 | `Exited` / `Churned` | Binary (`0`/`1` or `No`/`Yes`) | **Target variable**: whether the customer left the bank. |

---

## 🛠️ Project Workflow

The project follows a structured data science pipeline documented in [`notebook.ipynb`](notebook.ipynb):

1. **Importing Libraries and Loading the Dataset**
   - Core libraries setup (`numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy`).
   - Dataset ingestion and verification.
   - Initial structural inspection (`head`, `shape`, `columns`, `info`).

2. **Data Wrangling**
   - Missing value verification (0 null values detected; no imputation needed).
   - Duplicate detection (0 duplicate rows).
   - Cardinality analysis of categorical features.
   - Data cleaning: Dropping non-predictive identifiers (`RowNumber`, `CustomerId`, `Surname`).
   - Data transformation: Renaming target column to `Churned` and standardizing values (`No`/`Yes`).

3. **Exploratory Data Analysis (EDA)**
   - Target variable distribution and class balance analysis.
   - Univariate, bivariate, and multivariate analysis across demographic and financial indicators.
   - Key churn insights and behavioral correlations.

4. **Data Preprocessing**
   - Feature selection and importance ranking.
   - Categorical encoding (One-Hot / Ordinal Encoding) and feature scaling.
   - Train/Test split.
   - Handling class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).

5. **Model Building and Evaluation**
   - Candidate classification models selection.
   - Hyperparameter tuning and cross-validation.
   - Comprehensive model evaluation: Confusion Matrix, Accuracy, Precision, Recall, F1-Score, and ROC-AUC.
   - Feature importance extraction and business takeaways.

---

## 💻 Tech Stack

- **Language:** Python 3.x
- **Data Manipulation & Analysis:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Statistical Analysis & ML:** `scipy`, `scikit-learn`, `imbalanced-learn`
- **Environment:** Jupyter Notebook / Antigravity IDE

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/raghu9189/banking-churn-analysis-and-modeling.git
   cd banking-churn-analysis-and-modeling
   ```

2. **Create and activate a virtual environment (optional but recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn scipy scikit-learn imbalanced-learn notebook
   ```

4. **Launch the Jupyter Notebook:**
   ```bash
   jupyter notebook notebook.ipynb
   ```

---

## 📁 Repository Structure

```
├── Churn-Data.csv          # Bank customer churn dataset (10,000 records)
├── notebook.ipynb          # End-to-end data analysis and modeling notebook
└── README.md               # Project documentation and summary
```

---

## 👤 Author

- **Raghu Ballu** ([@raghu9189](https://github.com/raghu9189))

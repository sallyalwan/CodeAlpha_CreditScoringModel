# Credit Scoring Model — CodeAlpha Internship

## 📌 Project Overview
This project involves building a machine learning model to predict credit risk (Good vs. Bad) based on the **German Credit Dataset** (Prof. Hofmann). Unlike synthetic models, this project utilizes 20 historical financial attributes to identify patterns in borrower behavior and repayment probability.

## 📊 Key Insights from EDA
Before training, an Exploratory Data Analysis (EDA) was conducted:
* **Loan Amount:** Bad risk borrowers request ~32% more credit on average.
* **Duration:** Longer loan terms (24+ months) correlate strongly with higher default risk.
* **Savings:** Lower savings account balances are the strongest indicator of potential risk.

## 🛠️ Tech Stack & Workflow
* **Language:** Python 3.x
* **Libraries:** Pandas, Scikit-learn, Seaborn, Matplotlib
* **Features:** Includes a custom feature `amount_per_month` to measure monthly repayment burden.
* **Validation:** Used `StratifiedKFold` cross-validation to handle class imbalance.

## 📈 Model Performance
Three models were evaluated: Logistic Regression, Decision Tree, and Random Forest.

| Model | Accuracy | ROC-AUC | F1-Score |
| :--- | :--- | :--- | :--- |
| **Random Forest** | **76.5%** | **0.780** | **0.828** |
| Logistic Regression | 66.5% | 0.760 | 0.726 |
| Decision Tree | 67.0% | 0.641 | 0.753 |

**Random Forest** was selected as the final model due to its superior ability to handle non-linear relationships and its high AUC score.

## 🔑 Top Predictive Features
1. **Amount:** Total credit requested.
2. **Duration:** Length of the loan in months.
3. **Amount per Month:** The monthly installment burden.
4. **Savings:** Status of existing savings accounts.
5. **Credit History:** Past payment reliability.

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`


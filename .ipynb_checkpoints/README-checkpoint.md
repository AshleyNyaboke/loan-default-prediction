# Loan Default Prediction
### Using Machine Learning to Help Banks Identify High-Risk Borrowers

## Business Problem
Banks lose significant revenue when borrowers default on loans. 
This project builds a machine learning model that predicts the 
likelihood of loan default using borrower and loan characteristics, 
enabling banks to make smarter, data-driven lending decisions.

## Dataset
- **Source:** Kaggle — Loan Default Dataset
- **Size:** 148,670 loan records with 34 features
- **Target variable:** Status (1 = Default, 0 = No Default)

## Project Structure
- Data Exploration & Understanding
- Data Cleaning & Missing Value Treatment
- Exploratory Data Analysis (EDA)
- Model Building & Evaluation
- Data Leakage Detection & Fix
- Feature Importance Analysis
- Business Recommendations

## Key Findings
- 25% of loans in the dataset resulted in default
- LTV ratio, property value, and debt-to-income ratio 
  are the strongest predictors of default
- Credit score alone is NOT a strong predictor — 
  challenging traditional banking assumptions
- Joint applicants have the lowest default rate at 19%
- Incomplete applications correlate with higher default risk (29%)

## Models Built
| Model | Accuracy | Default Recall | Default Precision |
|-------|----------|---------------|-------------------|
| Logistic Regression | 78% | 25% | 63% |
| Random Forest (fixed) | 89% | 58% | 94% |

## Important Discovery: Data Leakage
During modelling, the initial Random Forest achieved 99.99% 
accuracy — identified as data leakage. Three columns contained 
post-approval information not available at prediction time. 
Removing these columns produced honest, deployable results.

## Business Recommendations
1. Prioritise LTV ratio in loan approval decisions
2. Look beyond credit scores — use debt-to-income ratio 
   and property value as stronger risk indicators
3. Flag incomplete applications as higher risk
4. Favour joint applications — lowest default rate observed

## Technologies Used
- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run
1. Clone this repository
2. Download the dataset from Kaggle: "Loan Default Dataset"
3. Open `loan_default_analysis.ipynb` in Jupyter Notebook
4. Run all cells from top to bottom

## Author
Ashley Nyaboke
Data Scientist | Python · SQL · Machine Learning
[GitHub](https://github.com/AshleyNyaboke)
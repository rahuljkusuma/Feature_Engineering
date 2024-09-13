# Feature Engineering


## Introduction
Feature engineering is a critical step in building a good **Credit Risk Model**. It involves creating new features or modifying existing ones to improve the predictive power of the model. While working in ABC, our team was planning to develop a score card and my manager asked me to do feature engineering for this model development. So I have followed below steps in feature engineering.

---

## 1. Data Preprocessing

- **Handling Missing Values**: Missing data can effect the model predictions. So first I have removed records with large proportion of missing data and then did imputation using mean, median or mode.
- **Encoding Categorical Variables**: Based on type of category I have used **Label Encoding** as well as **One-Hot Encoding**.
- **Scaling Numerical Features**: For some features I have checked the distribution and found that they are normally distributed, so I have used **Standardization**. I would have used **Normalization** for scaling, if the data is not normally distributed and with many outliers.
  
---

## 2. Key Features in Credit Risk Modelling

### 2.1. **Demographic Features**  
- **Age**: Younger borrowers may have a higher probability of default. Age can be used as is or binned into categories (e.g., 18–30, 31–45, 46+).
- **Marital Status**: Marital status can be correlated with financial stability.
- **Education Level**: Higher levels of education may indicate better financial literacy, reducing credit risk.

### 2.2. **Financial History Features**  
- **Credit Score**: The borrower’s credit score is a key indicator of creditworthiness.
- **Income Level**: Higher income levels usually correlate with lower credit risk.
- **Employment Status**: Stable employment indicates the ability to repay loans.
  
### 2.3. **Loan Features**
- **Loan Amount**: Larger loan amounts typically carry higher risk.
- **Loan Duration**: Longer loan terms may increase the risk of default.
- **Loan Purpose**: Certain types of loans (e.g., mortgage vs. personal loans) can have varying risk levels.

### 2.4. **Payment Behavior Features**
- **Payment History**: Past payment records (on-time, late payments, missed payments) are crucial indicators of future behavior.
- **Debt-to-Income Ratio**: This ratio helps to measure the borrower’s ability to manage monthly debt payments.
- **Number of Open Accounts**: More open accounts can indicate greater financial burden.

---

## 3. Feature Engineering Techniques

### 3.1. **Polynomial Features**
Creating interaction terms between features (e.g., income and age) can reveal non-linear relationships in the data.

### 3.2. **Binning and Discretization**
- **Binning**: Grouping continuous variables into discrete bins (e.g., grouping ages into ranges).
- **Discretization**: Transforming continuous features into categorical features, which can make the model more interpretable.

### 3.3. **Derived Features**
- **Debt-to-Income Ratio**: Calculated as total debt divided by total income.
- **Utilization Ratio**: The ratio of credit card balances to credit limits.

### 3.4. **Time-Based Features**
Creating features like:
- **Time Since Last Default**: Indicates the recency of a borrower's last default event.
- **Loan Tenure**: The length of time the loan has been active.
  
---

## 4. Feature Selection

Not all features contribute equally to the model’s performance. Feature selection helps to reduce overfitting, enhance model interpretability, and improve computational efficiency.

### Common Methods:
- **Correlation Analysis**: Remove highly correlated features.
- **Recursive Feature Elimination (RFE)**: Iteratively remove least important features based on model performance.
- **L1 Regularization (Lasso)**: Shrinks coefficients of less important features to zero.

---

## 5. Common Challenges in Feature Engineering

- **Multicollinearity**: When two or more features are highly correlated, it can distort the model's performance.
- **Imbalanced Data**: Credit risk data often has an imbalanced ratio of default vs. non-default cases. Techniques like oversampling, undersampling, or SMOTE can help balance the data.
- **Feature Drift**: Over time, the distribution of features may change, which can affect the model's performance.

---

## 6. Conclusion

Feature engineering is a key component in building effective credit risk models. By understanding the borrower’s demographic, financial behavior, and loan characteristics, along with applying the right transformation and selection techniques, one can significantly improve the model’s predictive power. Regularly revisiting and refining features is essential as economic conditions and borrower behaviors evolve over time.

---

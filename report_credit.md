
# Loan Risk Analysis Report

## Objective

The goal of this analysis is to evaluate the efficiency of a logistic regression model in classifying loans as healthy or high-risk. The dataset includes key financial metrics such as:
- Loan size
- Interest rate
- Borrower income
- Debt-to-income ratio
- Number of accounts
- Derogatory marks
- Total debt

### Target Variable
- **`loan_status`**: 
  - `0`: Healthy loan
  - `1`: High-risk loan

---

## Methodology

### Data Preparation
1. The dataset was divided into:
   - **Features (features_data)**: Predictor variables.
   - **Target (target_data)**: Labels indicating loan status.
2. Data splitting:
   - Training set and testing set were created using a random state of 1 to ensure reproducibility.

### Model Details
1. **Algorithm**: Logistic Regression
   - Selected for its effectiveness in binary classification.
2. **Implementation**:
   - Training was performed using the `LogisticRegression` module from the `scikit-learn` library.

---

## Outcomes

### Performance Metrics
- **Confusion Matrix**:
  ```
  [[18655   110]
   [   36   583]]
  ```
- **Accuracy**: `99.2%`
- **Precision (Label 1 - High-Risk Loans)**: `84.1%`
- **Recall (Label 1 - High-Risk Loans)**: `94.2%`

### Observations
- **Strengths**:
  - High overall accuracy (99.2%).
  - Robust precision for high-risk loans (84.1%).
- **Weaknesses**:
  - Despite high recall (94.2%), a small number of false positives and false negatives were identified.

---

## Conclusion

This logistic regression model is highly effective for loan risk classification. It reliably distinguishes between healthy and high-risk loans, making it a suitable tool for financial decision-making. However, to further reduce false negatives (i.e., missed high-risk loans), additional optimization or alternative algorithms could be explored.

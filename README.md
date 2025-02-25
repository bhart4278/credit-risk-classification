# credit-risk-classification

## Credit Risk Classification Report

Utilize supervised machine learning to evaluate a lending activity dataset and predict risk level.

### Overview of the Analysis

The purpose of this analysis was to build a supervised machine learning model to predict whether a loan is classified as healthy or high-risk. The dataset used contained financial information such as loan amount, interest rate, borrower income, debt levels, and other relevant financial indicators. The dataset was imbalanced, with significantly fewer high-risk loans compared to healthy loans.

To perform the machine learning process, the data was:

- Split into labels (loan status: healthy or high-risk) and features (financial variables).
- Further split into training and testing datasets.
- Processed using a `LogisticRegression` model from scikit-learn with a max iteration value of 500.
- Model fit to the training data
- Used test data to make model predictions.
- Evaluated using accuracy, precision, recall, balanced accuracy, and f1 scores.

### Results

#### Logistic Regression Model

- **Accuracy**: 99%
- **Balanced Accuracy**: 96.73%
- **Precision**:
  - Healthy Loans (0): 100%
  - High-Risk Loans(1): 84%
- **Recall**:
  - Healthy Loans(0): 99%
  - High-Risk Loans(1): 94%

### Summary

The Logistic Regression model provides strong predictive performance for classifying healthy loans. However, misclassification of high-risk loans as healthy remains a concern, given the potential financial implications.

Key Observations:

- The model predicts  healthy loans with 100% accuracy, risky loans with 84%.
- Due to the imbalanced nature of the dataset (very little high risk behavior in dataset), the model may underperform in identifying high-risk loans.
- Adjusting the dataset by balancing the number of high-risk and healthy loans or experimenting with different machine learning models could enhance the model's ability to identify high-risk loans more accurately.

### Model Pros and Cons

**Pros:**

- High accuracy in classifying healthy loans.
- Efficient and computationally inexpensive model.
- Suitable for binary classification problems.

**Cons:**

- Imbalanced dataset leads to fewer high-risk loan samples for training.
- Potential misclassification of high-risk loans as healthy.
- Lack of probability-based outputs for loans near decision boundaries.

If this model were applied to real-world loan approvals, additional data on high-risk loans or alternative modeling approaches might be necessary to mitigate risks effectively. Reducing false negatives (misclassified high-risk loans) is crucial to minimizing financial risk.


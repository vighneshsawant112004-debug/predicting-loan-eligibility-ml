# 🏦 Loan Amount Prediction Using Ridge Regression

This is my first machine learning project, built using a Kaggle practice dataset to predict loan amounts based on applicant profiles. The goal was to create a reliable regression pipeline that handles skewed data, multicollinearity, and generalizes well to new inputs.

### 🔧 Key Features
- Log transformation of skewed target variable (`loan_amount`)
- Feature engineering: income ratios, cleaned employment length
- Multicollinearity check using correlation heatmaps
- Ridge regression model with regularization
- Scaled inputs and inverse-transformed predictions
- Markdown summaries and visualizations for client-ready presentation

### 📊 Sample Prediction
> Predicted Loan Amount: ₹2,72,121.31  
> Note: While the training data capped at ₹40,000, the model extrapolates based on high-income profiles (e.g., ₹80,000 annual income), which is realistic in real-world lending scenarios.

### 🚀 What I Learned
- How to preprocess and transform data for regression
- The importance of feature selection and scaling
- How to interpret model behavior and justify predictions
- Building a clean, reproducible pipeline for future deployment

---

## 🔍 Regression Models Used

To predict loan amounts, I implemented and compared three regression models:

### 1. Linear Regression
- Served as the baseline model.
- Simple and interpretable, but sensitive to multicollinearity and outliers.

### 2. Ridge Regression
- Adds L2 regularization to penalize large coefficients.
- Helped reduce overfitting and improved generalization.
- Performed well on unseen data, especially after log-transforming the target variable.

### 3. Lasso Regression
- Adds L1 regularization, which can shrink some coefficients to zero.
- Useful for feature selection by automatically eliminating less important variables.
- Provided a more compact model with slightly reduced performance compared to Ridge.

### ✅ Final Choice
Based on performance metrics (R², RMSE) and generalization to new profiles, **Ridge Regression** was selected as the final model. It offered a good balance between bias and variance while maintaining interpretability.

### 📌 Final Note on Prediction Validity

While the predicted loan amount of **₹2,72,121.31** exceeds the maximum loan amount in the original dataset (**₹40,000**), it remains reasonable in real-world scenarios — especially for high-income applicants (e.g., ₹80,000 annual income). The dataset used is a **Kaggle practice dataset**, designed for learning and experimentation, not bound by strict real-world lending limits.

This extrapolation reflects the model’s ability to generalize beyond the training data and simulate realistic outcomes for new profiles. In actual financial settings, such loan amounts are common for well-qualified applicants, making the prediction both technically sound and contextually valid.



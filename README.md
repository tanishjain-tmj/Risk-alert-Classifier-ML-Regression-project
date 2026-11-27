# 💳 Credit Risk Classification Using Machine Learning

🎥 **Project Video Presentation:** [Watch Project Presentation](https://drive.google.com/file/d/1GD4fDJQpckd6YPEz-LzyjFd_mpjbBp0N/view?usp=sharing)

---

## 📌 Project Overview

This project focuses on predicting customer credit risk using Machine Learning classification algorithms. The objective is to classify customers into **Low Risk (0)** and **High Risk (1)** categories based on their financial and banking-related information.

The project explores data preprocessing, class imbalance handling, model training, hyperparameter tuning and performance evaluation to identify the most suitable classification model.

## 🎯 Project Objectives

- Understand and preprocess customer credit data.
- Handle missing values using KNN Imputation.
- Apply encoding and feature scaling.
- Build classification models to predict credit risk.
- Analyze the impact of class imbalance.
- Optimize models using Randomized Search CV and Grid Search CV.
- Evaluate models using classification metrics and ROC-AUC.
- Select the best model based on minimizing False Negatives.

## 📂 Dataset Information

The dataset contains customer-related information, including:

- Customer Age and Gender
- Region and Employment Type
- Annual Income
- Credit Score
- Credit Utilization Ratio
- Missed Payments
- Average Late Payment Days
- Monthly Transactions and Spending
- Cash Advance Count
- Account Tenure
- Debt Balance

**Target Variable:** `risk_status`

- `0` – Low Risk
- `1` – High Risk

`customer_id` is excluded because it is an identifier and does not contribute to prediction.

## 🛠️ Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Identified missing values.
- Applied KNN Imputation for numerical features.
- Used most-frequent imputation for categorical features.
- Applied One-Hot Encoding.
- Applied Standard Scaling.
- Performed stratified train-test splitting.

### 2. Model Building

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

### 3. Handling Class Imbalance

- Random Under-Sampling
- Random Over-Sampling
- SMOTE
- ADASYN

### 4. Hyperparameter Tuning

- Randomized Search CV
- Grid Search CV

Recall was used as the optimization metric to prioritize identifying high-risk customers.

### 5. Model Evaluation

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-Score
- ROC Curve
- AUC-ROC Score
- False Positive and False Negative analysis

## 📊 Model Performance

### Logistic Regression – Best Performing Model

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 99.89% |
| Precision | 99.20% |
| Recall | 100% |
| F1-Score | 99.60% |
| AUC-ROC | 0.99999 |

### Confusion Matrix

| | Predicted Low Risk | Predicted High Risk |
|---|---:|---:|
| Actual Low Risk | 795 | 1 |
| Actual High Risk | 0 | 124 |

**Key Observations:**
- Correctly identified all 124 high-risk customers.
- Achieved zero False Negatives.
- Produced only one False Positive.
- Demonstrated excellent classification performance.

### Impact of Class Balancing

All four balancing techniques achieved 100% Recall.

However, the original Logistic Regression model achieved the highest F1-score of approximately 99.60%, indicating that balancing did not improve its overall test performance.

### Model Comparison – AUC-ROC

| Model | AUC-ROC |
|---|---:|
| Logistic Regression | 0.999990 |
| Decision Tree | 0.928838 |
| Random Forest | 0.999737 |
| Tuned Model | 0.999873 |

Logistic Regression achieved the highest AUC-ROC score among the evaluated models.

## 🏆 Final Conclusion

Logistic Regression was selected as the best-performing model for this Credit Risk Classification project.

It achieved 99.89% accuracy, 100% recall and zero False Negatives on the test dataset.

Since identifying high-risk customers is the primary business requirement, Logistic Regression proved to be the most suitable model based on the evaluation results.

This project demonstrates the importance of data preprocessing, class imbalance handling, hyperparameter tuning and appropriate evaluation metrics in developing classification models.

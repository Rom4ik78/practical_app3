
# 📊 Comparing Classifiers for Bank Marketing Campaigns

### KNN • Logistic Regression • Decision Trees • Support Vector Machines (SVM)

This project is part of the Berkeley Professional Certificate in Machine Learning and Artificial Intelligence.

## 🎯 Business Objective

A Portuguese banking institution conducted direct marketing campaigns via telephone calls. The goal is to predict whether a client will subscribe to a term deposit.

This is a binary classification problem where:

- **yes** = client subscribes to a term deposit
- **no** = client does not subscribe

Because the dataset is imbalanced, evaluation focuses not only on Accuracy but also on Precision, Recall, F1-score, and ROC-AUC.

---

## 📂 Dataset

- 45,211 observations
- 16 input features
- 1 target variable
- No missing values

Features include:

- Demographics (age, job, marital status, education)
- Financial information (balance, loans, defaults)
- Campaign information (contact type, duration, month)
- Previous campaign history

---

## 🛠️ Data Preparation

### Data Cleaning

- Verified no missing values.
- Checked data types and target distribution.
- Encoded target variable into binary format.
- Performed train/test split before model evaluation.

### Feature Engineering

- One-Hot Encoding for categorical variables.
- StandardScaler for numerical variables.
- Scikit-Learn Pipelines used to avoid data leakage.
- Stratified 5-fold cross validation.

---

## 📊 Exploratory Data Analysis

Key observations:

- Longer call duration strongly correlates with successful subscriptions.
- Previous successful campaigns significantly increase conversion probability.
- Clients without personal loans subscribe more often.
- Customer age and account balance provide moderate predictive power.

The dataset is imbalanced, making ROC-AUC, Recall, and F1-score particularly important.

---

## 🤖 Models Evaluated

### Logistic Regression

Advantages:
- Fast training
- Interpretable coefficients
- Strong baseline performance

### K-Nearest Neighbors (KNN)

Advantages:
- Simple and intuitive
- Non-parametric

Disadvantages:
- Expensive predictions
- Sensitive to scaling

### Decision Tree

Advantages:
- Easy interpretation
- Captures nonlinear relationships

Disadvantages:
- Risk of overfitting

### Support Vector Machine (SVM)

Advantages:
- Excellent class separation
- Strong predictive performance

Disadvantages:
- Computationally expensive

---

## 🔧 Hyperparameter Tuning

### Logistic Regression

Best Parameters:

- C = 0.1
- class_weight = balanced
- l1_ratio = 1

Best CV ROC-AUC:

0.9122

### Decision Tree

Best Parameters:

- criterion = entropy
- max_depth = 20
- min_samples_leaf = 5
- min_samples_split = 2
- class_weight = balanced
- ccp_alpha = 0.001

Best CV ROC-AUC:

0.9099

### KNN

Best Parameters:

- n_neighbors = 31
- p = 2
- weights = distance

Best CV ROC-AUC:

0.8928

### SVM

Best Parameters:

- kernel = rbf
- C = 10
- gamma = 0.01
- class_weight = balanced

Best CV ROC-AUC:

0.9258

---

## 📈 Evaluation Metrics

### Accuracy

Measures overall classification correctness.

### Precision

Measures how many predicted subscribers actually subscribed.

### Recall

Measures how many actual subscribers were identified.

### F1-score

Balances Precision and Recall.

### ROC-AUC

Measures the model's ability to separate subscribers from non-subscribers across all classification thresholds.

---

## 📊 Final Model Comparison

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC | Fit Time (s) | Predict Time (s) |
|---------|---------:|---------:|---------:|---------:|---------:|---------:|---------:|
| Logistic Regression | 0.8498 | 0.4265 | 0.8223 | 0.5617 | 0.9087 | 8.50 | 0.014 |
| SVM | 0.8402 | 0.4139 | 0.8790 | 0.5628 | 0.9250 | 72.87 | 3.93 |

---

## 📈 Business Interpretation

In a marketing campaign, Recall is especially important because failing to identify a potential subscriber results in a missed sales opportunity.

The SVM model identified nearly 88% of all potential subscribers.

However, Logistic Regression achieved:

- Higher Accuracy
- Similar F1-score
- Strong ROC-AUC
- Nearly 9x faster training time
- Faster predictions
- Easier interpretability

---

## 🏆 Final Recommendation

### Recommended Model: Logistic Regression

Although SVM produced the best ROC-AUC and Recall, Logistic Regression delivered nearly identical overall performance while requiring substantially fewer computational resources.

Reasons:

1. Highest Accuracy (0.8498)
2. Strong ROC-AUC (0.9087)
3. Competitive Recall (0.8223)
4. Fast training and inference
5. Easier deployment
6. Better interpretability

For production deployment and business decision-making, Logistic Regression provides the best balance between predictive performance and operational efficiency.

---

## 🔮 Future Work

Potential improvements:

- XGBoost
- LightGBM
- CatBoost
- SMOTE for class balancing
- Feature selection methods
- Threshold optimization
- Cost-sensitive learning

---

## 📬 Author

Roman Andreev

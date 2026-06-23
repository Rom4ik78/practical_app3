# 📊 Comparing Classifiers for Bank Marketing Campaigns

### KNN • Logistic Regression • Decision Trees • Support Vector Machines (SVM)

This project is part of **Module 17** of the **Berkeley Professional Certificate in Machine Learning and Artificial Intelligence**.

The objective is to evaluate and compare the performance of four supervised learning algorithms—**K-Nearest Neighbors (KNN), Logistic Regression, Decision Trees, and Support Vector Machines (SVM)** using the Bank Marketing dataset. The models are trained to predict whether a client will subscribe to a term deposit following a telephone marketing campaign.

The project follows a structured machine learning workflow including **data exploration, preprocessing, feature engineering, model training, hyperparameter tuning, and performance evaluation** using metrics such as Accuracy, Precision, Recall, F1-score, ROC-AUC, and training time.

## 📂 Dataset Description

The data is related to direct marketing campaigns conducted by a Portuguese banking institution. The marketing campaigns were based on telephone calls. In many cases, multiple contacts with the same client were required to determine whether the client would subscribe to a bank term deposit.

The dataset used in this project is **`bank-full.csv`**, which contains all observations ordered chronologically from **May 2008 to November 2010**.

### 🎯 Objective

The classification task is to predict whether a client will subscribe to a term deposit (**target variable `y`**).

### Dataset Characteristics

| Property             | Value                           |
| -------------------- | ------------------------------- |
| Number of Instances  | 45,211 (`bank-full.csv`)        |
| Number of Attributes | 16 features + 1 target variable |
| Missing Values       | None                            |

---

## Feature Groups

| Group                                           | Features                                                      |
| ----------------------------------------------- | ------------------------------------------------------------- |
| **Client Demographics & Financial Information** | age, job, marital, education, default, balance, housing, loan |
| **Current Campaign Contact Information**        | contact, day, month, duration                                 |
| **Previous Campaign History**                   | campaign, pdays, previous, poutcome                           |
| **Target Variable**                             | y                                                             |

---

## Feature Description

| #  | Feature   | Type            | Description                                                                           | Possible Values                                                                                                                      |
| -- | --------- | --------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| 1  | age       | Numeric         | Age of the client                                                                     | N/A                                                                                                                                  |
| 2  | job       | Categorical     | Type of job                                                                           | admin., unknown, unemployed, management, housemaid, entrepreneur, student, blue-collar, self-employed, retired, technician, services |
| 3  | marital   | Categorical     | Marital status                                                                        | married, divorced (includes widowed), single                                                                                         |
| 4  | education | Categorical     | Education level                                                                       | unknown, secondary, primary, tertiary                                                                                                |
| 5  | default   | Binary          | Has credit in default?                                                                | yes, no                                                                                                                              |
| 6  | balance   | Numeric         | Average yearly balance (EUR)                                                          | N/A                                                                                                                                  |
| 7  | housing   | Binary          | Has a housing loan?                                                                   | yes, no                                                                                                                              |
| 8  | loan      | Binary          | Has a personal loan?                                                                  | yes, no                                                                                                                              |
| 9  | contact   | Categorical     | Communication type used for the last contact                                          | unknown, telephone, cellular                                                                                                         |
| 10 | day       | Numeric         | Day of the month of the last contact                                                  | 1–31                                                                                                                                 |
| 11 | month     | Categorical     | Month of the last contact                                                             | jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec                                                                           |
| 12 | duration  | Numeric         | Duration of the last contact (seconds)                                                | N/A                                                                                                                                  |
| 13 | campaign  | Numeric         | Number of contacts performed during the current campaign (including the last contact) | N/A                                                                                                                                  |
| 14 | pdays     | Numeric         | Days since the client was last contacted in a previous campaign                       | -1 = client was not previously contacted                                                                                             |
| 15 | previous  | Numeric         | Number of contacts before the current campaign                                        | N/A                                                                                                                                  |
| 16 | poutcome  | Categorical     | Outcome of the previous marketing campaign                                            | unknown, other, failure, success                                                                                                     |
| 17 | y         | Binary (Target) | Has the client subscribed to a term deposit?                                          | yes, no                                                                                                                              |
---

## 🛠️ Data Preparation and Feature Engineering

The following preprocessing steps significantly improved model quality.

### Data Cleaning


### Feature Engineering


---

## 🎯 Problem Statement
---

## 📊 Key Results

---

## ✅ Conclusion

---

## 🚀 How to Run

```bash
git clone https://github.com/Rom4ik78/practical_app3.git
cd practical_app3
pip install -r requirements.txt
jupyter notebook prompt_III.ipynb
```

---

## 📎 Project Structure

```text
├── data/
├── prompt_III.ipynb
├── README.md
└── requirements.txt
```

---

## 📬 Author

**Roman Andreev**  
📧 roman.andreev@me.com

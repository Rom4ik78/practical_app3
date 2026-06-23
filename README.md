
# Additional README Sections for Portfolio Version

## 📊 Exploratory Data Analysis (EDA)

### Target Distribution

The dataset is highly imbalanced.

| Class | Percentage |
|---------|---------:|
| No Subscription | ~88% |
| Subscription | ~12% |

This imbalance makes Accuracy alone insufficient for model evaluation. Therefore, Precision, Recall, F1-score, and ROC-AUC were used as primary performance metrics.

### Key Observations

- Clients contacted for a longer duration were more likely to subscribe.
- Previous successful marketing outcomes (`poutcome = success`) strongly correlated with positive responses.
- Customers without personal loans showed higher subscription rates.
- Age and account balance demonstrated moderate predictive power.

## 🤖 Models Evaluated

### K-Nearest Neighbors (KNN)
Advantages:
- Simple and intuitive.
- No training phase.

Disadvantages:
- Computationally expensive during prediction.
- Sensitive to feature scaling.

### Logistic Regression
Advantages:
- Fast training and prediction.
- Interpretable coefficients.
- Strong baseline model.

### Decision Tree
Advantages:
- Easy to interpret.
- Captures nonlinear relationships.

Disadvantages:
- Prone to overfitting.

### Support Vector Machine (SVM)
Advantages:
- Strong classification performance.
- Excellent class separation.

Disadvantages:
- Computationally expensive on large datasets.

## 🔧 Hyperparameter Tuning

GridSearchCV was used to identify optimal hyperparameters.

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

## 📈 Business Impact

For a marketing campaign, Recall is particularly important because missing a potential subscriber may result in lost revenue opportunities.

SVM achieved the highest Recall (0.8790), while Logistic Regression delivered similar predictive performance with significantly lower computational cost.

## 🔮 Future Work

- Gradient Boosting
- XGBoost
- LightGBM
- CatBoost
- SMOTE
- Feature Selection
- Threshold Optimization

## 🏆 Final Recommendation

Recommended Model: Logistic Regression

Reasons:
1. Highest Accuracy
2. Strong ROC-AUC
3. Competitive Recall
4. Fast training and prediction
5. High interpretability
6. Easier deployment and maintenance

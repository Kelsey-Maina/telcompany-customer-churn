# telcompany-customer-churn

# BUSINESS UNDERSTANDING.

I have been tasked by SyriaTel, a telecommunications company, to identify patterns and factors that will enable them to anticipate customer behavior and take proactive steps to reduce churn rates. For this analysis, I'm leveraging data from the SyriaTel dataset that contains data on customers' usage patterns and service information. As a result of the predictive analysis, the firm will be able to retain their clients. Overall, SyriaTel is looking to obtain predictive machine learning models that can predict whether customers are likely to churn or not.

### Objectives;

1. To build machine learning models that will predict how likely a customer will churn by analyzing customer features.

2. To identify the specific features that influence the rate of customer churn.

3. To determine the most accurate model in predicting the classification of churn/non-churn customers.

# DATA UNDERSTANDING.

This project analysis uses previous customer data from SyriaTel telecommunications company, which contains customer and service information. The dataset contains 3333 rows and 21 columns which include: Demographic data, customer usage patterns and service information. The target variable in the dataset is `churn`.

# DATA CLEANING.

The dataset is complete as it has no null values or duplicates, but some variables contain outliers.

# MODELLING.

## Model 1; Logistic Regression Model

Based on the evaluation results of the logistic regression model, the conclusions are:

- Cross-Validation Score: The mean recall score obtained from 6-fold cross-validation is approximately 0.783.

- Accuracy: The accuracy of the logistic regression model on the test set is approximately 0.79. 

- Precision: The precision of the logistic regression model is approximately 0.40. 

- Recall: The recall score of the logistic regression model is approximately 0.69. 

- F1-score: The F1-score of the logistic regression model is approximately 0.51.

## Model 2; Decision Tree Classifier

Based on the evaluation results of the decision tree classifier, the conclusions are:

- Cross-Validation Score: The mean recall score obtained from 6-fold cross-validation is approximately 0.848. 

- Accuracy: The accuracy of the decision tree classifier on the test set is approximately 0.88.

- Precision: The precision of the decision tree classifier is approximately 0.58.

- Recall: The recall score of the decision tree classifier is approximately 0.84. 

- F1-score: The F1-score of the decision tree classifier is approximately 0.69.

## Model 3; Random Forest 

Based on the evaluation results of the random forest, the conclusions are:

- Cross-Validation Score: The mean recall score obtained from 6-fold cross-validation is approximately 0.88. 

- Accuracy: The accuracy of the random forest on the test set is approximately 0.88.

- Precision: The precision of the random forest is approximately 0.60.

- Recall: The recall score of the random forest is approximately 0.66. 

- F1-score: The F1-score of the random forest is approximately 0.63.

## Model 4; KNN

Based on the evaluation results of the KNN model, the conclusions are:

- Cross-Validation Score: The mean recall score obtained from 6-fold cross-validation is approximately 0.903. 

- Accuracy: The accuracy of the KNN model on the test set is approximately 0.82.

- Precision: The precision of the KNN model is approximately 0.44.

- Recall: The recall score of the KNN model is approximately 0.64. 

- F1-score: The F1-score of the KNN model is approximately 0.52

## Finding the most important features;

![image](https://github.com/Kelsey-Maina/telcompany-customer-churn/assets/162282707/fcadcea9-83e5-41a2-8e03-527dc5ea9d61)

The `top features` that influence the rate of customer churn (in order) are:

- total day charge

- customer service calls

- total eve charge

# EVALUATION.

The recall scores and accuracy from the data frame above match the previous individual models. The `best` model from this data frame is the `Decision tree` with a recall score of 0.832, while the `worst` model is the `Random Forest` with a recall score of 0.248. For the Decision Tree, this means that the model is able to correctly identify around 83.2% of the churned customers in the test set. It represents the proportion of actual churned customers that were correctly identified by the model.

In the context of predicting customer churn for a telecommunications company, it is generally more important to focus on recall scores rather than accuracy because; If the model has high accuracy but low recall, it might be correctly predicting most non-churners but missing many actual churners. 

Moreover, other metrics like precision and F1 score, are important as they ensure a balanced approach. Precision ensures that the customers I am targeting with retention strategies are actually likely to churn, and the F1-score provides a balance between precision and recall.

## ROC Curve analysis

![image](https://github.com/Kelsey-Maina/telcompany-customer-churn/assets/162282707/ef84fc8d-a9da-42bf-b08a-0b26f33043f6)

The best model with the highest AUC is the `Decision Tree`, as it is the curve at the top left corner of the plot. This curve represents the model with the highest True Positive Rate (TPR) and the lowest False Positive Rate (FPR), which corresponds to the highest AUC (Area Under the Curve) of 0.885

# CONCLUSION.

`Decision Tree model` is the 'best' model performer among the four models. This would be the best Model for the SyriaTel Telecommunication Company to use to predict which customers will churn and take precautionary steps to reduce the churn rate.

The 'most' important feature for predicting churn is `total day charge`, which has a score of 0.231818. This means that the amount of money a customer spends on day calls is a strong predictor of whether they will churn. Other important features include `total eve charge, total intl charge, and international plan_yes` which relate to the amount of money a customer spends on their phone service moreover, another important feature `customer service calls` relates to the service quality of the company, which is a strong predictor of churn.

The 'least' important features are `voice mail plan_yes and area code`.

# RECOMMENDATIONS.

1. Reduce the total day charge on calls.

2. Improve the service quality on customer service calls.

3. Reduce the total eve charge on calls.

4. Focus on offering international plans to customers.

# NEXT STEPS.

1. Develop incentive programs for day calls reduction.

2. Enhance customer service experience.

3. Explore strategies for eve charge reduction.

4. Expand and introduce appealing international plans.

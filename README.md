# Understanding-Customer-Churn
Understanding the Factors Linked to Customer Churn in the Automotive Industry
### Overview

This repository delves into the factors contributing to customer churn in the automotive industry and explains the impact of these factors using Explainable AI (XAI) techniques, particularly SHAP (SHapley Additive exPlanations). The project aims to not only predict customer churn with high accuracy but also to provide a transparent understanding of the underlying drivers influencing customer behavior. By leveraging SHAP, we break down complex machine learning models into comprehensible insights, empowering businesses to implement targeted retention strategies based on interpretable model outputs.

### Dataset Information

1) Source: The dataset, sourced from Kaggle, consists of synthetic data that emulates customer information due to privacy constraints.
2) Size: 100,000 records with 22 features, including demographic details, financial data, and churn status.
3) Class Imbalance: The dataset exhibits a skewed distribution, with more non-churning customers than churning ones.

## Key Features:
Tenure Time: Duration a customer has been subscribed to the service.
Age: Customer’s age at the time of data collection.
Premium Amount: Annual premium amount paid by the customer.
Income: Customer’s annual income.
Marital Status: Whether the customer is married, single, etc.

##Methodology
The project follows a structured approach, beginning with data understanding and preparation, followed by model development, evaluation, and explainability analysis using SHAP.

1. Business Understanding
Understanding customer churn is crucial for businesses aiming to retain clients and ensure sustainable growth. By predicting churn and comprehending the factors that drive it, companies can deploy targeted strategies to minimize attrition.

2. Data Understanding
Exploratory Data Analysis (EDA) was performed to identify key trends, patterns, and any inconsistencies within the dataset.
The characteristics and distributions of the features were analyzed to understand their relationship with customer churn.

3. Data Preparation
Handling Missing Data: Missing values in features like latitude, longitude, and home market value were appropriately imputed or dropped based on their relevance and impact.
Feature Selection:
Logistic Regression (Logit): Used to identify statistically significant features.
Variance Inflation Factor (VIF): Employed to eliminate features with high multicollinearity.
Addressing Class Imbalance:
Undersampling: Reduced the majority class size to balance the dataset.
Oversampling: Synthesized new instances in the minority class to improve model training.
Encoding Categorical Variables: Used one-hot encoding for categorical variables to convert them into a suitable format for modeling.
Feature Scaling: Applied RobustScaler and MinMaxScaler to normalize numerical features.

4. Modeling
We applied various machine learning algorithms to develop churn prediction models:

Decision Tree
Artificial Neural Network (ANN)
Random Forest
XGBoost
AdaBoost
Logistic Regression
Naive Bayes

5. Hyperparameter Optimization
Hyperparameters for each model were fine-tuned using the Hyperopt library, with the objective of maximizing the ROC-AUC score through Bayesian optimization techniques.

6. Evaluation
Models were assessed based on several metrics, including:

Accuracy: Measures the proportion of correctly classified cases.
F1 Score: Balances precision and recall, crucial for imbalanced datasets.
Precision & Recall: Evaluates the model’s ability to predict churn accurately.
Random Forest and XGBoost demonstrated superior performance, showing high accuracy and reliability in identifying churning customers.

7. Model Explainability
To understand the factors influencing churn, we used SHAP to explain the predictions made by our models. Key insights include:

Tenure: Short tenure increases churn risk.
Age: Younger customers are more likely to churn.
Premium Amount: Higher premium amounts correlate with a higher likelihood of churn.
8. SHAP Analysis:
Visualizes the contribution of each feature to the model’s predictions.
Provides interpretable insights, aiding stakeholders in understanding the driving forces behind churn.

## Results
1. Top Models: Random Forest and XGBoost outperformed others in terms of accuracy and interpretability.
2. SHAP Insights: Highlighted key drivers of churn, enabling actionable strategies for customer retention.

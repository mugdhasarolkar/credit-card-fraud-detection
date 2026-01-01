Project Objective
The main objective of this project is to build a machine learning model on a credit card transaction dataset to accurately detect fraudulent transactions.

Dataset Overview
The dataset contains transaction records with the following features:

Account Information: Account Number, CVV.

Customer Demographics: Gender, Marital Status, City Address.

Transaction Details: Card Colour, Card Type, Domain, Amount.

Financial Metrics: Average Income Expenditure.

Target Variable: Outcome (0 for Valid, 1 for Fraud).

Project Workflow
Data Cleaning:

Checked for null values; the Customer Age feature was dropped due to significant missing data.

Verified that there were no duplicate records in the dataset.

Feature Engineering:

Converted categorical string data into numeric types using OrdinalEncoder from scikit-learn.

Handling Class Imbalance:

The dataset initially contained 27,370 fraud cases and 9,727 valid cases.

Under-sampling (using NearMiss) was applied to balance the training data.

Modeling: Tested multiple classifiers including:

Decision Tree

Logistic Regression

Random Forest

Results
The Random Forest Classifier outperformed other models with the following metrics:

Accuracy: ~85.93% (after K-Fold Cross Validation)

Precision: 0.919

Recall: 0.882

F1 Score: 0.900

Tech Stack
Language: Python
Libraries: pandas, numpy, scikit-learn, seaborn, matplotlib, imblearn.


Libraries: pandas, numpy, scikit-learn, seaborn, matplotlib, imblearn.

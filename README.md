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

Why These Choices Were Made

1.Dropping 'CustomerAge': During data cleaning, it was found that the CustomerAge feature had a significant number of missing values. To maintain a high-quality dataset and avoid introducing bias through estimation, I made the decision to remove this column.

2.Using Ordinal Encoding: Since the dataset contained categorical string information (like Gender and Card Type), I used an OrdinalEncoder to convert these into numeric values. This allowed the machine learning algorithms to process the categorical metadata effectively.

3.Balancing the Dataset (NearMiss): The initial dataset was highly imbalanced, with 27,370 fraud cases compared to only 9,727 valid cases. I applied NearMiss undersampling to balance the classes. This prevented the model from becoming biased toward the majority class and improved its ability to detect actual fraud.

4.Selecting Random Forest: After testing multiple models (Decision Tree, Logistic Regression, and Random Forest), the Random Forest Classifier was selected. It provided the best overall performance, likely because it can handle the complex, non-linear relationships found between features like 'Amount' and 'Outcome'.

5.K-Fold Cross-Validation: To ensure the 85.93% accuracy was reliable and not just a result of a lucky data split, I implemented 5-fold cross-validation. This confirms that the model is robust and performs consistently across different subsets of data.

Results
The Random Forest Classifier outperformed other models with the following metrics:

Accuracy: ~85.93% (after K-Fold Cross Validation)

Precision: 0.919

Recall: 0.882

F1 Score: 0.900

Tech Stack
Language: Python
Libraries: pandas, numpy, scikit-learn, seaborn, matplotlib, imblearn.



# Credit Card Fraud Detection Project


This project focuses on detecting fraudulent credit card transactions using various machine learning techniques. The dataset used in this project is highly imbalanced, with a small percentage of transactions being fraudulent.
Table of Contents

    Dataset Information
    Data Preprocessing
    Model Training and Evaluation
    Results
    Conclusion
    Dependencies
    Usage

# Dataset Information

The dataset contains transactions made by credit cards in September 2013 by European cardholders. It presents transactions that occurred over two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly imbalanced, with the positive class (frauds) accounting for 0.172% of all transactions.

    Columns:
        Time: Number of seconds elapsed between this transaction and the first transaction in the dataset.
        V1 - V28: Result of a PCA transformation to protect user identities and sensitive features.
        Amount: Transaction amount.
        Class: Response variable (1 for fraudulent transactions, 0 otherwise).

# Data Preprocessing

    Null values: Check for any missing values.
    Data Standardization: Standardize the Amount and Time columns using StandardScaler.
    Class Distribution: Analyze the distribution of the target variable to understand the imbalance.

# Model Training and Evaluation

Several models were trained and evaluated for detecting fraudulent transactions:

    Logistic Regression
    Random Forest Classifier
    Support Vector Classifier
    Dummy Classifier: For baseline comparison.

# Results

    Dummy Classifier:
        Accuracy: 99.83%
        F1 Score: Imbalanced, reflecting high accuracy due to class imbalance.

    Random Forest Classifier:
        Accuracy: 99.93%
        Precision: 0.93 (fraud class)
        Recall: 0.65 (fraud class)
        F1 Score: 0.77 (fraud class)

    Logistic Regression:
        Accuracy: 99.91%
        Precision: 0.86 (fraud class)
        Recall: 0.61 (fraud class)
        F1 Score: 0.71 (fraud class)

    Support Vector Classifier:
        Accuracy: 99.92%
        Precision: 0.90 (fraud class)
        Recall: 0.67 (fraud class)
        F1 Score: 0.77 (fraud class)

# Conclusion

The Random Forest Classifier achieved the highest accuracy and F1 score among all models. However, due to the imbalanced nature of the dataset, precision and recall for the fraud class are more critical metrics. The models' performance can be further improved by techniques such as:

    Oversampling the minority class (fraudulent transactions).
    Using advanced anomaly detection techniques.
    Feature engineering to extract more relevant features.

# CreditGuard-Predicting-Financial-Distress
## Overview

The objective of this project is to develop a predictive model that estimates the probability that an individual will experience serious financial distress specifically, being 90 days or more past due on a debt within the next two years.

## Dataset Contains 

• SeriousDlqin2yrs : Person experienced 90 days past due delinquency or worse 

• RevolvingUtilizationOfUnsecuredLines : Total balance on credit cards and personal lines of credit except real estate and no installment debt like car loans divided by the sum of credit limits.

• age : Age of borrower in years

• NumberOfTime30-59DaysPastDueNotWorse : Number of times borrower has been 30-59 days past due but no worse in the last 2 years.

• DebtRatio : Monthly debt payments, alimony,living costs divided by monthy gross income

• MonthlyIncome : Monthly income

• NumberOfOpenCreditLinesAndLoans : Number of Open loans (installment like car loan or mortgage) and Lines of credit (e.g. credit cards)

• NumberOfTimes90DaysLate : Number of times borrower has been 90 days or more past due.

• NumberRealEstateLoansOrLines : Number of mortgage and real estate loans including home equity lines of credit

• NumberOfTime60-89DaysPastDueNotWorse : Number of times borrower has been 60-89 days past due but no worse in the last 2 years.

• NumberOfDependents : Number of dependents in family excluding themselves (spouse, children etc.)

# 1. Approach to Data Analysis and Feature Engineering
## Data Cleaning:

• Loaded training and testing datasets (cs-training.csv, cs-test-1.csv).

• Dropped the ID column as it is not predictive.

• Identified and handled missing values using median imputation.

## Feature Engineering:

• Standardized features using StandardScaler to improve model convergence.

• No manual feature creation was applied, focusing instead on robust preprocessing.

• Target Variable: SeriousDlqin2yrs
  Indicates whether a borrower experienced a serious delinquency (90+ days past due) in the following 2 years.

# 2. Modeling Techniques Used

## Implemented a Multi-Layer Perceptron (MLP) using PyTorch:

• One hidden layer with 32 neurons and ReLU activation.

• Final output layer with sigmoid activation for binary classification.

• Loss function: Binary Cross Entropy (BCELoss).

• Optimizer: Adam with learning rate 0.001.

• Data was split using stratified train-test split to preserve the class distribution.

# 3. Model Performance and Evaluation

## Metrics Evaluated on Validation Set:

• Accuracy:0.9362

• AUC-ROC:  0.8361

## Visualizations:

• Confusion Matrix: Provided to assess true positives and false positives.

• ROC Curve: Shows strong separation ability.

• Prediction Probability Histogram: Demonstrates model confidence distribution.

# 4. Key Insights and Business Implications
• The model successfully distinguishes between low-risk and high-risk borrowers, supporting early risk identification.

• With a high AUC-ROC, it is effective for ranking borrowers by likelihood of default, crucial for credit scoring.

• The neural network approach provides non-linear modeling capability, improving over simple linear models.

• Can be integrated into loan origination workflows to enable fair and responsible lending decisions.



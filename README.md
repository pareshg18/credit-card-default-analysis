--------------THIS ANALYSIS IS DONE IN R USING JUPYTER NOTEBOOK----------------

# Loan-default-analysis

This project is an analysis to identify customers who might default on their first payment. Through this project, I wanted to identify the important 
factors that indicate towards applicant defaulting.

# DATA
The data is from a company called Net Pay Advance, that lends small loans to customers. Here, each row indicates a loan application.
![data](https://user-images.githubusercontent.com/45079009/85041083-51ff5c80-b13e-11ea-8569-23faa6d643e4.PNG)

# Data Cleaning and Exploring

Mean distribution

![mean_dist](https://user-images.githubusercontent.com/45079009/85041476-d356ef00-b13e-11ea-9de5-fc775b19869c.PNG)

Correlation matrix

![corr-credit](https://user-images.githubusercontent.com/45079009/85041495-d8b43980-b13e-11ea-8233-0d0b937da81b.PNG)

# Models Tested
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Ada-boost

The models were evaluate using ROC curve, and initially the data was used as is (given imbalance class distribution). Later, SMOTE technique and up-sampling was used to balance the classes and the models were used again on the new data.

# Results

The Random Forest was chosen, its parameters hyper-tuned.

![rf_tuned](https://user-images.githubusercontent.com/45079009/85041941-727be680-b13f-11ea-8b71-de0c39a367cb.PNG)

Due to a very limited training set, and poor predictor variables, such low AUC was achieved. However, variables such as Monthly Net Income, Months lived at residence, Having a Bank Account for a long duration, time left for the due date and Loan amount very important
factors indicating default towars the first payment.

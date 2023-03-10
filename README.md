# Predicting-Customer-Churn-in-Telecom-Industry

Problem Statement:
With the rapid development of the telecommunication industry, service providers are inclined more toward expanding the subscriber base. Retaining existing customers has become a huge challenge to meet the need to survive in the competitive environment. It is stated that the cost of acquiring a new customer is far more than that of retaining the existing one. Therefore, it is imperative for the telecom industries to use advanced analytics to understand consumer behavior and predict the association of the customers as to whether or not they will leave the company.

Data Description
The data contains 11 variables and of which Churn is the Target variable. 
The complete data dictionary can be found here.

Columns	Description
  Churn: 1 if customer cancelled service, 0 if not
  AccountWeeks: 	number of weeks customer has had active account
  ContractRenewal:	1 if customer recently renewed contract, 0 if not
  DataPlan:	1 if customer has data plan, 0 if not
  DataUsage:	gigabytes of monthly data usage
  CustServCalls:	number of calls into customer service
  DayMins:	average daytime minutes per month
  DayCalls:	average number of daytime calls
  MonthlyCharge:	average monthly bill
  OverageFee:	largest overage fee in last 12 months
  RoamMins:	average number of roaming minutes
Kindly download the data from here.

Tasks
Hypothesis-based EDA:
Plot the distribution chart for the target variable. What is the class imbalance ratio?
Does having more customer service calls to increase the churn probability? 
If a customer uses more data, does that impact churn?
Preprocess and create new features:
Create a function to clip outliers between Q1 to Q3 range for all columns
Create bucketed features based on the variable distribution for CustServCalls, AccountWeeks variables
Create a function named “treat_null_values” that takes in the dataframe and does the following:
Drops features that have more than >= 60% null values
Impute columns based on median for numerical columns and mode for categorical variables
Build Logistic Regression and XGBoost algorithm using the prepared data.
Research on using hyperparameters to handle a class imbalance in Logistic Regression and XGBoost algorithm and build models using the same (Hint: class_weight & scale_pos_weight)
Use SMOTE to oversample & undersample data, then build the logistic and XGBoost model. Then compare the results from the above 2 steps 4 & 5.

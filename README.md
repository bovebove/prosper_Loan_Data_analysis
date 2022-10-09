#  Exploration of prosperLoan dataset

## by Awagoumm Ndjotsa Bienvenue


## Dataset
**The original dataset is in "prosperLoanData.rar"** ,  so you must uncompress it first before running the project
Structure of your dataset?
- First, I separate the original dataset in two part :  df1 which contains data from loans before July 2009 and df2 which contains data from loans after July 2009 
- At this spet, my dataset contains 76201 rows ;
- At this spet, I was interested in loans that are no longer current ('LoanStatus'='Current') and I obtained a dataset with 25031 rows

- For Features selection I select the variables we will work with in the following by removing the variables that are correlated to each other at more than 90% and less than 1%.
Then I have the following features :
- The Numerical Variables (11): 'Term', 'BorrowerAPR', 'EstimatedReturn', 'EmploymentStatusDuration', 'CreditScoreRangeLower', 'OpenRevolvingAccounts', 'OpenRevolvingMonthlyPayment', 'InquiriesLast6Months', 'TradesNeverDelinquentPercentage', 'DebtToIncomeRatio' , 'LoanOriginalAmount'.
- Categorical variables (10) : 'LoanStatus', 'ProsperRatingAlpha', 'ProsperScore', 'ListingCategoryNumeric', 'BorrowerState', 'Occupation', 'EmploymentStatus', 'IncomeRange', 'LoanOriginationQuarter'.
- Variables of type datetime (1) : 'FirstRecordedCreditLine


###  The main features I am interested in my dataset are 'LoanStatus', 'EstimatedLoss' and 'EstimatedReturn'.

###  I think the following features, after cleaning, will be useful for my analysis: 
- The Numerical Variables (11): 'Term', 'BorrowerAPR', 'EstimatedReturn', 'EmploymentStatusDuration', 'CreditScoreRangeLower', 'OpenRevolvingAccounts', 'OpenRevolvingMonthlyPayment', 'InquiriesLast6Months', 'TradesNeverDelinquentPercentage', 'DebtToIncomeRatio' , 'LoanOriginalAmount'.
- Categorical variables (10) : 'LoanStatus', 'ProsperRatingAlpha', 'ProsperScore', 'ListingCategoryNumeric', 'BorrowerState', 'Occupation', 'EmploymentStatus', 'IncomeRange', 'LoanOriginationQuarter'.
- Variables of type datetime (1) : 'FirstRecordedCreditLine


### For the rest of this work, we will use df2 which contains data from loans after July 2009 because it contains more data than df1 in terms of records and missing values;
### The same analyses can be reproduced on df1 within the limits of available data; 
### Also, we will study the loans that are no longer current to try to see the influence of variables on the final status of a loan

## Summary of Findings

> We have discovered new qualitative information; this information is presented in the two files attached to the analyses ; Some of them are :
Observations 1 :
23.2% of loans are completed;
Most loans are still in progress (67.62%);
Very few loans (1.2%) are in default;
Very few loans (2.4%) are in arrears between 1 and more than 120 days;
In the following we will study the LoanStatus according to the duration (Term)

Observations 2:
The distribution of loans according to risk is quasi-symmetrical with respect to the central value "C", it could be said that for 1 loan out of 2, the risk is average;
In the following, we will study the LoanStatus as a function of risk (ProsperRatingAlpha)

Observations 3:
The largest number of lenders belong to the middle class (annual salary between $50,000 and $74,999), followed by the lower middle class (annual salary between $24,999 and $50,000) and then the upper middle class (annual salary between $75,000 and $99,999)
In the following we will study the status of loans according to the annual income of the lender

Observations 5:
The semesters with more loans are semester 4 (30.1%), followed by semester 1 (26.9%) and semester 3 (23.8%), it would be interesting to see the impact of this variable on the status of a loan in a multivariate faceted visualization (we will do so in the following)

Observations 6:
There was an increase in the number of loans from 2009 to 2013 (from 2.3% to 41.3%);
There is a drop in the number of loans between 2013 and 204 (from 41.3% to 14.0%)
It would be interesting to understand this drop in a multivariate visualization by faceting (we will do so in the following)
In the following, we will study the relationships between LoanStatus by semester and by year

Observations 8:
- The state with the most lenders is California, it would be interesting to see if they repay their loans in a multivariate gaph
- 24.3% of the loans are given to people whose occupation is not yet listed, this calls for better work to list all the occupations
- Less than 5% of loans are given to people without a job, this should encourage lenders to get a job to increase their chances of receiving a loan

Observations 9 :
- Short-term loans (12 months) have the highest repayment rate
- Medium-term loans have a very high rate of late payment and default; they have the lowest rate of on-time repayment

- Those with incomes in the $1-24999 range have a very high default rate (over 60%)
- Those with incomes in the $25000-49999 range have a very high (highest) rate of late payment
- Those with incomes in the $500,000-74,999 range have a very high default rate (above 60%)
- Those with incomes over 75,000 have the best on-time repayment rates 

- The lower the risk, the higher the on-time repayment rates and the lower the default and delinquency rates, so the risk rating system is good




## Key Insights for Presentation

Observations 1:
The largest number of lenders belong to the middle class (annual salary between $50,000 and $74,999), followed by the lower middle class (annual salary between $24,999 and $50,000) and then the upper middle class (annual salary between $75,000 and $99,999)
In the following we will study the status of loans according to the annual income of the lender

Observations 2:
The semesters with more loans are semester 4 (30.1%), followed by semester 1 (26.9%) and semester 3 (23.8%), it would be interesting to see the impact of this variable on the status of a loan in a multivariate faceted visualization (we will do so in the following)

Observations 3:
- Less than 5% of loans are given to people without a job, this should encourage lenders to get a job to increase their chances of receiving a loan

Observations 3:
- 24.3% of the loans are given to people whose occupation is not yet listed, this calls for better work to list all the occupations


Observations 4 :
- Short-term loans (12 months) have the highest repayment rate
- Medium-term loans have a very high rate of late payment and default; they have the lowest rate of on-time repayment

Observations 5 :
- Those with incomes in the $1-24999 range have a very high default rate (over 60%)
- Those with incomes in the $25000-49999 range have a very high (highest) rate of late payment
- Those with incomes in the $500,000-74,999 range have a very high default rate (above 60%)
- Those with incomes over 75,000 have the best on-time repayment rates 

Observations 6 :
- The EstimatedReturn for the vast majority of loans is between 0.0 and 0.2

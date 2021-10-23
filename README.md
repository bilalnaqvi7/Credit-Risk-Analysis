# Credit-Risk-Analysis
We have performed data analysis and data visualisation on a subset of the Lending Club dataset and then created a logical regression model to  assess whether or not a new customer is likely to meet it's debt obligations(pay back the loan).

## Table of Contents
1. Introduction
2. Dataset
3. Exploratory Data Analysis
4. Credit Scoring – What , Why & How 
5.

## 1.Introduction
Credit analysis is a type of analysis an investor or bond portfolio manager performs on companies or other debt issuing entities to measure the entity's ability to meet its debt obligations. The credit analysis seeks to identify the appropriate level of default risk associated with investing in that particular entity.
One of the objectives of this notebook is to show step-by-step how to visualize the dataset and assess whether or not a new customer is likely to pay back the loan.

LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission, and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.

Given historical data on loans given out with information on whether or not the borrower defaulted (charge-off), we can build a model that can predict if a borrower will pay back their loan. This way in the future when we get a new potential customer, we can assess if they are likely to pay back the loan.

The following questions will be answered throughout the Kernel:

Which features are available in the dataset?
What is the distribution of numerical feature values across the samples?
What is the length of the dataframe?
What is the total count of missing values per column?
How many unique employment job titles are there?
Do you wonder how lending companies choose whether to give you money or not?
How does a lending company decide how much money to give you?
Would you offer this person a loan?
Did this person actually end up paying back their loan?

## 2.Dataset

We will be using a subset of the LendingClub DataSet obtained from Kaggle: https://www.kaggle.com/wordsforthewise/lending-club
There are many LendingClub data sets on Kaggle. Here is the information on this particular data set:

## 3.Exploratory Data Analysis

### Analyze by visualizing data
Get an understanding for which variables are important, view summary statistics, and visualize the data.

### Pearson correlation matrix
We use the Pearson correlation coefficient to examine the strength and direction of the linear relationship between two continuous variables.

The correlation coefficient can range in value from −1 to +1. The larger the absolute value of the coefficient, the stronger the relationship between the variables. For the Pearson correlation, an absolute value of 1 indicates a perfect linear relationship. A correlation close to 0 indicates no linear relationship between the variables.

The sign of the coefficient indicates the direction of the relationship. If both variables tend to increase or decrease together, the coefficient is positive, and the line that represents the correlation slopes upward. If one variable tends to increase as the other decreases, the coefficient is negative, and the line that represents the correlation slopes downward.

We can see a strong correlation between loan_amnt and installment. (The monthly payment owed by the borrower if the loan originates)

### Loan status and loan amount distribution
This is an imbalance problem, because we have a lot more entries of people that fully paid their loans then people that did not pay back.
We can expect to probably do very well in terms of accuracy but our precision and recall are going to be the true metrics that we will have to evaluate our model based off of.
In the loan amount distribution we can see spikes in even ten thousend dollar, so this is indicating that there are certain amounts that are basically standard loans.

### Relationship between loan_amnt, loan_status and installment
#### Countplot per grade and subgrade
Essentially this is showing the percentage of charged off loans.
Looks like it is increasing as the letter grade gets higher.
Better grades are bluer and the worse grades are redder.

## 4.Credit Scoring – What , Why & How 
### What : Methodology leveraged by Financial Institutions to determine the risk of non payment associated with loans 
### Why is it used?
Credit Scoring enables decision making at all customer lifecycle stages
Removes the need to manually examine each loan customer
Clear understanding of Denial or Approval reasons leading to sound business approach

### How is it used?
Credit Scores are used to determine the following areas under Loan portfolios

Approval – Should the Loan be approved?
Pricing – What is the right Interest ?
Cross Sell – Can we sell another loan ?
Refinance – Should there be a change in Interest?



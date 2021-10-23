# Credit-Risk-Analysis
We have performed data analysis and data visualisation on a subset of the Lending Club dataset and then created a logical regression model to  assess whether or not a new customer is likely to meet it's debt obligations(pay back the loan).

## Table of Contents
1. Introduction
2. Dataset
3. Exploratory Data Analysis
4. Data PreProcessing
5. Categorical Variables and Dummy Variables
6. Scaling and Train Test Split
7. Creating a Model
8. Training the Model
9. Evaluation on Test Data
10. Predicting on a New Customer

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

![8A4054E2-DE4A-45A4-B26F-4083C40FF649](https://user-images.githubusercontent.com/92293353/138538643-ef9fb9c3-dd8d-4a78-a6df-4f89c739cdf2.jpeg)

## 3.Exploratory Data Analysis

### Analyze by visualizing data
Get an understanding for which variables are important, view summary statistics, and visualize the data.

### Pearson correlation matrix
We use the Pearson correlation coefficient to examine the strength and direction of the linear relationship between two continuous variables.

The correlation coefficient can range in value from −1 to +1. The larger the absolute value of the coefficient, the stronger the relationship between the variables. For the Pearson correlation, an absolute value of 1 indicates a perfect linear relationship. A correlation close to 0 indicates no linear relationship between the variables.

The sign of the coefficient indicates the direction of the relationship. If both variables tend to increase or decrease together, the coefficient is positive, and the line that represents the correlation slopes upward. If one variable tends to increase as the other decreases, the coefficient is negative, and the line that represents the correlation slopes downward.

We can see a strong correlation between loan_amnt and installment. (The monthly payment owed by the borrower if the loan originates.)

### Loan status and loan amount distribution
This is an imbalance problem, because we have a lot more entries of people that fully paid their loans then people that did not pay back.
We can expect to probably do very well in terms of accuracy but our precision and recall are going to be the true metrics that we will have to evaluate our model based off of.
In the loan amount distribution we can see spikes in even ten thousend dollar, so this is indicating that there are certain amounts that are basically standard loans.

### Relationship between loan_amnt, loan_status and installment

#### Countplot per grade and subgrade
Essentially this is showing the percentage of charged off loans.
Looks like it is increasing as the letter grade gets higher.
Better grades are bluer and the worse grades are redder.

## 4.Logistic Regression Model
This is the main ML technique used which is directly based on 'regressional analysis' which data scientists use to evaluate the credit risk i.e. whether the customer will be able to payback the loan.

![B6FAD377-5711-4C24-8D32-9D9FFA71C9F5](https://user-images.githubusercontent.com/92293353/138539787-30266bbe-8d04-4abd-939b-39cd662b0e40.jpeg)

# Other contents are directly processed as code along with the text in the source code file(Credit-Risk-Analysis.ipynb)

## 5.Data Preprocessing

## 6. Categorical Variables and Dummy Variables

## 7. Scaling and Train Test Split

## 8. Creating a Model

## 9. Training the Model

## 10. Evaluation on Test Data

## 11. Predicting on a New Customer
Would you offer this person a loan?

![852476DE-D18C-4C73-8470-3EBB47347046](https://user-images.githubusercontent.com/92293353/138539844-d374cc8c-08ec-47ee-b7c3-89c571a9cc6c.jpeg)

Did this person actually end up paying back their loan?

![1997343E-9096-49AB-93C8-EB95F37DE7EE_4_5005_c](https://user-images.githubusercontent.com/92293353/138539851-c78c847a-0036-408e-b922-16b023868716.jpeg)

### NOTE - The '1.0' in the code cell is the final result which in this case is an 'affirmative' value indicating that the loan that was offered was paid back by the new customer.

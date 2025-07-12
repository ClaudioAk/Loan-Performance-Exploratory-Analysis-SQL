# Loan-Performance-Exploratory-Analysis-SQL

EasyLoan provides a variety of loan services, such as personal loans, car loans, and mortgages.

EasyLoan extends its services to clients in Canada, the United Kingdom, and the United States.

The analytics team is tasked with reporting performance across these geographic regions. Their goal is to pinpoint strengths and weaknesses for the business strategy team.

Your assistance is needed to ensure the data is both accessible and reliable before reporting begins.

Database Schema
<img width="836" height="390" alt="lending_schema" src="https://github.com/user-attachments/assets/bd0405f4-9414-4c18-b65a-74f62969dcc5" />
# Task 1 

The analytics team wants to use the `client` table to create a dashboard for client details. For them to proceed, they need to be sure the data is clean enough to use.

The `client` table below illustrates what the analytics team expects the data types and format to be.

Write an SQL query that returns the `client` table with the specified format, including identifying and cleaning all invalid values. 
-  Your output should be a DataFrame with the name 'client'. Do not modify the `client` table.
-  Note that the DataLab environment formats dates as YYYY-MM-DD-hh-ss-SSS. 

| Column Name       | Description                                                      |
|-------------------|------------------------------------------------------------------|
| client_id         | Unique integer (set by the database, can’t take any other value) |
| date\_of\_birth       | Date of birth of the client, as a date                           |
| employment_status        | Current employment status of the client, either employed or unemployed, as a lower case string                              |
| country          | The country where the client resides, either USA, UK or CA, as an upper case string                      |

# Task 2

You have been told that there was a problem in the backend system as some of the `repayment_channel` values are missing. 

The missing values are critical to the analysis so they need to be filled in before proceeding.

Luckily, they have discovered a pattern in the missing values:

- Repayment higher than 4000 dollars should be made via `bank account`.
- Repayment lower than 1000 dollars should be made via `mail`.

Write an SQL query that makes the `repayment` table match these criteria.
-  Your output should be a DataFrame with the name 'repayment'. Do not modify the original `repayment` table.

-  # Task 3

Starting on January 1st, 2022, all US clients started to use an online system to sign contracts.

The analytics team wants to analyze the loans for US clients who used the new online system.

Write a query that returns the data for the analytics team. Your output should include `client_id`,`contract_date`, `principal_amount` and `loan_type` columns.


# Task 4

The business strategy team is considering offering a more competitive rate to the US market. 

The analytic team want to compare the average interest rates offered by the company for the same loan type in different countries to determine if there are significant differences.

Write a query that returns the data for the analytics team. Your output should include `loan_type`, `country` and `avg_rate` columns.

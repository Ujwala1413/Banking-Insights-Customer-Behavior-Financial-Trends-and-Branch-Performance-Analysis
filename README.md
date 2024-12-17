# PROJECT TITLE: 
## Banking Insights :Customer-Behavior-Financial-Trends-and-Branch-Performance-Analysis
This project analyzes customer behavior, financial trends, and branch performance using transaction data. Key insights include branch-specific performance, account preferences, loan patterns, and actionable strategies to enhance customer satisfaction and profitability.
![image](https://github.com/user-attachments/assets/6d197bea-ff8e-4742-88d4-2f617f2f35b8)

# PROJECT OVERVIEW:
## **Objective**
The objective of this project is to identify potential customers for cross-selling financial products, such as loans, credit cards, and savings accounts, by analyzing their financial behavior, account details, and transaction history. This will help the bank offer suitable products to customers, improve sales, and enhance customer satisfaction.

## **Data Source**
The data for this project was sourced from 7 different CSV files, which were later converted into SQL dump files for analysis. The files include:
1. Accounts
2. Branches
3. Customers
4. KYC
5. Loans
6. Payments
7. Transactions

## **Tools used**
1. Programming Language: Python
2. Development Environment: Jupyter Notebook, MySQL Workbench
## **Libraries used**
1. Data Manipulation: NumPy, Pandas
2. Data Visualization: Matplotlib
3. Database Connectivity: MySQL-Connector-Python, PyODBC, SQLite3

# DATA UNDERSTANDING:
## **Data Description**
The dataset consists of multiple files containing detailed information about the bank's operations and customers. The key data files include:
1. Accounts: Contains information about customer accounts, including account_id, customer_id, branch_id, account type, and balance [No. of Records: 1054]
2. Branches: Includes data about bank branches, such as branch IDs, locations, and branch name. [No. of Records: 10]
3. Customers: Contains customer demographic information, such as customer_id, first_name, last_name, email, phone, and address. [No. of Records: 1134]
4. KYC: Stores Know Your Customer (KYC) details for each customer, including kyc_id, customer_id, adhar_number, and kyc_status. [No. of Records: 500]
5. Loans: Provides information on the types of loans customers have, such as loan_id, customer_id, loan amounts, interest rates, and loan status (active or closed). [No. of Records: 564]
6. Payments: Tracks payment transactions made by customers, including payment_id, loan_id, and payment amounts. [No. of Records: 2000]
7. Transactions: Includes transaction details such as transaction ID, amount, and type (debit/credit). [No. of Records: 2061]

## **Data Quality Issues**
### 1. Accounts: 
Null Values: 33,
Duplicate values: 43,
Incorrect datatype: 3 (account_id, customer_id, branch_id)
### 2. Branches:
No inconsistencies in the data, 
Data types are also correct.
### 3. Customers:
Null Values: 50, 
Duplicates values: 119, 
Incorrect datatypes: 1 (customer_id), 
Unnecessary column: 1 (Phone), 
### 4. KYC:
Null values: 0, 
Duplicate values: 0, 
Incorrect datatype: Nill, 
Unnecessary column: 1 (Adhar_number)
### 5. Loans:
Null Values: 48, 
Duplicate values: 49, 
Incorrect datatypes: 2 (loan_id, customer_id)
### 6. Payments: 
No inconsistencies in the data, 
Data types are also correct.
### 7. Transactions:
Null values: 0, 
Duplicate values: 61
Incorrect datatype: Nill

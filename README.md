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

## **Exploratory Data Analysis (EDA)**
### Summary Statistics:
1. Calculated measures like mean, median, mode, standard deviation for numerical columns to understand central tendency and variability.

2. Used info() to check column data types, non-null values, and memory usage.

3. Explored the first few rows with head() and the last few rows with tail() to get a quick snapshot of the data.

4. Verified dataset size using shape to identify the number of rows and columns.

### Descriptive Analysis:
1. describe() function was applied to get a summary of numerical columns, including count, mean, standard deviation, min, and max values.

### Missing Value Analysis:
1. Checked for missing or null values using isnull().sum() to identify potential data cleaning requirements.
Data Types Validation:

2. Validated and converted column data types where necessary for compatibility using functions like astype().

### Distribution Analysis:
1. Plotted histograms and boxplots using Matplotlib to visualize the distribution and detect outliers in numerical data.

### Category Analysis:
1. Performed frequency counts using value_counts() for categorical variables to understand distribution patterns.
Data Integrity Checks:

2. Verified the uniqueness of IDs (e.g., customer ID, transaction ID) to ensure no duplicates exist where they shouldn’t.

## **Data Visualization:**
### 1. Column Charts:
a) Customer Distribution Across Branches: To identify branches with the highest and lowest customer counts.

b) Highest & Lowest Balance Analysis per Branch of the Customer: To compare the financial performance of different branches.

c) Current and Savings Account per Branch: To visualize the distribution of account types across branches.

d) Number of Customers Having Active Loan Status: To highlight the number of active loan holders.

e) Total Balance of All Accounts per Branch: To assess the overall financial standing of branches.

f) Balances Across Different Account Types per Branch: To analyze balance patterns by account type.

g) Total Number of Transactions Processed per Branch: To evaluate branch activity based on transaction volume.

h) Distribution of Transaction Types per Branch (Count): To identify transaction trends across branches.

### 2. Line Charts:
a) Analyzing the Difference Between Highest and Lowest Balance in Each Branch: To observe trends in financial disparities between branches over time.

### 3. Pie Charts:
a) KYC Status of Customers: To illustrate the proportion of verified, pending, and under-review KYC statuses.

b) Type of Loans Customers Are Preferring Most: To showcase the popularity of loan types (e.g., home, personal, auto).

c) Loan Status of Customers: To display the distribution of active and closed loans among customers.

## **Data Preparation**
### Data Cleaning:
The data cleaning process was performed to ensure accuracy and relevance for analysis. Key steps included:

1. Handling Missing and Duplicate Values: Null values were dropped, and duplicate records were removed to maintain data integrity.

2. Dropping Unnecessary Columns:

a) Phone Number: Excluded as it was not required for analysis.

b) Address: Removed due to inconsistencies, with some entries containing incomplete or irrelevant information (e.g., only numbers, plot numbers, or city names).

c) Aadhar Number: Omitted as it had no analytical relevance.

3. Data Type Conversion: Adjusted data types where necessary to ensure compatibility and accurate computation for example: float to int.
### Data Integration:
To establish relationships and combine relevant data across multiple tables, the merge function was utilized effectively. The following relationships were created:

1. Accounts & Branch: To link account details with their respective branches.

2. Customers & KYC: To associate customer records with their KYC verification status.

3. Accounts & Customers: To connect account details to the corresponding customer profiles.

4. Customers & Loans: To relate customers to their loan details.

5. Loans & Payments: To map loan records with payment transactions.

6. Accounts & Transactions: To integrate account details with transaction history.

# RESULTS AND FINDINGS:
### i) Customer Distribution Across Branches
![image](https://github.com/user-attachments/assets/e2314f73-bb07-477e-844f-67be8cc63bb4)





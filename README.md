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
![image](https://github.com/user-attachments/assets/1db042eb-6aa0-483f-88e3-5b1a03dbffcd)
Branch N12n & O11r has most customer count showing more satisfaction as compared to M20i.

### ii) Highest & Lowest Balance analysis per Branch of the customer
![image](https://github.com/user-attachments/assets/329f3640-8968-4f53-b638-01f2daf9840d)
Branch "Y15a" has the most money, while "B16a" has the least.

### iii) Customer with highest & lowest balance in each branch
![image](https://github.com/user-attachments/assets/39aa3bc5-2fca-48a4-83de-0f071ecf79fe)
The data reveals that Branch 5 has the highest customer balance, while Branch 2 has the lowest.

### iv) Current and Savings Account Per Branch
Branch 10 has the highest number of current accounts, while Branch 3 has the highest number of savings accounts. 

### v) Analysing difference between Highest and Lowest Balance in each Branch
There's a significant difference between the highest and lowest balances across branches. 
This suggests that some branches are performing better than others in terms of customer spending and account balances.

### vi) Well Performing Branches
Branches N12n, O11r, and V18a are consistently among the top performers in terms of customer base, account numbers, and maximum balance. This indicates their strong performance across key metrics.

### vii) KYC Status of Customers
There are still bottlenecks in the "Pending" with 32.4% and "Under Review" with 31.4% stages.

### viii) Type of Loans customers are perferring most
Customers are mostly preffering Home loan followed by personal loan.

### ix) Highest & Lowest Interest Rate as per loan type
![image](https://github.com/user-attachments/assets/2c59ee27-5299-4bd9-82db-f4ad99dff5b8)

### x) Loan status of customers
![image](https://github.com/user-attachments/assets/7a710a14-3b57-439d-ae81-3ea04f503d95)

### xi) Highest and Lowest interest rate for active and closed loan.
![image](https://github.com/user-attachments/assets/6eadc03a-fa13-41fb-99a7-7d42f43a8ba0)

### xii) Number of Customers having Active loan status
Most people have active home loans, followed by personal loans and then auto loans.

### xiii) Customers having more than 1 loan currently
The number of customer having more than 1 loan is:  66

### xiv) Maximum & Minimum Loan Amount
Maximum Loan Amount:  499987.64
Minimum Loan Amount:  12196.68

### xv) Total Balance of all accounts per branch
Branches with the most money i.e B16a, O11r, V18a and Y15a are doing well.
Branches with less money i.e M20i and R17i.

### xvi) Balances across different account types per branch
R13n branch having the highest savings account as well as least current accounts as well, whereas N12n has highest current accounts and R17i has least savings account.

### xvii) Total no. of transactions processed per branch
Branch 2 is the busiest, while Branch 10 is the least busy.

### xviii) Distribution of transaction types per branch (count)
![image](https://github.com/user-attachments/assets/73ad0cc3-9d7f-45f7-b20a-2165c9df1e3d)






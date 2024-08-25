# **Bank Loan Performance Analysis :**
![image](https://github.com/user-attachments/assets/cced70ed-0807-4d30-bc8d-80c7f6755a74)
## Introduction:
&nbsp;&nbsp;&nbsp;&nbsp;I was assigned to a dataset of Banking domain which is large in size and that got me into the workplace of PowerBi straight away. And here I am showcasing the overview of what i have done with it.
[_Click here to download my Project (.pbix file)_](https://drive.google.com/file/d/1J0-SUvff1F_4yOtcZRDWlvQQBYuamO0y/view?usp=sharing)
### Skills Demonstrated:
* **Transformation**: Dealing with missing values and inconsistancies, Formatting to the right type, getting the data familiar
* **DAX**: Calculated Columns, Measures, Calculated Tables
* **Modeling**: Star Schema
* **Report Making**: Visuals, Slicers, Bookmarks
## Problem Statement:
&nbsp;&nbsp;&nbsp;&nbsp;Given the data, here are the problems to consider

* Load the Dataset
* Transform it, make it cleansed
* Make a Relationship and create Measures and Columns
* Create Report for these on your own custom:
  * Loan Performance Analysis
  * Borrower Profile Analysis
  * Summary Page
## Data Sourcing:
**DataSet**: [_Bank Loan (.xlsx)_](https://drive.google.com/uc?export=download&id=1yNL9gfv-DlD3cEW9o2GJvtJ9Bzbm37R7)<br>
&nbsp;&nbsp;&nbsp;&nbsp;The Excel file contained 22 columns and 466,286 rows of total (60mb). It contained Loan Details and Borrower Details.
![Screenshot (134)](https://github.com/user-attachments/assets/cec01280-c6ef-4530-8181-4bc1d1481425)
![Screenshot (135)](https://github.com/user-attachments/assets/70d6a79c-bafa-4fe8-84a6-3109f6c8175d)
## Data Transformation/Cleaning:
&nbsp;&nbsp;&nbsp;&nbsp;The data is first explored for all kind of inconsistancies and cleansed properly, those include
* **Creating custom columns** BorrowerDetails[total_amount_paid], BorrowerDetails[delinquency_status]
* **Removing the columns** that is not necessary for analysis _**eg**. LoanDetials[subgrade]_
* **Replacing** Numeric values with understandable replacements _**eg**. replacing -9,-99 with 'Unknown'_
* **Dealing with inconsistancies** texture incosistancies _**eg**. LoanDetails[purpose]_
* **Appropriating Data Types** on columns of Date, Binary, Currency  _**eg**. BorrowerDetials[total_pymnt]_
* **Removing Duplicates** duplicates found in LoanDetails[id]
## Data Analysis Expression & Data Heirarchies:
* **Calculated Columns**:
  * _'remaining_installments'_ which Out Principal by Installment
* **Measures**:
  * _'Fully Paid Loan Percentage'_: Percentage of Loan which is paid and closed
  * _'Non-Verified Borrowers Count'_: Count of borrowers who is not yet verified
## Data Modeling:
&nbsp;&nbsp;&nbsp;&nbsp; Nothing complex with modeling here, its just 2 queries and there exist a many-to-one relationship with the common column names _'loan_id'_.
![image](https://github.com/user-attachments/assets/001f33da-6791-4aff-ac0e-2f418d41b795)
## Data Analysis and Visuals:
### Report 1: Loan Performance Analysis
![image](https://github.com/user-attachments/assets/76784711-4c70-431e-807d-7b55a3ec91cd)

### Report 2: Borrower Profile Analysis
![image](https://github.com/user-attachments/assets/ac1e7b58-2094-419b-bb01-355a1f0292d4)

### Summary Page: 
![image](https://github.com/user-attachments/assets/3acfa8fd-236c-4055-ae9c-e087d6aaed17)

## Conclusion:
&nbsp;&nbsp;&nbsp;&nbsp;Its clear as the visuals shows the Borrower Profile and Loan Performance Analysis outcomes

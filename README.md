Data Source: https://drive.google.com/uc?export=download&id=1yNL9gfv-DlD3cEW9o2GJvtJ9Bzbm37R7 <br/>
PBIX file : 
# **Bank Loan Performance Analysis :**
![unnamed](https://github.com/user-attachments/assets/3807189e-beaa-481e-833e-1e9bf34c4199)
## Introduction:
&nbsp;&nbsp;&nbsp;&nbsp;I was assigned to a dataset of Banking domain which is large in size and that got me into the workplace of PowerBi straight away. And here I am showcasing the overview of what i have done with it.
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
**DataSet**: [_Global Terrorism_](https://drive.google.com/file/d/1J0-SUvff1F_4yOtcZRDWlvQQBYuamO0y/view?usp=sharing)<br>
&nbsp;&nbsp;&nbsp;&nbsp;The Excel file contained 22 columns and 466,286 rows of total (60mb). It contained Loan Details and Borrower Details.
![Screenshot (134)](https://github.com/user-attachments/assets/cec01280-c6ef-4530-8181-4bc1d1481425)
![Screenshot (135)](https://github.com/user-attachments/assets/70d6a79c-bafa-4fe8-84a6-3109f6c8175d)
## Data Transformation/Cleaning:
&nbsp;&nbsp;&nbsp;&nbsp;The data is first splitted for the sake of snowflake schema and to make it scalable, then further transformation took place including
* Making the **column multiples into single column** on gangs, weapons, attacktypes and also its sub-categories
* **Removing the columns** that is not necessary for analysis _**eg**. written notes, explaing the events_
* **Replacing** Numeric values with understandable replacements _**eg**. replacing -9,-99 with 'Unknown'_
* **Making Bridge tables** for colums with multiple entries _**eg**. multiple weapon types can be used in one event_
* **Appropriating Data Types** on columns of Date, Binary, Currency
* **Appending and Removing Duplicates** which happens while spliting the data
## Data Analysis Expression & Data Heirarchies:
* **Calculated Columns**:
  * _'NoOf days to Execute'_ which is the date difference between _'Resolution Date'(if available)_ and _'Date of Event'_
  * _'Gang Label'_ to know the gang is recogniced or Unknown
  * _'NoOf SubGangs'_ each gang has
* **Measures**:
  * _'Success Rate of Attack Type'_: Percentage of Success of each type of Attack
  * _'International Support %'_: Percentage of International Support gained
* **Calculated Tables:**
  * _"Gang Summary"_: Details of each gang including their, success and failures, kills and wounds, kidnapping and ransom, etc
* **Data Hierarchies**:
  * Date Hierarchy: which is made automatic in nature for _'Event Date', 'Resolution Date'_
  * Gang Hierarchy: _'Gang Name', 'Gang SubName'_
  * Target Hierarchy: _'Target', 'Target Subtype'_
  * Weapon Hierarchy: _'Weapon Type', 'Weapon Subtype'_
  * Location Hierarchy: _'country', 'region', 'prov_state', 'city'_
## Data Modeling:
&nbsp;&nbsp;&nbsp;&nbsp;Since I prepared everything for SnowFlake Schema, I made relationship with fact table to all related queries with _'eventid'_. Its finally 21 queries, and here how it looks like
![Screenshot (125)](https://github.com/user-attachments/assets/9ef129b2-bf24-4364-b1df-c78664d43f55)
## Data Analysis and Visuals:
![Screenshot (122)](https://github.com/user-attachments/assets/53893094-8737-4e78-8151-15afcd69bbe2)
![Screenshot (124)](https://github.com/user-attachments/assets/21084f23-790f-4420-ac5a-25f6b6ce8972)
![Screenshot (127)](https://github.com/user-attachments/assets/5df7afcc-ed99-467a-b108-143b26edffa4)

## Conclusion:
&nbsp;&nbsp;&nbsp;&nbsp;Its clear as the visuals shows the terrorisms and its features

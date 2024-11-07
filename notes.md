1- Number of columns: 32 Number of rows: 346018
---
2- Classification Codes and Normalized UNSPSC was matched
---
3- Columns with no missing values: ['_id', 'Creation Date', 'Fiscal Year', 'Purchase Order Number', 'Acquisition Type', 'Acquisition Method', 'Department Name', 'CalCard']
---
# Missing Values Report
## Columns with more than 50% missing values
| Column Name | Missing Count | Data Type |
|-------------|---------------|-----------|
| LPA Number | 253673 | object |
| Requisition Number | 331649 | object |
| Sub-Acquisition Type | 277681 | object |
| Sub-Acquisition Method | 315122 | object |
| Supplier Qualifications | 204273 | object |
---
# Missing Values Report
## Columns with more than 25% missing values
| Column Name | Missing Count | Data Type |
|-------------|---------------|-----------|
| LPA Number | 253673 | object |
| Requisition Number | 331649 | object |
| Sub-Acquisition Type | 277681 | object |
| Sub-Acquisition Method | 315122 | object |
| Supplier Qualifications | 204273 | object |
---
4- So from the above 2 reports (50% and 25%) we can see that the same 5 columns that take the very percentage of missing values.
---

- Column: LPA Number - Missing Values Percentage: 73.31%
- Column: Requisition Number - Missing Values Percentage: 95.85%
- Column: Sub-Acquisition Type - Missing Values Percentage: 80.25%
- Column: Sub-Acquisition Method - Missing Values Percentage: 91.07%
- Column: Supplier Qualifications - Missing Values Percentage: 59.04%
---


5- I have 30 rows with missing price values, after investigation I can't find pattern that help me to fill those missing values, like family or products with same classification codes 
also i think it's hard to fill them as unique creation and purchasing dates and Supplier name all those reflect on pricing
---
6- What I will try to do now is fill the missing values in the Purchase Date using the Creation Date and Fiscal Year.

- . **Show the Fiscal Year that contains the most missing Purchase Dates.**
- . **Show the department name that contains the most missing Purchase Dates, as data entry will be the same for every department.**
- . **Try to extract a pattern from here.**
Missing Values in Fiscal Year: Fiscal Year
2012-2013    6332
2013-2014    6549
2014-2015    4555
Name: Purchase Date, dtype: int64
- No Exact Pattern In Fiscal Year, Will Add More Grouping Based on Department Name
**Very Well, We Found A Pattern In Department Name**

There is a relationship between Department Name and Purchase Date.
**As Shown In The Figure**
![2012-2013.png](saved_plots\2012-2013.png)

![2013-2014.png](saved_plots\2013-2014.png)

![2014-2015.png](saved_plots\2014-2015.png)

I can see that the Department Name with the largest number of missing Purchase Dates is Consumer Affairs.
So we will fill the Purchase Date with the mean of the period each department takes to fill the Purchase Date. It's the difference in days between the Creation Date and the Purchase Date.
---



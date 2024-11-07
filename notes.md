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


7- Number of Missing Values in CalCard: 0 With Unique Values: ['NO' 'YES']
Value Conuts: CalCard
NO     340646
YES      5372
Name: count, dtype: int64, that show there is no balance in CalCard Most of purchase is without credit card
![CalCard.png](saved_plots\CalCard.png)

Can't Find any pattern or reason about why littile number of operaions is using CelCard, so we will keep it as it is

---

![Class Title.png](saved_plots\Class Title.png)
--- 
8- **Number Of Oberations In June Is High, In Every Fiscal Year**

![Number Of Oberations In June Is High, In Every Fiscal Year.png](saved_plots\Number Of Oberations In June Is High, In Every Fiscal Year.png)
---

9- **Top Class and Family Titles by Fiscal Year**

- **2012-2013**
  - **Top Class Title**: Printer and facsimile and photocopier supplies
  - **Top Family Title**: Office machines and their supplies and accessories

- **2013-2014**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels

- **2014-2015**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels

---

**10- Total Spending By Fiscal Year**

- **2012-2013**
  - **Top Class Title**: Printer and facsimile and photocopier supplies
  - **Top Family Title**: Office machines and their supplies and accessories
  - **Total Spending**: $62,054,189,182.06

- **2013-2014**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels
  - **Total Spending**: $42,543,169,213.68

- **2014-2015**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels
  - **Total Spending**: $46,989,774,165.58
![TopSpending.png](saved_plots\TopSpending.png)

---

**11- Top Supplier by Number of Operation By Fiscal Year**

- **2012-2013**
  - **Top Supplier**: 1249060.0

- **2013-2014**
  - **Top Supplier**: 1743406.0

- **2014-2015**
  - **Top Supplier**: 1743406.0


---

**12- Top Supplier and Total Spending By Fiscal Year**

- **2012-2013**
  - **Top Supplier**: 1087520.0 
  - **Total Spending**: 11160129000.04

- **2013-2014**
  - **Top Supplier**: 1029823.0
  - **Total Spending**: 1029823.0

- **2014-2015**
  - **Top Supplier**: 1743406.0
  - **Total Spending**: $3509792000.0

---

**Why The number of operations always high in june in every fiscal year?**<br>
**13- Top Class and Family Titles by Fiscal Year**

- **2012-2013**
  - **Top Class Title**: Printer and facsimile and photocopier supplies
  - **Top Family Title**: Office machines and their supplies and accessories

- **2013-2014**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels

- **2014-2015**
  - **Top Class Title**: Petroleum and distillates
  - **Top Family Title**: Fuels

After Searching it's not according to Family or Class, it's according to it is end of Fiscal Year So many of states expand hish in june in every Fiscal Year
The government of California tends to spend more in June than in any other month for several reasons related to budget management and the fiscal year:

1. **End of the Fiscal Year**: June marks the end of the fiscal year in California, which concludes on June 30th. During this month, government agencies aim to ensure that they have fully utilized their allocated budget to avoid reductions in the next fiscal year.

2. **Settling Accounts**: Agencies need to settle their accounts and ensure that all bills and dues are paid before the fiscal year ends. This leads to increased spending during this month.

3. **Reallocation of Funds**: Sometimes, there are unused funds in the budget that need to be reallocated or spent before the fiscal year ends to avoid losing them.

4. **Preparation for the New Fiscal Year**: Preparing for the new fiscal year may require additional spending at the end of the current year to ensure a smooth transition between fiscal years.

These combined factors lead to increased government spending in June compared to other months of the year.


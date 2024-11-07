# 1- Depending on the high percentage of missing valuesin those columns we can decide to drop those columns
| Column Name | Missing Count | Data Type |
|-------------|---------------|-----------|
| LPA Number | 253673 | object |
| Requisition Number | 331649 | object |
| Sub-Acquisition Type | 277681 | object |
| Sub-Acquisition Method | 315122 | object |
| Supplier Qualifications | 204273 | object |
---
# 2- Will remove Normalized UNSPSC as it same value Classification Codes
---
# 3- I will remove the rows containg missing price values
---
# 4- I will fill the missing values in the Purchase Date with the mean of the period each department takes to fill the Purchase Date, it is the difference in days between the Creation Date and the Purchase Date.
---
# 5- I will keep CalCard as it is. just add One-Hot-Encoding to it.
---


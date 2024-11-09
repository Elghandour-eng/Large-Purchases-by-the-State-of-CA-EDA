# Data Cleaning and Transformation Steps

1. **Drop Columns with High Percentage of Missing Values**  
   Depending on the high percentage of missing values in these columns, we can decide to drop them:

   | Column Name             | Missing Count | Data Type |
   |-------------------------|---------------|-----------|
   | LPA Number              | 253,673       | object    |
   | Requisition Number      | 331,649       | object    |
   | Sub-Acquisition Type    | 277,681       | object    |
   | Sub-Acquisition Method  | 315,122       | object    |
   | Supplier Qualifications | 204,273       | object    |

---

2. **Remove Normalized UNSPSC**  
   Will remove Normalized UNSPSC as it has the same value as Classification Codes.

---

3. **Remove Rows with Missing Price Values**  
   I will remove the rows containing missing price values.

---

4. **Fill Missing Purchase Dates**  
   I will fill the missing values in the Purchase Date with the mean of the period each department takes to fill the Purchase Date. It is the difference in days between the Creation Date and the Purchase Date.

---

5. **Keep CalCard and Apply One-Hot-Encoding**  
   I will keep CalCard as it is and just add One-Hot-Encoding to it.

---

6. **Remove Requisition Number**  
   I will remove the column Requisition Number as it duplicates with Purchase Order Number.

---

7. **Remove Duplicated Rows**  
   I will remove the duplicated rows, which are counted as 2,084.

---

8. **Split Location String**  
   I will split the Location string into 3 columns: Zip Code, Latitude, and Longitude.

---

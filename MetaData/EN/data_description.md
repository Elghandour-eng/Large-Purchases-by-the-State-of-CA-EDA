`This dataset provides detailed information on purchase orders, including dates, fiscal years, supplier details, item descriptions, and classification codes, to facilitate procurement analysis and reporting.`


1. **Creation Date:**
   - **Description:** System Date.

2. **Purchase Date:**
   - **Description:** Date of purchase order entered by the user. This date can be backdated; therefore, the creation date is primarily used.

3. **Fiscal Year:**
   - **Description:** Fiscal year derived based on creation date. State of California fiscal year starts on July 1 and ends on June 30.

4. **LPA Number:**
   - **Description:** Leveraged Procurement Agreement (LPA) Number, aka Contract Number. If there is a contract number in this field, the amount is considered contract dollars.

5. **Purchase Order Number:**
   - **Description:** Unique number for each purchase order. Different departments can have the same purchase order number.

6. **Requisition Number:**
   - **Description:** Unique number for each requisition. Different departments can have the same requisition number.

7. **Acquisition Type:**
   - **Description:** Type of acquisition (e.g., Non-IT Goods, Non-IT Services, IT Goods, IT Services).

8. **Sub-Acquisition Type:**
   - **Description:** Depends on the acquisition type used. Please see data dictionary for additional information.

9. **Acquisition Method:**
   - **Description:** Type of acquisition used to make purchase. Please see data dictionary and supplemental acquisition method document for further information.

10. **Sub-Acquisition Method:**
    - **Description:** Depends on the acquisition method used. Please see data dictionary for additional information.

11. **Department Name:**
    - **Description:** Name of purchasing department. Normalized field.

12. **Supplier Code:**
    - **Description:** Supplier code. Normalized field.

13. **Supplier Name:**
    - **Description:** Name of the supplier.

14. **Supplier Qualifications:**
    - **Description:** Identifies supplier qualifications as a certified small business (SB), small business enterprise (SBE), disabled veteran business enterprise (DVBE), non-profits (NP), and micro-business (MB).

15. **Supplier Zip Code:**
    - **Description:** Supplier Zip Code.

16. **CalCard:**
    - **Description:** State credit card used for purchase? Yes/No.

17. **Item Name:**
    - **Description:** Name of items being purchased.

18. **Item Description:**
    - **Description:** Description of items being purchased.

19. **Quantity:**
    - **Description:** Quantity of items being purchased.

20. **Unit Price:**
    - **Description:** Unit price of items.

21. **Total Price:**
    - **Description:** Total price of items. This does not include taxes or shipping.

22. **Classification Codes:**
    - **Description:** United Nations Standard Products and Services Code® (UNSPSC) v. 14 of items purchased.

23. **Normalized UNSPSC:**
    - **Description:** Normalized UNSPSC number. The first 8 digits of the classification code identify the entire purchase order.

24. **Commodity Title:**
    - **Description:** Correlated commodity title based on the 8-digit normalized UNSPSC.

25. **Class:**
    - **Description:** Correlated class number based on the 8-digit normalized UNSPSC.

26. **Class Title:**
    - **Description:** Correlated class title based on the 8-digit normalized UNSPSC.

27. **Family:**
    - **Description:** Correlated family number based on the 8-digit normalized UNSPSC.

28. **Family Title:**
    - **Description:** Correlated family title based on the 8-digit normalized UNSPSC.

29. **Segment:**
    - **Description:** Correlated segment number based on the 8-digit normalized UNSPSC.

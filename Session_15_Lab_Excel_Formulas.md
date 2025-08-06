# Session 15: Excel for Analysis (Formulas & Functions)

**Unit 2: Data Tools and Platforms**
**Hour: 15**
**Mode: Practical Lab**

---

### 1. Objective

This lab provides hands-on practice with the most fundamental building blocks of Excel analysis: formulas and functions. By the end of this session, you will be able to use common functions to perform calculations and make logical decisions on a dataset.

**This is a guided lab. The instructor will demonstrate these steps in Excel, and students will follow along.**

---

### 2. The Dataset

We will use a simple sales report dataset. Create a new Excel sheet named `Sales Data` and enter the following data:

| OrderID | Product | Category | Units Sold | Unit Price |
| :--- | :--- | :--- | :--- | :--- |
| 101 | Apples | Fruit | 50 | $1.20 |
| 102 | Bread | Bakery | 30 | $3.50 |
| 103 | Milk | Dairy | 25 | $4.00 |
| 104 | Oranges | Fruit | 40 | $1.50 |
| 105 | Cheese | Dairy | 20 | $5.00 |
| 106 | Croissant | Bakery | 35 | $2.50 |

---

### 3. Lab Activities

#### Activity 1: Calculating a New Column (Total Sales)

1.  In cell **F1**, type the header `Total Sales`.
2.  In cell **F2**, we want to calculate the total sales for the first order (Apples). The formula is `Units Sold * Unit Price`.
3.  Type the following formula in cell **F2**: `=D2*E2` and press Enter. The cell should display `60`.
4.  **Auto-fill the formula:** Click on cell **F2**. You'll see a small square handle at the bottom-right corner. Double-click this handle. Excel will automatically apply the formula down to the rest of the rows.

Your sheet should now look like this:

| Total Sales |
| :--- |
| 60 |
| 105 |
| 100 |
| 60 |
| 100 |
| 87.5 |

#### Activity 2: Using Basic Statistical Functions

Now, let's calculate some summary statistics for our sales.

1.  Go to cell **A8** and type `Total Revenue`.
2.  In cell **B8**, use the `SUM` function to add up all the values in the `Total Sales` column. Type: `=SUM(F2:F6)` and press Enter. (Result should be `512.5`).
3.  In cell **A9**, type `Average Sale`.
4.  In cell **B9**, use the `AVERAGE` function. Type: `=AVERAGE(F2:F6)` and press Enter. (Result should be `92.08...`).
5.  In cell **A10**, type `Highest Sale`. In cell **B10**, use the `MAX` function: `=MAX(F2:F6)`.
6.  In cell **A11**, type `Lowest Sale`. In cell **B11**, use the `MIN` function: `=MIN(F2:F6)`.
7.  In cell **A12**, type `Number of Orders`. In cell **B12**, use the `COUNT` function: `=COUNT(A2:A6)`.

#### Activity 3: Using a Logical Function (`IF`)

Let's create a new column to label each order as "Large Order" if its `Total Sales` are greater than $90, and "Small Order" otherwise.

1.  In cell **G1**, type the header `Order Size`.
2.  The `IF` function has three parts: `IF(logical_test, value_if_true, value_if_false)`.
3.  In cell **G2**, type the following formula: `=IF(F2>90, "Large Order", "Small Order")` and press Enter.
4.  The result for the first row should be "Small Order" since 60 is not greater than 90.
5.  Use the auto-fill handle on cell **G2** to apply the formula to the rest of the rows.

Your `Order Size` column should now contain the correct labels for each order based on its sales value.

---

### 4. Session Wrap-up

*   You have successfully used Excel formulas to create new data from existing data.
*   You have practiced using fundamental statistical functions (`SUM`, `AVERAGE`, `MAX`, `MIN`, `COUNT`).
*   You have implemented business logic using the `IF` function to categorize data.
*   These skills are the bedrock of performing analysis in a spreadsheet environment.
*   **Next Session:** We will learn how to organize and query our data using Excel's powerful sorting and filtering capabilities.
# Session 18: Excel for Analysis (VLOOKUP)

**Unit 2: Data Tools and Platforms**
**Hour: 18**
**Mode: Practical Lab**

---

### 1. Objective

This lab covers `VLOOKUP`, one of the most famous and essential Excel functions. You will learn how to use it to look up a value in one table and bring the corresponding data into another table, effectively merging two datasets.

**This is a guided lab. The instructor will demonstrate these steps in Excel, and students will follow along.**

---

### 2. The Dataset

We need two tables for this exercise.

1.  Create a new sheet named `Orders`. Enter the following data. Notice it has a `ProductID` but not the `Product Name` or `Category`.

| OrderID | ProductID | Units Sold |
| :--- | :--- | :--- |
| 101 | P01 | 50 |
| 102 | P02 | 30 |
| 103 | P03 | 25 |
| 104 | P04 | 40 |
| 105 | P05 | 20 |
| 106 | P06 | 35 |

2.  Create a second sheet named `Products`. This will be our "lookup table".

| ProductID | Product Name | Category |
| :--- | :--- | :--- |
| P01 | Apples | Fruit |
| P02 | Bread | Bakery |
| P03 | Milk | Dairy |
| P04 | Oranges | Fruit |
| P05 | Cheese | Dairy |
| P06 | Croissant | Bakery |

**The Goal:** We want to bring the `Product Name` and `Category` from the `Products` sheet into our `Orders` sheet.

---

### 3. Understanding VLOOKUP

The `VLOOKUP` function means "Vertical Lookup". It searches for a value in the **first column** of a table and returns a corresponding value from a specified column in the same row.

The syntax is: `VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])`

*   **`lookup_value`**: The value you want to search for. (e.g., `P01`). This is the common key between the two tables.
*   **`table_array`**: The range of cells that contains the lookup table. (e.g., the data in the `Products` sheet).
*   **`col_index_num`**: The column number in the lookup table from which to retrieve the value. The count starts from 1. (e.g., to get `Product Name`, the index is 2).
*   **`[range_lookup]`**: This is almost always set to `FALSE` or `0`, which means "find an exact match".

---

### 4. Lab Activities

#### Activity 1: Looking Up the Product Name

1.  Go to the `Orders` sheet. In cell **D1**, type the header `Product Name`.
2.  In cell **D2**, we will write our first `VLOOKUP` formula.
    *   **`lookup_value`**: This is the `ProductID` for this row, which is in cell `B2`.
    *   **`table_array`**: This is our data in the `Products` sheet. Go to the `Products` sheet and select the entire data range, `A2:C7`. When you do this, Excel will write `Products!A2:C7` in your formula. **Crucially, we must lock this reference** by pressing **F4** (on Windows) or **Cmd+T** (on Mac). This changes the reference to `Products!$A$2:$C$7`, which prevents it from changing when we drag the formula down.
    *   **`col_index_num`**: We want the `Product Name`, which is the **2nd** column in our `Products` table. So the number is `2`.
    *   **`range_lookup`**: We need an exact match, so we use `FALSE`.
3.  The final formula in cell **D2** will be: `=VLOOKUP(B2, Products!$A$2:$C$7, 2, FALSE)`
4.  Press Enter. The cell should correctly show "Apples".
5.  Use the auto-fill handle on cell **D2** to drag the formula down for all orders.

#### Activity 2: Looking Up the Category

Now, let's repeat the process to get the `Category`.

1.  In cell **E1** of the `Orders` sheet, type the header `Category`.
2.  In cell **E2**, we write a new formula. It's almost identical to the last one.
    *   **`lookup_value`**: Still `B2`.
    *   **`table_array`**: Still `Products!$A$2:$C$7` (remember to lock it with F4).
    *   **`col_index_num`**: This time, we want the `Category`, which is the **3rd** column in our `Products` table. So the number is `3`.
    *   **`range_lookup`**: Still `FALSE`.
3.  The final formula in cell **E2** is: `=VLOOKUP(B2, Products!$A$2:$C$7, 3, FALSE)`
4.  Press Enter and auto-fill the formula down the column.

Your `Orders` sheet is now complete and enriched with data from the `Products` sheet.

---

### 5. Session Wrap-up

*   `VLOOKUP` is the fundamental way to merge datasets in Excel.
*   It requires a common key or ID (`ProductID` in our case) that exists in both tables.
*   Remember the four arguments: what you're looking for, where to look, which column to return, and always use `FALSE` for an exact match.
*   Locking the `table_array` with `$` signs (by pressing F4) is critical for dragging the formula correctly.
*   **Next Session:** We will move beyond Excel and get our first look at a professional Business Intelligence tool, which is designed for advanced visualization and dashboarding.
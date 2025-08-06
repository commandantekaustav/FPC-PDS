# Session 16: Excel for Analysis (Sorting and Filtering)

**Unit 2: Data Tools and Platforms**
**Hour: 16**
**Mode: Practical Lab**

---

### 1. Objective

This lab focuses on two essential data exploration techniques in Excel: sorting and filtering. These tools allow you to quickly organize your data and isolate specific information for analysis.

**This is a guided lab. The instructor will demonstrate these steps in Excel, and students will follow along.**

---

### 2. The Dataset

Continue using the `Sales Data` sheet from the previous session. It should include the `Total Sales` and `Order Size` columns you created.

| OrderID | Product | Category | Units Sold | Unit Price | Total Sales | Order Size |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 101 | Apples | Fruit | 50 | $1.20 | 60 | Small Order |
| 102 | Bread | Bakery | 30 | $3.50 | 105 | Large Order |
| 103 | Milk | Dairy | 25 | $4.00 | 100 | Large Order |
| 104 | Oranges | Fruit | 40 | $1.50 | 60 | Small Order |
| 105 | Cheese | Dairy | 20 | $5.00 | 100 | Large Order |
| 106 | Croissant | Bakery | 35 | $2.50 | 87.5 | Small Order |

---

### 3. Lab Activities

#### Activity 1: Basic Sorting

Let's organize our table to see the highest-selling orders first.

1.  Click anywhere inside your data table (e.g., cell C4).
2.  Go to the **Data** tab in the Excel ribbon.
3.  Find the **Sort** section.
4.  Click the large **Sort** button to open the Sort dialog box.
5.  In the dialog box:
    *   Set **Sort by** to `Total Sales`.
    *   Set **Sort On** to `Values`.
    *   Set **Order** to `Largest to Smallest`.
6.  Click **OK**.
7.  Your table will now be re-ordered, with the `$105` sale for Bread at the top.

**Task:** Try sorting the table alphabetically by the `Product` column (A to Z).

#### Activity 2: Multi-Level Sorting

What if we want to sort by `Category` first, and then within each category, sort by `Total Sales`?

1.  Click the **Data** -> **Sort** button again.
2.  In the Sort dialog box:
    *   Your first level should be `Total Sales`. Let's change it. Set **Sort by** to `Category` and **Order** to `A to Z`.
3.  Click the **Add Level** button. A new row will appear.
4.  In this second level:
    *   Set **Then by** to `Total Sales`.
    *   Set **Sort On** to `Values`.
    *   Set **Order** to `Largest to Smallest`.
5.  Click **OK**.
6.  Observe the result: The table is now grouped by Bakery, then Dairy, then Fruit. Within each of those categories, the orders are sorted from the highest sale to the lowest.

#### Activity 3: Filtering Data

Filtering allows you to temporarily hide rows that don't meet your criteria.

1.  Click anywhere inside your data table.
2.  Go to the **Data** tab and click the large **Filter** button (it looks like a funnel).
3.  You will now see small drop-down arrows appear in each header cell. This indicates that filtering is active.

**Task 1: Filter by a single category**
1.  Click the filter arrow in the `Category` header.
2.  Uncheck `(Select All)`.
3.  Check the box next to `Fruit`.
4.  Click **OK**.
5.  Only the rows for Apples and Oranges will be visible. The other rows are hidden, not deleted. Notice the row numbers on the left are now blue and non-sequential.

**Task 2: Clear the filter**
1.  Click the filter arrow in the `Category` header again (it will now show a funnel icon).
2.  Select **Clear Filter From "Category"**. All rows will reappear.

**Task 3: Filter by a number condition**
1.  Click the filter arrow in the `Units Sold` header.
2.  Hover over **Number Filters**.
3.  Select **Greater Than...**.
4.  In the dialog box, enter `30`.
5.  Click **OK**.
6.  Only the rows where `Units Sold` is greater than 30 will be visible.

---

### 4. Session Wrap-up

*   **Sorting** organizes all of your data based on specific criteria.
*   **Filtering** hides data that you don't want to see at the moment.
*   You can perform multi-level sorts to create more sophisticated views of your data.
*   Filtering is a powerful and fast way to query your data and answer specific questions without writing complex formulas.
*   **Next Session:** We will explore Excel's most powerful feature for summarizing data: PivotTables.
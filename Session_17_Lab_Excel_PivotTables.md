# Session 17: Excel for Analysis (PivotTables)

**Unit 2: Data Tools and Platforms**
**Hour: 17**
**Mode: Practical Lab**

---

### 1. Objective

This lab introduces PivotTables, arguably the most powerful data summarization tool in Excel. You will learn how to transform a raw data table into a dynamic summary report that can be "pivoted" to answer multiple business questions quickly.

**This is a guided lab. The instructor will demonstrate these steps in Excel, and students will follow along.**

---

### 2. The Dataset

Continue using the `Sales Data` sheet from the previous sessions. Ensure all filters are cleared and the data is visible.

---

### 3. Understanding PivotTables

A PivotTable has four main areas:
1.  **Filters:** Used to apply a high-level filter to your entire report.
2.  **Columns:** Creates the columns of your summary report.
3.  **Rows:** Creates the rows of your summary report.
4.  **Values:** The field you want to perform a calculation on (e.g., Sum, Average, Count).

**Analogy:** Think of your data as a pile of Lego bricks. A PivotTable is a special board that lets you instantly sort and stack those bricks by color, shape, or size to see how many of each you have.

---

### 4. Lab Activities

#### Activity 1: Creating Your First PivotTable

**Business Question:** "What is the total revenue (Total Sales) for each product **Category**?"

1.  Click anywhere inside your data table.
2.  Go to the **Insert** tab and click **PivotTable**.
3.  A dialog box will appear. Excel should automatically select your data range. Ensure the "New Worksheet" option is selected and click **OK**.
4.  You will be taken to a new sheet with the PivotTable builder interface. On the right, you'll see the "PivotTable Fields" pane with a list of your columns.

#### Activity 2: Building the Report

1.  From the "PivotTable Fields" list, find `Category`.
2.  **Click and drag** the `Category` field into the **Rows** area at the bottom of the pane. You will see the row labels (Bakery, Dairy, Fruit) appear in your PivotTable on the left.
3.  Now, find `Total Sales` in the list.
4.  **Click and drag** the `Total Sales` field into the **Values** area.
5.  **Done!** The PivotTable instantly calculates the sum of `Total Sales` for each category. It should show:
    *   Bakery: 192.5
    *   Dairy: 200
    *   Fruit: 120

#### Activity 3: "Pivoting" the Data

**New Business Question:** "How did sales for each **Product** perform? And let's break it down by **Order Size**."

We can answer this without creating a new table. We just "pivot" the existing one.

1.  In the "PivotTable Fields" pane, **drag** `Category` out of the **Rows** area to remove it.
2.  **Drag** the `Product` field into the **Rows** area. Your report now shows total sales for each product.
3.  Now, **drag** the `Order Size` field into the **Columns** area.
4.  Your PivotTable instantly transforms! It now shows a matrix with Products as rows, Order Size as columns, and the sum of Total Sales as the values. This allows you to see exactly how much revenue came from large vs. small orders for each product.

#### Activity 4: Changing the Value Calculation

**New Business Question:** "What was the **average** sale amount per category, not the total?"

1.  In the **Values** area, you will see "Sum of Total Sales". Click on it.
2.  Select **Value Field Settings**.
3.  In the dialog box, under "Summarize value field by", select **Average**.
4.  You can also click "Number Format" to format the result as currency.
5.  Click **OK**.
6.  The PivotTable now shows the average sale amount instead of the sum.

---

### 5. Session Wrap-up

*   PivotTables are the fastest way to summarize and aggregate data in Excel.
*   You learned how to build a summary report by dragging and dropping fields into the **Rows**, **Columns**, and **Values** areas.
*   The power of "pivoting" is the ability to quickly reconfigure your report to answer new questions without starting over.
*   You can change the calculation in the Values field from a `SUM` to an `AVERAGE`, `COUNT`, or other statistical measures.
*   **Next Session:** We will learn another critical Excel skill: merging data from different sources using the `VLOOKUP` function.
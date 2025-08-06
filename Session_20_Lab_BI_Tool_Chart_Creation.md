# Session 20: BI Tool First Chart Creation

**Unit 2: Data Tools and Platforms**
**Hour: 20**
**Mode: Practical Lab**

---

### 1. Objective

This lab builds on our introduction to BI tools. We will use the drag-and-drop interface to create two fundamental charts to answer specific business questions about the Telco churn data.

**This is a guided lab. The instructor will demonstrate these steps, and students will follow along.**

---

### 2. The Setup

Open your BI tool with the Telco Customer Churn dataset already connected from the previous session. You should be in a new, empty worksheet, ready to build a visualization.

---

### 3. Lab Activities

#### Activity 1: Creating a Bar Chart

**Business Question:** "Which contract type has the highest churn rate?"

1.  **Drag `Contract` to Columns:** From the Data pane, drag the `Contract` dimension to the **Columns** shelf. You will see three column headers appear: Month-to-month, One year, Two year.
2.  **Drag `Number of Records` or `Count of Customers` to Rows:** Drag the default count measure to the **Rows** shelf. A bar chart will appear, showing the total number of customers in each contract type.
3.  **Add `Churn` for Color:** This is the key step. Drag the `Churn` dimension from the Data pane and drop it onto the **Color** property in the Marks card. The bars will now be segmented by color, showing the proportion of "Yes" and "No" for churn within each contract.
4.  **Change to Percentage:** The current view shows the raw count. To see the *rate*, we need to change the calculation.
    *   In Tableau, right-click the `Count of Customers` pill on the Rows shelf, select "Quick Table Calculation" -> "Percent of Total". Then, right-click it again, select "Compute Using" -> "Table (Down)" or "Pane (Down)". This calculates the percentage within each bar.
    *   In Power BI, you would change the visual to a "100% Stacked Bar Chart".

![Churn by Contract Bar Chart](https://i.imgur.com/mO3xJgD.png)
*(Image showing a completed bar chart where the 'Month-to-month' bar has a much larger 'Yes' churn segment)*

**Interpretation:** You can immediately and visually confirm the hypothesis from Session 10: customers on a month-to-month contract churn at a dramatically higher rate than those on yearly contracts.

#### Activity 2: Creating a Scatter Plot

**Business Question:** "Is there a relationship between a customer's `tenure` (how long they've been a customer) and their `MonthlyCharges`? Does this differ for customers who churn?"

1.  Create a new worksheet.
2.  **Drag `tenure` to Columns:** Drag the `tenure` measure to the **Columns** shelf. It will likely default to `SUM(tenure)`. Right-click it and change it to **Dimension** to see each individual point.
3.  **Drag `MonthlyCharges` to Rows:** Drag the `MonthlyCharges` measure to the **Rows** shelf. Right-click and ensure it is also a **Dimension**. You should now see a single dot.
4.  **Disaggregate Marks:** In Tableau, go to the "Analysis" menu and uncheck "Aggregate Measures". This will plot a mark for every single customer. You will now see a cloud of points.
5.  **Add `Churn` for Color:** Just like before, drag the `Churn` dimension to the **Color** property on the Marks card.

![Churn Scatter Plot](https://i.imgur.com/2s4z5Yj.png)
*(Image showing a scatter plot. The churned customers (e.g., in orange) are concentrated in the area of low tenure and high monthly charges.)*

**Interpretation:** The visualization clearly shows two clusters:
*   Customers who churned (colored orange, for example) are heavily clustered in the bottom-left and top-left areas: they have low tenure, and can have either low or high monthly charges.
*   Customers who stayed (colored blue) are spread out but dominate the high-tenure (right side) of the plot.

---

### 4. Session Wrap-up

*   You have successfully created two of the most common and powerful chart types using a BI tool.
*   You learned that building a chart is about asking a question and dragging the corresponding Dimensions and Measures to the correct shelves.
*   Using properties like **Color** is essential for adding layers of detail to your analysis.
*   Most importantly, you saw how quickly a visual can confirm a hypothesis or reveal a pattern that would be difficult to see in a table of raw numbers.
*   **Next Session:** We will shift our focus entirely to Python and set up our programming environment for the rest of the course.
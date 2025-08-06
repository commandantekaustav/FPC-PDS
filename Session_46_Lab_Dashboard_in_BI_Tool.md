# Session 46: Dashboard Creation in a BI Tool

**Unit 4: Descriptive Statistics and Visualization**
**Hour: 46**
**Mode: Practical Lab**

---

### 1. Objective

This lab reinforces the principles of dashboarding by recreating the insights from our Python dashboard using an interactive BI tool (Tableau or Power BI). The goal is to understand the strengths of a BI tool for creating user-friendly, interactive reports.

**This is a guided lab. The instructor will demonstrate the workflow, and students will follow along.**

---

### 2. The BI Tool Workflow

Creating a dashboard in a BI tool follows a simple process:
1.  **Create Individual Worksheets:** Build each chart (or "viz") on its own separate worksheet.
2.  **Create a New Dashboard:** Open a new dashboard canvas.
3.  **Assemble the Dashboard:** Drag and drop the completed worksheets from the sidebar onto the canvas.
4.  **Add Interactivity:** Use filters that can control multiple worksheets at once.

---

### 3. Lab Activities

#### Activity 1: Connect to the Clean Data

*   **Important:** For this exercise, it's best to use a **cleaned** version of the data. Export the DataFrame from the end of Session 36 to a CSV file called `telco_clean.csv`.
*   In your BI tool, create a new connection to this `telco_clean.csv` file.

#### Activity 2: Create the Individual Worksheets (The 4 Vizzes)

Create four new worksheets, one for each of the plots from our 2x2 Python dashboard.

**Worksheet 1: Churn by Contract**
1.  Drag `Contract` to **Columns**.
2.  Drag `Number of Records` (or the count of customers) to **Rows**.
3.  Drag `Churn` to the **Color** property.
4.  Rename the sheet to "Churn by Contract".

**Worksheet 2: Churn by Internet Service**
1.  Drag `InternetService` to **Columns**.
2.  Drag `Number of Records` to **Rows**.
3.  Drag `Churn` to **Color**.
4.  Rename the sheet to "Churn by Internet Service".

**Worksheet 3: Tenure Distribution**
1.  Change the chart type to a **Histogram**.
2.  Drag the `tenure` measure to the main area.
3.  Drag `Churn` to **Color**.
4.  Rename the sheet to "Tenure Distribution".

**Worksheet 4: Monthly Charges Distribution**
1.  Change the chart type to a **Histogram**.
2.  Drag the `MonthlyCharges` measure to the main area.
3.  Drag `Churn` to **Color**.
4.  Rename the sheet to "Monthly Charges Distribution".

#### Activity 3: Assemble the Dashboard

1.  Click the "New Dashboard" icon at the bottom of the screen.
2.  You will see an empty canvas and a list of your completed worksheets on the left.
3.  **Drag and drop** each of the four worksheets onto the canvas. The BI tool will help you arrange them in a grid. Try to create the same 2x2 layout we had in Python.

![Assembling Dashboard](https://i.imgur.com/8QhF5zF.png)
*(Image showing the drag-and-drop interface of a BI tool dashboard canvas)*

#### Activity 4: Add Interactivity

This is where BI tools truly shine.

1.  **Add a Filter:** From any of the worksheets on the dashboard, find a field you want to filter by, for example, `PaymentMethod`. Right-click it and choose "Show Filter". A filter card will appear on the right side of the dashboard.
2.  **Make the Filter Global:** Click the drop-down menu on the new filter card. Go to **Apply to Worksheets** and select **All Using This Data Source**.

Now, when you check or uncheck different payment methods in the filter, **all four charts on the dashboard will update simultaneously**. This allows for a level of interactive exploration that is impossible with a static Python chart.

---

### 4. Session Wrap-up

*   You have successfully built a cohesive, multi-chart dashboard in a professional BI tool.
*   You understand the workflow of building individual charts on worksheets and then assembling them on a dashboard canvas.
*   You have experienced the primary advantage of BI tools: the ability to add **global, interactive filters** that allow users to explore the data for themselves.
*   This reinforces the idea of using the right tool for the job: Python for heavy cleaning and modeling, and BI tools for interactive reporting and interpretation.
*   **Next Session:** We will focus on how to present the insights from this dashboard to a business audience.
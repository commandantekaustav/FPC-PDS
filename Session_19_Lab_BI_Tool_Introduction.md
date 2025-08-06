# Session 19: BI Tool Introduction (Tableau / Power BI)

**Unit 2: Data Tools and Platforms**
**Hour: 19**
**Mode: Practical Lab**

---

### 1. Objective

This lab provides a high-level, guided tour of a modern Business Intelligence (BI) tool like Tableau or Power BI. The goal is to understand the interface, connect to a data source, and see how the drag-and-drop paradigm works.

**Note:** This is a conceptual and visual lab. The instructor will demonstrate these steps, and students are encouraged to follow along if they have the software installed, but the primary goal is to understand the process.

---

### 2. The BI Tool Environment

When you first open Tableau or Power BI, you'll generally see three main areas:

1.  **Connect Pane:** A list of all the different data sources you can connect to (Excel, CSV, SQL Server, etc.).
2.  **Data Source Page:** After connecting to data, this is where you can see a preview of your tables, create joins (similar to VLOOKUP), and do some light data cleaning.
3.  **Workspace / Canvas:** This is the main area where you build your visualizations ("vizzes" or "visuals") by dragging and dropping data fields.

---

### 3. Lab Activities

#### Activity 1: Connecting to Data

**Goal:** Connect to the TelCo Customer Churn dataset we used previously.

1.  **Download the data:** First, ensure you have the `Telco-Customer-Churn.csv` file saved on your computer.
2.  **In the BI Tool:**
    *   In the **Connect** pane, select the option for **Text file** (for Tableau) or **Get Data -> Text/CSV** (for Power BI).
    *   Navigate to and select the `Telco-Customer-Churn.csv` file you saved.
3.  **Data Source Page:**
    *   The tool will automatically load the data and show you a preview in a table format.
    *   It will try to guess the data type for each column (e.g., `MonthlyCharges` as a number, `Contract` as a string). You can review these and correct them if needed. For example, ensure `SeniorCitizen` is treated as a Whole Number.

    ![Data Source Preview](https://i.imgur.com/k2x2fGZ.png)
    *(Image showing the data preview screen in a BI tool)*

#### Activity 2: Understanding Dimensions and Measures

Once you move to the main workspace, the BI tool will automatically categorize your data fields into two groups in the "Data" pane on the left:

*   **Dimensions (Blue in Tableau):** These are **qualitative**, categorical fields. You use them to slice and dice your data. They are the "by" in your questions (e.g., "Sales *by* Region", "Churn *by* Contract Type").
    *   *Examples:* `Gender`, `Contract`, `PaymentMethod`, `InternetService`.

*   **Measures (Green in Tableau):** These are **quantitative**, numerical fields that can be aggregated (summed, averaged, etc.). They are the "what" you are measuring.
    *   *Examples:* `tenure`, `MonthlyCharges`, `TotalCharges`. It will also create a "Count of Customers" measure.

This automatic separation is a key feature that makes building vizzes intuitive.

![Dimensions and Measures](https://i.imgur.com/k9vjH8s.png)
*(Image showing the data pane with blue dimension pills and green measure pills)*

#### Activity 3: The Drag-and-Drop Canvas

The main workspace consists of "shelves" or "wells" where you drag your data fields. Common shelves include:

*   **Columns Shelf:** Fields dragged here will create columns in your chart.
*   **Rows Shelf:** Fields dragged here will create rows in your chart.
*   **Marks Card:** This is where you control the visual properties of your chart:
    *   **Color:** Drag a field here to color your marks by that field.
    *   **Size:** Drag a field here to size your marks by that field.
    *   **Label:** Drag a field here to add text labels.
    *   **Tooltip:** Drag fields here to add more information when you hover over a data point.

![Workspace Canvas](https://i.imgur.com/9bE2r9o.png)
*(Image showing the main workspace with Columns, Rows, and Marks Card shelves)*

---

### 4. Session Wrap-up

*   You have learned the basic layout of a professional BI tool.
*   You successfully connected to a CSV data source.
*   You understand the critical difference between **Dimensions** (categorical data for slicing) and **Measures** (numerical data for aggregating).
*   You are familiar with the drag-and-drop canvas, which is the core mechanic for building visualizations.
*   **Next Session:** We will use this knowledge to build our first charts and answer business questions with just a few clicks.
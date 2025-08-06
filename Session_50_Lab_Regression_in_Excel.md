# Session 50: Simple Regression in Excel

**Unit 5: Basics of Predictive Analytics**
**Hour: 50**
**Mode: Practical Lab**

---

### 1. Objective

This lab serves as a gentle introduction to the mechanics of predictive modeling using a familiar tool: Microsoft Excel. We will use the **Data Analysis ToolPak** to build a simple linear regression model and interpret its output. This helps to build intuition before we move to the more powerful Python environment.

**Goal:** Predict a customer's `TotalCharges` based on their `tenure`.

---

### 2. The Dataset & Setup

1.  Open the clean `telco_clean.csv` file you created in Unit 4. If you don't have it, load the Telco dataset into Python, perform the cleaning from Session 36, and save it using `df.to_csv('telco_clean.csv', index=False)`.
2.  **Enable the Data Analysis ToolPak:**
    *   In Excel, go to `File` -> `Options` -> `Add-ins`.
    *   At the bottom, next to "Manage:", select `Excel Add-ins` and click `Go...`.
    *   Check the box for `Analysis ToolPak` and click `OK`.
    *   A new `Data Analysis` button should now appear on your **Data** tab.

---

### 3. Lab Activities

#### Activity 1: Creating a Scatter Plot

First, let's visualize the relationship we want to model, just like we did in our Python labs.
1.  Select the `tenure` and `TotalCharges` columns.
2.  Go to the **Insert** tab.
3.  In the Charts section, choose **Scatter**.
4.  You should see a clear positive relationship, suitable for linear regression.

#### Activity 2: Running the Regression Analysis

1.  Go to the **Data** tab and click on the **Data Analysis** button.
2.  From the list, select **Regression** and click **OK**.
3.  This opens the Regression dialog box. We need to fill it in:
    *   **Input Y Range:** This is the variable we want to predict (the dependent variable). Select the entire `TotalCharges` column, including the header.
    *   **Input X Range:** This is the variable we are using to make the prediction (the independent variable). Select the entire `tenure` column, including the header.
    *   **Labels:** Check this box because we included the headers in our selection.
    *   **Output Range:** Choose a cell on the same worksheet where you want the top-left corner of the output to appear (e.g., cell `AA1`).
4.  Click **OK**.

#### Activity 3: Interpreting the Output

Excel will produce a large summary output. Let's focus on the most important parts.

**1. R Square (Coefficient of Determination)**
*   You will see a value for `R Square` (e.g., around 0.68).
*   **Interpretation:** This value tells you what percentage of the variation in the Y variable (`TotalCharges`) can be explained by the X variable (`tenure`). In this case, approximately **68%** of the variation in a customer's total charges can be explained by how long they've been a customer. This indicates a moderately strong relationship.

**2. The Coefficients Table**
*   This is the most important part. It gives you the "recipe" for your model. You will see two rows: `Intercept` and `tenure`.
*   **Intercept:** This is the predicted `TotalCharges` when `tenure` is 0. (e.g., around `-363.46`).
*   **`tenure` Coefficient:** This is the slope of the line. It tells you how much `TotalCharges` is predicted to increase for **every one-month increase** in `tenure`. (e.g., around `86.44`).

**The Model Equation:**
Based on these coefficients, we can write our predictive model:

`Predicted TotalCharges = 86.44 * tenure - 363.46`

**Making a Prediction:**
*   **Question:** What are the predicted total charges for a customer with a tenure of **50** months?
*   **Calculation:** `86.44 * 50 - 363.46 = 4322 - 363.46 = 3958.54`
*   **Conclusion:** Our model predicts that a customer with a 50-month tenure will have total charges of approximately $3958.54.

---

### 4. Session Wrap-up

*   You have successfully built your first predictive model using Excel's Data Analysis ToolPak.
*   You learned how to interpret the key outputs:
    *   **R Square** tells you how well your model fits the data.
    *   **Coefficients** give you the mathematical formula to make new predictions.
*   You used the model's formula to make a prediction for a new data point.
*   **Limitations:** While useful for simple models, this process is manual, not easily reproducible, and cannot handle complex algorithms.
*   **Next Session:** We will begin the process of building this same model in Python, which overcomes all of these limitations.
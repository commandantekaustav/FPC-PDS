# Session 11: Workflow in Practice (Map Case Study to Workflow)

**Unit 1: Introduction to Data Science**
**Hour: 11**
**Mode: Practical Lab / Activity**

---

### 1. Objective

This session is a hands-on planning and critical thinking activity. Using the TelCo Churn case study from the previous session, students will explicitly map the required tasks to the OSEMN data science workflow. This exercise solidifies their understanding of the workflow as a practical project plan.

---

### 2. The OSEMN Framework Recap

*   **O - Obtain:** Get the data.
*   **S - Scrub:** Clean the data.
*   **E - Explore:** Understand the data's patterns and relationships.
*   **M - Model:** Make predictions using the data.
*   **N - iNterpret:** Communicate the results.

---

### 3. In-Class Activity: Group Brainstorming

**Instructions:**
Break into small groups. For each phase of the OSEMN workflow, list 2-3 specific actions you would need to take for the TelCo Customer Churn project. Be as specific as possible.

---

#### **O - Obtain**
*   **Action 1:** __________________________________________________
*   **Action 2:** __________________________________________________
*   **Action 3:** __________________________________________________

<details>
  <summary>Click for Example Answers</summary>
  
  *   **Action 1:** Download the `.csv` file from the provided URL.
  *   **Action 2:** Load the `.csv` file into a Pandas DataFrame.
  *   **Action 3:** Verify the data loaded correctly by checking the first 5 rows with `.head()`.
</details>

<br>

#### **S - Scrub (Clean)**
*   **Action 1:** __________________________________________________
*   **Action 2:** __________________________________________________
*   **Action 3:** __________________________________________________

<details>
  <summary>Click for Example Answers</summary>
  
  *   **Action 1:** Investigate the `TotalCharges` column, which has an incorrect `object` data type, and convert it to a numeric type.
  *   **Action 2:** After conversion, check if `TotalCharges` has any missing values and decide on a strategy to handle them (e.g., fill with the median).
  *   **Action 3:** Check other columns for consistency (e.g., are `gender` values always 'Male' and 'Female'?).
</details>

<br>

#### **E - Explore (Exploratory Data Analysis)**
*   **Action 1:** __________________________________________________
*   **Action 2:** __________________________________________________
*   **Action 3:** __________________________________________________

<details>
  <summary>Click for Example Answers</summary>
  
  *   **Action 1:** Create a bar chart to visualize the number of customers who churned vs. those who didn't.
  *   **Action 2:** Create histograms to see the distribution of numerical features like `tenure` and `MonthlyCharges`.
  *   **Action 3:** Create bar charts to compare churn rates across different categories, like `Contract` type or `InternetService`.
</details>

<br>

#### **M - Model**
*   **Action 1:** __________________________________________________
*   **Action 2:** __________________________________________________
*   **Action 3:** __________________________________________________

<details>
  <summary>Click for Example Answers</summary>
  
  *   **Action 1:** Convert all categorical columns (like `gender`, `Contract`) into a numerical format that a machine learning model can understand (e.g., one-hot encoding).
  *   **Action 2:** Separate the data into features (the input columns) and the target (the 'Churn' column).
  *   **Action 3:** Split the data into a training set and a testing set.
  *   **Action 4 (Bonus):** Train a classification algorithm (like Logistic Regression) on the training data.
</details>

<br>

#### **N - iNterpret (Communicate)**
*   **Action 1:** __________________________________________________
*   **Action 2:** __________________________________________________
*   **Action 3:** __________________________________________________

<details>
  <summary>Click for Example Answers</summary>
  
  *   **Action 1:** Create a summary slide that shows the most important factors influencing churn (e.g., "Customers on month-to-month contracts are 4x more likely to churn.").
  *   **Action 2:** Explain the model's accuracy in simple business terms.
  *   **Action 3:** Provide a clear recommendation to the marketing team (e.g., "Focus retention efforts on new customers with high monthly charges and fiber optic service.").
</details>

---

### 4. Session Wrap-up

*   This exercise demonstrates that a data science project is not just about coding; it's about structured planning.
*   By mapping tasks to the workflow, we create a clear project plan that anyone on a team can understand.
*   This plan will be our guide for the rest of the course as we learn the skills needed to complete each step.
*   **Next Session:** We will execute the first part of our plan by loading the TelCo dataset and performing our initial hands-on exploration.
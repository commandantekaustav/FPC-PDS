# Session 6: Workflow in Practice (Case Study Introduction)

**Unit 1: Introduction to Data Science**
**Hour: 6**
**Mode: Practical Lab / Case Study**

---

### 1. Objective

This session applies the theoretical workflow to a concrete business problem. We will deconstruct a common business challenge and understand how a data scientist would frame it before writing any code.

---

### 2. The Business Problem

**Company:** TelCo, a major telecommunications provider.

**Problem:** TelCo is losing customers to competitors. Acquiring a new customer is 5-10 times more expensive than retaining an existing one. The management wants to proactively identify customers who are at a high risk of "churning" (leaving the company) so they can offer them targeted promotions and improve their service experience.

**The Goal:** Build a model that can predict whether a customer will churn or not based on their profile and usage history.

---

### 3. Framing the Problem for Data Science

*   **Business Goal:** Reduce customer churn.
*   **Data Science Goal:** Classify customers into two groups: `Churn = Yes` or `Churn = No`. This is a **binary classification** problem.
*   **Success Metric:** How do we know if our model is good? A simple metric would be **accuracy** (what percentage of customers did we correctly classify?). More advanced metrics like precision and recall would also be important.
*   **Business Impact:** If the model is successful, the marketing team can use the list of high-risk customers to run a retention campaign, potentially saving the company millions of dollars.

---

### 4. The Dataset: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

This is a classic public dataset that simulates real-world customer data.

*   **Obtain:** We have been given this dataset as a CSV file.
*   **Data Dictionary:** Understanding the columns is crucial.

| Column | Description | Data Type |
| :--- | :--- | :--- |
| `customerID` | A unique ID for each customer. | Text |
| `gender` | The customer's gender. | Categorical |
| `SeniorCitizen` | Whether the customer is a senior citizen (1, 0). | Numeric (Binary) |
| `Partner` | Whether the customer has a partner (Yes, No). | Categorical |
| `Dependents` | Whether the customer has dependents (Yes, No). | Categorical |
| `tenure` | Number of months the customer has been with the company. | Numeric |
| `PhoneService` | Whether the customer has phone service (Yes, No). | Categorical |
| `MultipleLines` | Whether the customer has multiple lines (Yes, No, No phone service). | Categorical |
| `InternetService` | Customer's internet service provider (DSL, Fiber optic, No).| Categorical |
| `OnlineSecurity` | Whether the customer has online security (Yes, No, No internet). | Categorical |
| `OnlineBackup` | Whether the customer has online backup (Yes, No, No internet). | Categorical |
| `DeviceProtection`| Whether the customer has device protection (Yes, No, No internet).| Categorical |
| `TechSupport` | Whether the customer has tech support (Yes, No, No internet). | Categorical |
| `StreamingTV` | Whether the customer has streaming TV (Yes, No, No internet). | Categorical |
| `StreamingMovies`| Whether the customer has streaming movies (Yes, No, No internet). | Categorical |
| `Contract` | The customer's contract term (Month-to-month, One year, Two year).| Categorical |
| `PaperlessBilling`| Whether the customer has paperless billing (Yes, No). | Categorical |
| `PaymentMethod` | The customer's payment method. | Categorical |
| `MonthlyCharges`| The amount charged to the customer monthly. | Numeric |
| `TotalCharges` | The total amount charged to the customer. | Numeric |
| **`Churn`** | **Whether the customer churned (Yes or No).** | **Target Variable**|

---

### 5. In-Class Activity: Brainstorming & Hypothesis Generation

Before we even look at the data, let's think like business analysts.

**Discussion Prompt:** "Based on the column descriptions, which factors do you *think* will be the most important predictors of churn? State your hypothesis."

*   *Example Hypothesis 1:* "I hypothesize that customers with **Month-to-month contracts** will churn more than customers with One or Two year contracts, because they have no long-term commitment."
*   *Example Hypothesis 2:* "I hypothesize that customers with **higher MonthlyCharges** will churn more, because they might find a cheaper competitor."
*   *Example Hypothesis 3:* "I hypothesize that customers with **shorter tenure** will churn more, as they are less loyal and may still be 'shopping around'."

**Goal:** This encourages critical thinking and connects the data back to real-world logic. This is the essence of "Substantive Expertise".

---

### 6. Session Wrap-up

*   We have successfully taken a vague business problem ("reduce churn") and framed it as a specific data science problem (a binary classification task).
*   We have a dataset and a clear understanding of what each column means.
*   We have formed initial hypotheses that we can test in the next phase.
*   **Next Session:** We will move to the hands-on part of the workflow. We'll load this exact dataset and perform the initial "Scrub" and "Explore" steps.
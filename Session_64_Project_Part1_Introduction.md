# Session 64: Capstone Project Part 1 (Problem Formulation)

**Unit 6: Data Ethics, Privacy, and Future Trends**
**Hour: 64**
**Mode: Practical Project**

---

### 1. Objective

This session kicks off our final capstone project. Today, we will introduce the project scenario, the dataset, and the business goal. The primary activity is to practice the first and most important step of any data science project: **framing the business problem** and defining what success looks like.

---

### 2. The Project Scenario

**Company:** A fictional US e-commerce company called "StyleSphere" that sells clothing and accessories.

**Business Problem:** The marketing team has a budget for a new promotional email campaign. They want to maximize the return on investment (ROI) by targeting only the customers who are **most likely to respond** to the offer. Sending emails to customers who won't buy is wasteful and can lead to them unsubscribing.

**Your Task as a Data Scientist:**
Analyze a dataset of past customer behavior and campaign responses to build a profile of the "ideal" customer to target. While we won't build a full predictive model, our EDA should lead to a clear, data-driven recommendation for the marketing team.

---

### 3. Introducing the Dataset: `marketing_campaign.csv`

This is a public dataset containing information about customers, their purchasing habits, and their response to a previous campaign.

**Data Dictionary (Key Columns):**

*   `ID`: Unique customer identifier.
*   `Year_Birth`: Customer's year of birth.
*   `Education`: Customer's education level.
*   `Marital_Status`: Customer's marital status.
*   `Income`: Customer's yearly household income.
*   `Kidhome`, `Teenhome`: Number of children/teens in the household.
*   `Dt_Customer`: Date of customer's enrollment with the company.
*   `Recency`: Number of days since the customer's last purchase.
*   `MntWines`, `MntFruits`, etc.: Amount spent on various product categories in the last 2 years.
*   `NumDealsPurchases`: Number of purchases made with a discount.
*   `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`: Number of purchases through different channels.
*   `NumWebVisitsMonth`: Number of visits to the company's website in the last month.
*   **`Response`**: **(This is our Target Variable)**. `1` if the customer accepted the offer in the last campaign, `0` otherwise.

---

### 4. In-Class Activity: Project Planning & Hypothesis Generation

**Instructions:**
In your groups, discuss and answer the following questions. This is your project plan.

**1. Business Goal:**
*   Restate the business problem in a single sentence.
    *   *Example:* "Our goal is to identify the key characteristics of customers who respond to marketing campaigns to improve targeting for future campaigns."

**2. Data Science Problem Type:**
*   Is this a supervised or unsupervised problem? Why?
    *   *Answer:* Supervised, because we have the labeled `Response` column (the "right answer").
*   Is it a regression or classification problem? Why?
    *   *Answer:* Classification, because the outcome is a discrete category (Responded=1, Did Not Respond=0).

**3. Initial Hypotheses (Brainstorm at least 3):**
*   Before looking at the data, what do you *think* will be the key predictors of a positive response?
    *   *Hypothesis 1 (Example):* "Customers with higher `Income` will be more likely to respond."
    *   *Hypothesis 2 (Example):* "Customers who have purchased more recently (`Recency` is low) will be more likely to respond."
    *   *Hypothesis 3 (Example):* "Customers with kids at home (`Kidhome` > 0) will be less likely to respond because their spending is focused elsewhere."

**4. OSEMN Workflow Plan:**
*   Briefly list one key action for each step of the workflow for this project.
    *   **Obtain:** Load the `marketing_campaign.csv` file.
    *   **Scrub:** Check for missing values (especially in `Income`), and check data types.
    *   **Explore:** Calculate summary statistics and create visualizations to test our hypotheses.
    *   **Model:** (For this project, our "model" will be the final recommendation).
    *   **iNterpret:** Create a final summary report or presentation for the marketing team.

---

### 5. Session Wrap-up

*   We have a clear business problem, a relevant dataset, and an initial project plan.
*   We have translated the business goal into a data science problem (supervised classification).
*   We have formed several testable hypotheses that will guide our exploration.
*   **Next Session:** We will execute the **Obtain** step by loading the data and performing our initial inspection.
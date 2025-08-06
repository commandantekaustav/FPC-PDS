# Session 59: Presenting Model Findings

**Unit 5: Basics of Predictive Analytics**
**Hour: 59**
**Mode: Lab / Activity**

---

### 1. Objective

This session focuses on the final step: communicating the results of our predictive model to a non-technical, business-focused audience. The goal is to synthesize our findings from the EDA, model evaluation, and interpretation labs into a clear, concise, and actionable summary.

**This is a structured writing and discussion activity.**

---

### 2. The Executive Summary Template

A good executive summary for a data science project should answer four key questions in simple terms:

1.  **The Business Problem:** What problem were we trying to solve?
2.  **Our Approach:** What did we do? (In very high-level terms).
3.  **The Key Findings:** What did we learn? What are the most important insights?
4.  **The Recommendations:** What should the business do next based on our findings?

---

### 3. In-Class Activity: Writing the Summary

**Instructions:**
Based on all the labs in Unit 5, fill in the blanks below to create a one-page executive summary for the TelCo Marketing Managers.

---

### **Executive Summary: Predicting Customer Churn**

#### 1. The Business Problem

TelCo is facing a significant challenge with customer churn, which is costly to the business. We were tasked with analyzing customer data to understand the key drivers of churn and to build a predictive model that can identify at-risk customers *before* they leave.

#### 2. Our Approach

We analyzed a dataset of over 7,000 customers. Our process involved:
*   **Exploratory Data Analysis (EDA):** We used descriptive statistics and visualizations to uncover initial patterns in the data.
*   **Predictive Modeling:** We built a **Logistic Regression** model, a standard machine learning technique, to predict the probability of a customer churning based on their profile and services.
*   **Model Evaluation:** We tested the model on unseen data to ensure its performance is reliable.

#### 3. The Key Findings

Our analysis revealed several critical insights:

*   **Finding 1: Contract Type is the #1 Predictor.** Customers on a **Month-to-Month** contract are overwhelmingly more likely to churn than those on one or two-year contracts. Our model identified this as the single most important factor.
*   **Finding 2: Tenure Matters.** Newer customers are a much higher churn risk. The average tenure for a customer who churned was only **~18 months**, compared to **~37 months** for a customer who stayed.
*   **Finding 3: Model Performance.** Our predictive model can identify at-risk customers with an overall **accuracy of approximately 80%**. More importantly, it is particularly good at identifying the characteristics of a churning customer. However, our model's main weakness is that it fails to identify about 48% of the customers who end up churning (this is its "recall" score).

#### 4. Recommendations

Based on these findings, we recommend a two-pronged strategy:

1.  **Immediate Action - Targeted Retention:** We can now provide the marketing team with a weekly list of customers our model has flagged as "high risk of churn". We recommend focusing this campaign on **customers with low tenure and month-to-month contracts**, offering them a promotional discount to switch to a one-year contract.
2.  **Strategic Improvement - Model Enhancement:** We should continue to refine the predictive model. By incorporating more data (such as customer support call logs) and testing more advanced algorithms, we can improve the model's recall and "catch" a higher percentage of true churners, further increasing the ROI of our retention campaigns.

---

### 4. Session Wrap-up

*   This exercise simulates the final, and often most important, part of a data scientist's job: translating complex analysis into business value.
*   A good summary avoids technical jargon (like "log-odds" or "F1-score") and focuses on the findings and their business implications.
*   The structure (Problem, Approach, Findings, Recommendations) is a reliable way to present your work effectively.
*   **Next Session:** We will conduct a final review of Unit 5 to solidify all the concepts of predictive modeling we have learned.
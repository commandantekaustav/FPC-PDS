# Session 47: Interpreting and Presenting a Dashboard

**Unit 4: Descriptive Statistics and Visualization**
**Hour: 47**
**Mode: Lab / Activity**

---

### 1. Objective

This session focuses on the final, critical step of the "iNterpret" phase: communication. Having a dashboard is not enough; a data scientist must be able to guide a business audience through it, explain the key insights, and provide actionable recommendations.

**This is a role-playing and discussion-based activity.**

---

### 2. The Scenario

*   **You are the Data Scientist.**
*   **Your audience is a group of Marketing Managers at TelCo.**
*   **Your goal:** Use the interactive dashboard you just built to convince them to focus their customer retention efforts on a specific, high-risk segment.

---

### 3. The Presentation Structure (The "Story")

A good data presentation follows a simple narrative structure:

1.  **The Hook (The "What"):** Start with the single most important finding. Don't bury the lead.
2.  **The Supporting Evidence (The "Why"):** Use the other charts on your dashboard to provide context and explain *why* the main finding is happening.
3.  **The Recommendation (The "So What?"):** State a clear, actionable recommendation based on your evidence.

---

### 4. In-Class Activity: Group Presentations

**Instructions:**
1.  Break into small groups.
2.  Each group will have 5 minutes to prepare a short (~2 minute) presentation based on the dashboard.
3.  Designate one person to be the "presenter".
4.  The presenter will "walk" the rest of the class (the "marketing managers") through the dashboard, following the story structure above.

**Presenter's Guided Script / Talking Points:**

**(Start with the dashboard showing all data, no filters applied)**

**1. The Hook (The "What")**

*   "Good morning. The goal of our analysis was to find the biggest drivers of customer churn. Our key finding is clear: **customers on month-to-month contracts are churning at an alarming rate.**"
*   (Point to the "Churn by Contract" chart). "As you can see, the vast majority of our churn comes from this single segment."

**2. The Supporting Evidence (The "Why")**

*   "So, why is this happening? Let's look at the profile of these customers."
*   (Point to the "Tenure Distribution" chart). "First, churners in general have a much lower tenure than loyal customers. They leave quickly."
*   (Point to the "Churn by Internet Service" chart). "We also see that customers with **Fiber optic** internet service have a very high rate of churn compared to those with DSL."
*   (Now, use the interactive filter). "Let's see what happens when we look at **only** the Fiber optic customers." (Apply the filter). "Notice that within the Fiber optic group, the month-to-month contract is still the primary source of churn. This confirms these two factors are linked."
*   (Point to the "Monthly Charges Distribution" chart). "This might be because our Fiber optic service, while fast, is also our most expensive. New customers on a flexible contract are likely being poached by competitors with lower promotional pricing."

**3. The Recommendation (The "So What?")**

*   "Based on this evidence, we have a clear, high-risk customer segment: **New customers (low tenure) on month-to-month contracts with Fiber optic internet service.**"
*   "My recommendation is that the marketing team designs a targeted retention campaign specifically for this group. This could be an offer to upgrade to a one-year contract at a discounted rate for the first few months. By stabilizing this volatile segment, we can make a significant impact on our overall churn numbers."

---

### 5. Session Wrap-up

*   This exercise demonstrated the difference between showing data and telling a story.
*   A good presentation has a clear narrative: hook, evidence, and recommendation.
*   Interactive dashboards are powerful presentation tools because they allow you to dynamically filter and answer audience questions in real-time.
*   The goal of a data presentation is not just to share insights, but to drive **action**.
*   **Next Session:** We will conduct a final review of Unit 4 with a capstone mini-project, applying all our EDA skills to a new dataset.
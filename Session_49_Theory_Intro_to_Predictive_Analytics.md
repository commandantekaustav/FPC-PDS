# Session 49: Introduction to Predictive Analytics

**Unit 5: Basics of Predictive Analytics**
**Hour: 49**
**Mode: Theory**

---

### 1. Objective

This session introduces the fundamental concepts of predictive analytics and machine learning. By the end of this hour, students will be able to:
*   Define machine learning and its relationship to predictive analytics.
*   Differentiate between the two main types of supervised learning: Regression and Classification.
*   Explain the difference between supervised and unsupervised learning.

---

### 2. Lecture & Discussion Points

#### What is Machine Learning?

So far, all of our analysis has been **descriptive** (what happened in the past?) or **diagnostic** (why did it happen?). Predictive analytics is about looking into the future.

*   **Formal Definition:** Arthur Samuel (1959) - Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed.
*   **Simple Definition:** Instead of writing explicit rules, you feed the computer data and let it learn the patterns itself.
*   **Analogy:**
    *   **Traditional Programming:** You are a chef with a very specific recipe (`IF temp > 350, cook for 10 mins, ELSE cook for 15 mins`). You write the rules.
    *   **Machine Learning:** You are a food critic who has tasted thousands of perfect and burnt cookies. You can't write the exact recipe, but you can instantly recognize a good cookie when you see one. You learn from **examples**. The ML model is the same; it learns the "recipe" from the data you show it.

#### Supervised vs. Unsupervised Learning

These are the two main paradigms in machine learning. The difference is simple: **Does the data have the "right answer" included?**

**1. Supervised Learning**
*   **Core Idea:** You train the model on data that has a known, labeled outcome (the "right answer"). The model's job is to learn the mapping from the inputs to the output.
*   **Analogy:** You are teaching a child to identify fruits. You show them a picture of a round, red fruit (**input data**) and say "this is an apple" (**labeled outcome**). After many examples, the child can identify a new apple they've never seen before.
*   **Our TelCo Dataset:** This is a supervised learning problem because our historical data includes the `Churn` column. For every customer in the past, we know the "right answer" (whether they churned or not).
*   **This is the most common type of machine learning used in business.**

**2. Unsupervised Learning**
*   **Core Idea:** You train the model on data that has **no** labeled outcome. The model's job is to find the hidden structure or patterns in the data all by itself.
*   **Analogy:** You give a child a big box of Lego bricks of different shapes and colors and say "organize these". The child might group them by color, by shape, or by size. There is no single "right answer", but the child finds inherent structure.
*   **Business Example:** **Customer Segmentation.** An e-commerce company has data on customer purchase history but no predefined "groups". They can use an unsupervised algorithm (like K-Means Clustering) to automatically discover segments of customers with similar buying habits (e.g., "Bargain Hunters", "High Spenders", "Weekend Shoppers"). We did this conceptually in our labs.
*   **Key Algorithm Type:** Clustering.

#### The Two Types of Supervised Learning

Supervised learning problems can be further broken down into two types based on the kind of output you are trying to predict.

**1. Regression**
*   **Goal:** Predict a **continuous numerical value**.
*   **The "Question" it answers:** "How much?" or "How many?"
*   **Examples:**
    *   Predicting the **price** of a house based on its size and location.
    *   Predicting the **number of sales** a store will have next month.
    *   Predicting the **temperature** tomorrow.
*   **Key Algorithms:** Linear Regression, Ridge Regression.

**2. Classification**
*   **Goal:** Predict a **discrete category or class label**.
*   **The "Question" it answers:** "Which one?" or "Is this A or B?"
*   **Examples:**
    *   Predicting whether an email is **spam or not spam** (Binary Classification).
    *   Predicting if a customer will **churn or not churn** (Binary Classification - our TelCo problem!).
    *   Predicting whether a picture contains a **cat, a dog, or a bird** (Multiclass Classification).
*   **Key Algorithms:** Logistic Regression, Decision Trees, Support Vector Machines.

---

### 3. In-Class Activity

**Prompt:** "For each of the following business problems, identify the type of machine learning problem it is."

1.  "Grouping your customers into different market segments based on their browsing behavior."
    *   *Answer:* **Unsupervised Learning (Clustering)**. There are no predefined groups.
2.  "Forecasting the total revenue your company will make next quarter."
    *   *Answer:* **Supervised Learning (Regression)**. The output is a continuous number (revenue).
3.  "Building a system to automatically approve or deny loan applications based on historical data."
    *   *Answer:* **Supervised Learning (Classification)**. The output is a discrete category (Approve/Deny).
4.  "Analyzing text from customer reviews to determine if the sentiment is positive, negative, or neutral."
    *   *Answer:* **Supervised Learning (Classification)**. The output is a discrete category.

---

### 4. Session Wrap-up

*   Machine learning is about learning patterns from data instead of being explicitly programmed.
*   **Supervised Learning** uses labeled data to make predictions.
*   **Unsupervised Learning** finds hidden patterns in unlabeled data.
*   Supervised problems are either **Regression** (predicting a number) or **Classification** (predicting a category).
*   Our TelCo churn problem is a **Supervised Classification** problem.
*   **Next Session:** We will start our final hands-on labs by building a simple regression model in Excel.
# Session 60: Unit 5 Review (Quiz & Q&A)

**Unit 5: Basics of Predictive Analytics**
**Hour: 60**
**Mode: Lab / Review**

---

### 1. Objective

This session is designed to review and solidify the core concepts of predictive analytics covered in Unit 5. Students will test their knowledge through a short quiz and participate in a Q&A session to clarify any remaining questions about the machine learning workflow.

---

### 2. Unit 5 Knowledge Check (Quiz)

**Instructions:** Answer the following questions based on the concepts learned in this unit.

---

**Question 1:**
You are asked to build a model to predict the exact dollar amount a customer will spend in the next month. What type of machine learning problem is this?
a) Classification
b) Regression
c) Clustering
d) Unsupervised Learning

<details>
  <summary>Click for Answer</summary>
  **Answer: b) Regression.** The target variable (exact dollar amount) is a continuous numerical value.
</details>

---

**Question 2:**
What is the primary purpose of splitting your data into a training set and a testing set?
a) To make the dataset smaller and faster to process.
b) To have a separate dataset for creating visualizations.
c) To evaluate the model's performance on unseen data.
d) To clean the data more effectively.

<details>
  <summary>Click for Answer</summary>
  **Answer: c) To evaluate the model's performance on unseen data.** This prevents "overfitting" and gives a true measure of how the model will perform in the real world.
</details>

---

**Question 3:**
Why is One-Hot Encoding (using `pd.get_dummies()`) necessary?
a) To make the data look cleaner in the DataFrame.
b) To convert numerical features into text.
c) To convert categorical text features into a numerical format that ML models can understand.
d) To reduce the number of columns in the dataset.

<details>
  <summary>Click for Answer</summary>
  **Answer: c) To convert categorical text features into a numerical format that ML models can understand.** Machine learning models are based on mathematics and cannot process raw text like 'Month-to-month'.
</details>

---

**Question 4:**
In a churn prediction model, a **False Negative (FN)** represents:
a) The model correctly predicted a customer would not churn.
b) The model incorrectly predicted a customer would churn.
c) The model incorrectly predicted a customer would NOT churn, but they actually did.
d) The model correctly predicted a customer would churn.

<details>
  <summary>Click for Answer</summary>
  **Answer: c) The model incorrectly predicted a customer would NOT churn, but they actually did.** This is often the most costly business error in a churn model.
</details>

---

**Question 5:**
You build a model to detect a rare disease (1% of the population has it). Your model has an accuracy of 99%. Why might this accuracy score be misleading?
a) Accuracy is not a valid metric for any model.
b) A model with 99% accuracy is perfect.
c) An R-squared score would be better.
d) A "dumb" model that always predicts "No Disease" would also be 99% accurate.

<details>
  <summary>Click for Answer</summary>
  **Answer: d) A "dumb" model that always predicts "No Disease" would also be 99% accurate.** This illustrates the accuracy paradox on imbalanced datasets. You need metrics like the Confusion Matrix to see if you are correctly identifying the rare, positive cases.
</details>

---

### 3. Open Q&A and Discussion

This is an open forum for students to ask any questions they have about the topics covered in Unit 5.

**Potential Discussion Prompts for the Instructor:**

*   "Can someone explain the difference between a False Positive and a False Negative in the context of an email spam filter?"
    *   *FP:* An important email is incorrectly sent to the spam folder.
    *   *FN:* A spam email is incorrectly allowed into the inbox.
*   "When would you choose to use Median imputation over Mean imputation for missing values?"
    *   When the data has outliers that would skew the mean.
*   "What's the difference between `model.fit()` and `model.predict()`?"
    *   `.fit()` is the training/learning step, done on the training data (`X_train`, `y_train`).
    *   `.predict()` is the testing/inference step, done on new, unseen data (`X_test`).
*   "Can we build a model to predict `TotalCharges` using categorical variables like `Contract`?"
    *   Yes! You would one-hot encode the `Contract` column first, and then the model would learn a separate coefficient for each of the new binary columns.

---

### 4. Session Wrap-up

*   This session solidified your understanding of the end-to-end predictive modeling workflow, from data preparation to model training and evaluation.
*   You are now familiar with the key terminology and concepts that define supervised machine learning.
*   This concludes the practical, hands-on modeling portion of the course.
*   **Next Session:** We will begin our final unit, Unit 6, by discussing the critical ethical considerations that every data scientist must be aware of.
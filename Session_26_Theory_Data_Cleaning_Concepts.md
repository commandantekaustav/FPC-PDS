# Session 26: Data Cleaning Concepts

**Unit 3: Data Collection and Cleaning**
**Hour: 26**
**Mode: Theory**

---

### 1. Objective

This session provides the theoretical foundation for the most critical and time-consuming part of the data science workflow: data cleaning (scrubbing). Students will learn to identify common types of "dirty" data and understand the conceptual approaches to fixing them.

---

### 2. Lecture & Discussion Points

#### Why is Data Cleaning So Important?

The "Garbage In, Garbage Out" (GIGO) principle is the golden rule of data science. If you feed a machine learning model messy, inaccurate data, you will get messy, inaccurate predictions. Your analysis is only as good as the quality of your data.

**Data cleaning is the process of detecting and correcting (or removing) corrupt or inaccurate records from a dataset.**

#### Common Types of "Dirty" Data and How to Handle Them

**1. Missing Data**
*   **What it is:** Empty cells in your dataset, often represented as `NaN` (Not a Number) in Pandas.
*   **Why it happens:** Data wasn't collected, entry error, privacy concerns.
*   **How to handle it:**
    *   **Deletion:**
        *   **Listwise Deletion (Row):** If a row has a missing value, delete the entire row. *Use with caution!* This is only safe if you have a huge dataset and are missing very few values. Otherwise, you throw away valuable information.
        *   **Column Deletion:** If a column is mostly empty (e.g., > 60% missing), it might be better to delete the entire column as it doesn't provide much information.
    *   **Imputation (Filling in the blanks):** This is often the preferred method.
        *   **For Numerical Data:** Fill missing values with the **mean** or **median** of the column. (Median is generally safer as it's not affected by outliers).
        *   **For Categorical Data:** Fill missing values with the **mode** (the most frequent value) of the column, or with a constant like "Missing".
        *   **Advanced Methods:** Use a machine learning model (like k-Nearest Neighbors) to predict the missing value based on other columns.

**2. Duplicate Data**
*   **What it is:** The exact same row appearing more than once.
*   **Why it happens:** Entry errors, merging datasets from different sources, system glitches.
*   **How to handle it:** This is usually an easy fix. Identify the duplicate rows and delete them, keeping only the first occurrence.

**3. Outliers**
*   **What it is:** Data points that are significantly different from other observations.
*   **Why it happens:**
    *   Legitimate but extreme values (e.g., the CEO's salary in a dataset of employee salaries).
    *   Measurement or data entry errors (e.g., a person's age is listed as 150).
*   **How to handle it:** This is highly context-dependent.
    *   **Investigate:** First, determine if it's an error or a real value.
    *   **If it's an error:** Treat it like missing data (delete or impute).
    *   **If it's a real value:** You have a choice. You can keep it, but be aware that it can skew statistical measures (like the mean) and some machine learning models. Sometimes, outliers are the most interesting data points (e.g., for fraud detection).

**4. Inconsistent Formatting & Typos**
*   **What it is:** The same category being represented in multiple ways.
*   **Why it happens:** Free-text entry fields, lack of data validation.
*   **Examples:**
    *   "NY", "N.Y.", "New York"
    *   "Female", "female", "F"
    *   "Ltd.", "Limited"
*   **How to handle it:** This requires "standardization". Choose one canonical format (e.g., "New York") and write a script to replace all other variations with that one format.

**5. Incorrect Data Types**
*   **What it is:** Data stored in the wrong format, like numbers being stored as text. We saw this with `TotalCharges` in our Telco dataset.
*   **Why it happens:** Often due to hidden characters (like spaces) or inconsistent entries in a column.
*   **How to handle it:**
    1.  Identify the problematic characters that are preventing the conversion.
    2.  Remove or replace them.
    3.  Convert the column to the correct data type (e.g., from `object` to `float`).

---

### 3. Session Wrap-up

*   Data cleaning is the most important step for accurate and reliable analysis.
*   We've identified the main culprits of "dirty" data: missing values, duplicates, outliers, and inconsistencies.
*   We've discussed the high-level strategies for dealing with each of these problems.
*   **Next Session:** We will put theory into practice by starting our hands-on labs for data collection, beginning with web scraping.
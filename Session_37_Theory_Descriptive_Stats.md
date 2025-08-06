# Session 37: Descriptive Statistics

**Unit 4: Descriptive Statistics and Visualization**
**Hour: 37**
**Mode: Theory**

---

### 1. Objective

This session introduces the core concepts of descriptive statistics. By the end of this hour, students will be able to:
*   Define descriptive statistics and its purpose in the data science workflow.
*   Differentiate between measures of central tendency and measures of dispersion.
*   Understand the meaning of mean, median, mode, variance, and standard deviation.

---

### 2. Lecture & Discussion Points

#### What are Descriptive Statistics?

*   **Definition:** Descriptive statistics are brief summary coefficients that quantitatively describe or summarize the main features of a collection of data.
*   **Purpose:** They don't allow us to make conclusions or predictions beyond the data we have analyzed. Instead, they simplify large amounts of data into a sensible, easy-to-understand summary.
*   **Analogy:** If your dataset is a full-length movie, descriptive statistics are the movie's trailer. They don't show you every scene, but they give you a very good idea of the main plot points, characters, and genre.
*   **Role in Workflow:** This is the "E" in OSEMN (Explore). It's the first step in quantitative data exploration.

#### Part 1: Measures of Central Tendency

These measures describe the "center" or "typical" value of a dataset.

**1. Mean (Average)**
*   **Definition:** The sum of all values divided by the number of values.
*   **Calculation:** `Sum of Values / Number of Values`
*   **When to use it:** Excellent for data that is symmetrically distributed (like a bell curve) and doesn't have extreme outliers.
*   **Weakness:** It is **highly sensitive to outliers**.
    *   **Example:** Consider the salaries: `$50k, $60k, $70k, $80k, $900k`.
    *   The mean is `($50+$60+$70+$80+$900)/5 = $232k`. This is not a "typical" salary in this group; the outlier has skewed it.

**2. Median**
*   **Definition:** The middle value in a dataset that has been sorted from smallest to largest.
*   **Calculation:** Sort the data. If there is an odd number of values, the median is the one in the middle. If there is an even number, it's the average of the two middle values.
*   **When to use it:** This is the preferred measure of central tendency when your data is skewed or has outliers.
*   **Strength:** It is **robust to outliers**.
    *   **Example:** For the salaries `$50k, $60k, $70k, $80k, $900k`, the sorted list is the same.
    *   The median is the middle value: `$70k`. This is a much better representation of the "typical" salary.

**3. Mode**
*   **Definition:** The value that appears most frequently in a dataset.
*   **When to use it:**
    *   It is the only measure of central tendency that can be used for **categorical data**. (e.g., In the `Contract` column, the mode is 'Month-to-month').
    *   It can be useful for numerical data to see if there is a common, recurring value.
*   **Note:** A dataset can have more than one mode (bimodal, multimodal) or no mode at all.

#### Part 2: Measures of Dispersion (or Variability)

These measures describe how "spread out" or "varied" the data points are.

**1. Range**
*   **Definition:** The difference between the highest and lowest values in a dataset.
*   **Calculation:** `Maximum Value - Minimum Value`
*   **Weakness:** Extremely sensitive to outliers. A single high or low value can make the range misleading.

**2. Variance**
*   **Definition:** The average of the squared differences from the Mean. It measures how far each number in the set is from the average.
*   **Conceptual Steps:**
    1.  Calculate the mean.
    2.  For each value, subtract the mean and square the result.
    3.  Calculate the average of those squared differences.
*   **Challenge:** The units are squared (e.g., "dollars squared"), which is not intuitive to interpret.

**3. Standard Deviation (σ)**
*   **Definition:** The square root of the variance. This is the **most common and important measure of dispersion**.
*   **Calculation:** `sqrt(Variance)`
*   **Strength:** It brings the measure of spread back into the original units of the data (e.g., "dollars" instead of "dollars squared"), making it much easier to interpret.
*   **Interpretation:**
    *   A **low** standard deviation indicates that the data points tend to be very close to the mean.
    *   A **high** standard deviation indicates that the data points are spread out over a wider range of values.

---

### 3. In-Class Activity

**Prompt:** "Consider two sets of student test scores (out of 100):"
*   **Class A:** `[80, 81, 82, 83, 84]`
*   **Class B:** `[60, 70, 80, 90, 100]`

"Calculate the mean and standard deviation for both. What do the results tell you about the two classes?"

*   **Class A Mean:** `82`. **Class B Mean:** `82`.
*   **Discussion:** "The mean is the same! Does this mean the classes performed similarly?"
*   **Class A Std Dev:** `~1.58`. **Class B Std Dev:** `~15.81`.
*   **Conclusion:** "No, they performed very differently. Class A was very consistent, with everyone scoring close to the average. Class B had a huge spread in scores, with some students doing very well and some doing poorly. The standard deviation reveals this story, while the mean alone hides it."

---

### 4. Session Wrap-up

*   Descriptive statistics summarize the key features of our data.
*   **Central Tendency (Mean, Median, Mode)** tells us about the "typical" value.
*   **Dispersion (Range, Standard Deviation)** tells us about the "spread" of the data.
*   Using these measures together provides a much more complete picture than using any single one alone.
*   **Next Session:** We'll discuss the principles of visualizing these statistics effectively to tell a compelling story with data.
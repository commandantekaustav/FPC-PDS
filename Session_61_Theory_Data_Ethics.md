# Session 61: Data Ethics (Bias, Fairness, and Transparency)

**Unit 6: Data Ethics, Privacy, and Future Trends**
**Hour: 61**
**Mode: Theory / Discussion**

---

### 1. Objective

This session introduces the critical topic of data ethics. By the end of this hour, students will be able to:
*   Define algorithmic bias and identify its primary sources.
*   Understand the concepts of fairness and transparency in machine learning.
*   Recognize the potential for data science models to cause real-world harm if not developed responsibly.

---

### 2. Lecture & Discussion Points

#### Why Does Data Ethics Matter?

Machine learning models are increasingly used to make important decisions that affect people's lives: who gets a loan, who gets a job interview, how long a sentence a criminal receives, what medical treatment a patient gets.

If the models making these decisions are biased or unfair, they can perpetuate and even amplify existing societal inequalities. A data scientist is not just a technician; they have a professional and moral responsibility to understand and mitigate these risks.

#### Part 1: Algorithmic Bias

*   **Definition:** Algorithmic bias occurs when a computer system reflects the implicit values of the humans who created it, or is trained on biased data. The model produces results that are systematically prejudiced.
*   **Key Insight:** A model can be mathematically optimal (e.g., have high accuracy) and still be ethically wrong.

**Where does bias come from?**

1.  **Biased Data (The most common source):**
    *   **Historical Bias:** The data reflects existing prejudices in the world.
        *   *Famous Example:* An AI recruiting tool was trained on 10 years of a company's hiring data. Since the company had historically hired more men for technical roles, the model learned to penalize resumes that contained the word "women's" (e.g., "captain of the women's chess club"). The model perfectly learned the company's past bias.
    *   **Measurement Bias:** The data is collected or measured in a way that is not representative of all groups.
        *   *Example:* A facial recognition system trained primarily on images of light-skinned faces will have a much higher error rate when trying to identify dark-skinned faces.
    *   **Selection Bias:** The data collected is not a random sample of the target population.
        *   *Example:* A model predicting income is trained only on data from people who have smartphones and live in major cities. The model will perform poorly for rural populations.

2.  **Biased Model / Algorithm:**
    *   Sometimes the way the model is designed or the variables chosen can introduce bias.
    *   *Example:* Using a variable like a person's zip code as a feature in a loan application model. Because of historical segregation, zip code can be a strong proxy for race. The model might inadvertently learn to discriminate based on race, even if "race" is not an explicit feature. This is called **redlining**.

#### Part 2: Fairness

*   **Definition:** Fairness in machine learning means ensuring that a model's predictions do not disproportionately harm (or benefit) specific subgroups of the population, particularly those in legally protected categories (race, gender, etc.).
*   **The Challenge:** There is no single mathematical definition of "fairness" that everyone agrees on. Sometimes, improving one type of fairness can make another type worse.
    *   *Example Fairness Metric 1:* "Demographic Parity" - The model's approval rate should be the same for all groups (e.g., the percentage of men and women approved for a loan should be equal).
    *   *Example Fairness Metric 2:* "Equal Opportunity" - Among all qualified applicants, the model's approval rate should be the same for all groups (e.g., of all the men and women who would *actually* pay back a loan, an equal percentage should be approved).

#### Part 3: Transparency and Interpretability

*   **Definition:** Transparency is the idea that we should be able to understand *why* a model made a particular decision. Some models are "black boxes."
*   **Black Box Models:** Complex models like deep neural networks can be incredibly accurate, but it's almost impossible to trace the exact reason for a specific prediction.
*   **Interpretable Models:** Simpler models like Linear Regression and Decision Trees are highly interpretable. You can look at the coefficients or the tree structure to understand exactly which features were most important.
*   **The Trade-off:** There is often a trade-off between model accuracy and interpretability.
*   **Why it matters:** If a model denies someone a loan, and you can't explain why, how can that person appeal the decision? In regulated industries like finance and healthcare, interpretability is often a legal requirement.

---

### 3. In-Class Activity

**Case Study Discussion: COMPAS (Correctional Offender Management Profiling for Alternative Sanctions)**

*   **Background:** COMPAS is a tool used in some US courts to predict the likelihood of a defendant re-offending (recidivism). Judges sometimes use this risk score to help set bail and determine sentences.
*   **The Controversy (ProPublica Investigation):** A 2016 investigation found that:
    *   The model was no more accurate than predictions made by untrained people online.
    *   The model was twice as likely to **falsely flag** Black defendants as future criminals than white defendants (higher False Positive rate for one group).
    *   The model was twice as likely to **falsely label** white defendants as low-risk who then went on to re-offend (higher False Negative rate for another group).
*   **Discussion Prompts:**
    1.  What kind of bias might have been present in the historical data used to train this model? (Historical bias in arrest records and policing).
    2.  Which type of error (False Positive or False Negative) is "worse" in this context? (A False Positive means an innocent person is denied bail or gets a longer sentence. A False Negative means a potentially dangerous person is released).
    3.  Is it fair for a "black box" algorithm to have this much influence over someone's freedom?

---

### 4. Session Wrap-up

*   Data ethics is not an afterthought; it is a core part of the data science process.
*   Bias often originates from the data we use, reflecting past societal inequalities.
*   A data scientist's job includes investigating their data and models for potential unfairness and being transparent about their model's limitations.
*   **Next Session:** We will continue this discussion by focusing on the related topics of data privacy and protection.```
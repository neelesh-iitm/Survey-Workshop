Okay, Professor, here are detailed lecture notes for Session 2, structured for delivery and potentially as a handout for participants.

---

**Lecture Notes: Session 2 - Statistical Analysis of Survey Data (Excel & Jamovi)**

**Session Duration:** 1 Hour

**Instructor:** Professor [Your Name]

**Date:** [Date]

**I. Introduction & Recap (5 mins)**

*   **Welcome Back:** Briefly welcome participants to Session 2.
*   **Recap Session 1:** "In our last session, we focused on designing effective surveys and collecting data using Google Forms. We learned about crafting clear questions, structuring questionnaires, and the basics of sampling and ethics."
*   **Session 2 Goal:** "Today, we move from data collection to making sense of that data. Our goal is to learn how to prepare survey data for analysis, calculate and interpret fundamental statistics, and use common tools – Excel for basic tasks and the user-friendly statistical software Jamovi for more advanced analysis – to extract meaningful insights."
*   **Learning Objectives (Reiterate):**
    *   Prepare and inspect survey data (cleaning, coding).
    *   Compute and interpret descriptive statistics (frequencies, means, etc.).
    *   Use Excel for basic analysis & visualization.
    *   Introduce Jamovi for descriptive and basic inferential statistics (e.g., t-tests).
    *   Understand how to interpret statistical outputs in context.

**II. The Crucial First Step: Data Preparation (10 mins)**

*   **Why Prepare Data?**
    *   "Garbage In, Garbage Out" (GIGO) principle applies strongly here. Analysis is only as good as the data quality.
    *   Raw survey data is often messy: incomplete answers, typos, inconsistent entries, responses needing coding.
    *   Ensures accuracy, consistency, and usability for analysis tools.
*   **Key Data Preparation Tasks:**
    *   **Data Cleaning:**
        *   *Checking for Incompleteness:* Identify partially filled surveys. Decide on handling (e.g., exclude respondent, exclude specific missing answers).
        *   *Identifying Invalid Entries:* Look for out-of-range values (e.g., a '6' on a 1-5 scale), typos in text fields, inconsistent answers (if logic checks possible).
        *   *Handling Outliers (Brief Mention):* Extreme values that might skew results (e.g., an income vastly higher than others). Requires careful consideration – are they errors or genuine extreme cases?
    *   **Data Coding:**
        *   *Converting Categorical to Numeric (if needed):* Some software prefers numbers. E.g., Male=1, Female=2; Yes=1, No=0. *Crucial:* Keep a **codebook** documenting these assignments.
        *   *Coding Open-Ended Responses:* For qualitative analysis, themes might be identified and coded. For quantitative use, sometimes specific keywords or sentiments can be coded numerically (e.g., Positive=1, Neutral=0, Negative=-1). *Note: Detailed qualitative analysis is beyond this session, but coding is the first step.*
    *   **Data Organization (Spreadsheet Format):**
        *   Standard structure: Rows = Respondents (Cases), Columns = Variables (Survey Questions).
        *   **Clear Column Headers:** Use short, informative names (e.g., `Q1_Gender`, `Q5_Satisfaction`, `Age`). Avoid spaces or special characters if possible (use underscores).
        *   Consistency: Ensure data types within columns are consistent (e.g., all numbers in a numeric column).
    *   **Handling Missing Data (Brief Overview):**
        *   Common issue in surveys.
        *   *Simple Approaches:* Listwise deletion (remove entire respondent if *any* data missing - can lose a lot of data), Pairwise deletion (use available data for each specific calculation - sample size varies), Mean/Median imputation (replace missing with average - can distort variance).
        *   *Advanced Methods:* Multiple imputation (more sophisticated, often preferred).
        *   *Key Point:* Be aware of missing data, report how it was handled, understand the potential impact on results. For today, we'll mostly work with complete data or note where data is missing.
*   **Example:** Show a small snippet of "raw" data vs. "cleaned & coded" data.

**III. Summarizing the Story: Descriptive Statistics (10 mins)**

*   **Purpose:** The foundation of analysis. Provides a summary of the main features of the data. Answers basic questions like "What did people say?" or "What's the typical response?".
*   **Types of Variables Dictate Statistics:**
    *   **Categorical Variables** (Nominal/Ordinal - e.g., Gender, Yes/No, Education Level):
        *   **Frequency:** Count of responses in each category.
        *   **Percentage:** Proportion of responses in each category (Frequency / Total N * 100).
        *   *Interpretation:* Shows the distribution across categories. Which options were most/least popular?
        *   *Example:* "Q1: Preferred Work Mode - Remote: 60 (60%), Hybrid: 30 (30%), Office: 10 (10%). N=100." -> Tells us remote work is the strong preference in this sample.
    *   **Scale/Numeric Variables** (Interval/Ratio - e.g., Age, Rating Scales 1-5, Income):
        *   **Measures of Central Tendency:**
            *   *Mean:* Arithmetic average (Sum of values / N). Sensitive to outliers.
            *   *Median:* Middle value when data is sorted. Robust to outliers.
            *   *Mode:* Most frequent value (can be used for categorical too).
        *   **Measures of Dispersion (Variability):**
            *   *Range:* Maximum - Minimum. Simple but sensitive to outliers.
            *   *Standard Deviation (SD):* Average distance of data points from the mean. Most common measure of spread. Higher SD = more variability.
            *   *Variance:* Standard Deviation squared.
        *   *Interpretation:* Mean/Median show the "typical" score. SD shows how spread out the responses are.
        *   *Example:* "Q5: Satisfaction (1-5 scale) - Mean: 3.8, Median: 4, SD: 0.9." -> Average satisfaction is slightly positive; the middle respondent rated 4; responses are moderately clustered around the mean.
*   **Visualizing Distributions:** Mention that charts (bar charts for categorical, histograms for scale) help visualize these descriptive statistics.

**IV. Tools for Analysis: Excel & Jamovi (5 mins)**

*   **Microsoft Excel:**
    *   Ubiquitous spreadsheet software.
    *   Good for: Data entry, cleaning, basic calculations, simple charts, Pivot Tables for summaries.
    *   Accessible, familiar to many.
    *   Limitations: Can become cumbersome for complex statistics, not primarily designed for rigorous statistical testing (though add-ins exist).
*   **Jamovi:**
    *   Free, open-source statistical software.
    *   User-friendly point-and-click interface (like SPSS).
    *   **Built on R:** Combines the power and flexibility of the R statistical language with ease of use. No coding required for standard analyses. (Reference: `medium.com` point).
    *   Good for: Descriptive statistics, inferential tests (t-tests, ANOVA, Chi-Square, Regression, etc.), publication-ready tables and plots.
    *   Excellent alternative to paid software (SPSS, SAS). Continuously updated with new modules.
*   **Approach Today:** Use Excel for initial summaries/charts, then show how Jamovi streamlines descriptives and enables easy inferential testing.

**V. Basic Analysis & Visualization in Excel (Demonstration - 5 mins, Activity Prep)**

*   **Focus:** Quick summaries and visual insights.
*   **Demonstrate (using sample dataset):**
    *   **Calculating Frequencies:** Using `COUNTIF` function or Pivot Tables.
        *   *Scenario:* Count responses for a categorical question (e.g., "Yes"/"No").
    *   **Calculating Descriptives:** Using `AVERAGE`, `MEDIAN`, `STDEV.S` functions.
        *   *Scenario:* Calculate mean, median, SD for a Likert scale question.
    *   **Creating Basic Charts:** Using Excel's charting tools.
        *   *Scenario:* Create a Bar Chart for frequencies, or a Pie Chart (use cautiously - best for few categories).
*   **Prepare for Hands-On:** Ensure participants have the sample dataset open in Excel.

**VI. Introduction to Jamovi & Descriptive Analysis (Demonstration - 10 mins, Activity Prep)**

*   **Interface Overview:** Briefly show the Jamovi layout (Data view, Analysis tab, Results window). Dynamic updates are a key feature.
*   **Importing Data:** Show how to open a dataset (e.g., CSV, Excel file). Jamovi recognizes variable types (Nominal, Ordinal, Continuous).
*   **Generating Descriptive Statistics:**
    *   Navigate to `Analyses` -> `Exploration` -> `Descriptives`.
    *   Move variables of interest into the `Variables` box.
    *   Show automatic output tables (N, Missing, Mean, Median, SD for continuous; Frequencies/Percentages for nominal/ordinal).
    *   Tick boxes for additional stats (e.g., Variance, Range) or Plots (e.g., Histograms, Bar plots).
*   **Compare with Excel:** Highlight the ease and comprehensiveness of Jamovi's output for standard descriptives.
*   **Prepare for Hands-On:** Ensure participants have Jamovi installed and the sample dataset ready.

**VII. Introduction to Inferential Statistics with Jamovi (Demonstration - 5 mins, Activity Prep)**

*   **Purpose:** Moving beyond describing the sample to making inferences or testing hypotheses about the broader population (acknowledging sampling limitations). Answering questions like "Is there a real difference between groups?" or "Are these two variables related?".
*   **Focus on Interpretation, Not Deep Theory:**
*   **Example 1: Independent Samples T-test:**
    *   *Purpose:* Compare the means of a continuous variable between two independent groups.
    *   *Scenario:* "Does satisfaction (Q5 - scale) differ significantly between Male and Female respondents (Q1 - categorical)?"
    *   *Demo:* Navigate to `Analyses` -> `T-Tests` -> `Independent Samples T-Test`. Assign Dependent Variable (Q5) and Grouping Variable (Q1).
    *   *Key Output:* Group means, **p-value**.
*   **Example 2: Chi-Square Test of Association:**
    *   *Purpose:* Test if there is a statistically significant association between two categorical variables.
    *   *Scenario:* "Is there an association between Year of Study (Categorical) and Workshop Attendance (Yes/No - Categorical)?"
    *   *Demo:* Navigate to `Analyses` -> `Frequencies` -> `Contingency Tables`. Assign variables to Rows and Columns. Select 'Chi-square' test under 'Statistics'.
    *   *Key Output:* Contingency table (observed counts), **p-value** for the Chi-square test.
*   **Interpreting the p-value (Simplified):**
    *   The p-value represents the probability of observing the data (or something more extreme) if there were *no real difference/association* in the population.
    *   **Common Threshold:** p < 0.05.
    *   *If p < 0.05:* We conclude the observed difference/association is "statistically significant" (unlikely due to random chance alone *in this sample*).
    *   *If p ≥ 0.05:* We conclude there is not enough evidence to say the difference/association is statistically significant.
*   **Prepare for Hands-On:** Provide clear scenarios for participants to test.

**VIII. Hands-On Activity (Guided - 15 mins)**

*   **Goal:** Apply the demonstrated techniques in Excel and Jamovi.
*   **Dataset:** Use provided sample dataset or collated Session 1 data.
*   **Part 1: Excel (5 mins)**
    *   **Task 1:** Calculate Frequency & Percentage for a categorical variable ([Q_Categorical]) using `COUNTIF` or Pivot Table.
    *   **Task 2:** Calculate Mean, Median, SD for a scale variable ([Q_Scale]) using functions.
    *   **Task 3:** Create a Bar Chart showing the frequencies from Task 1.
*   **Part 2: Jamovi (10 mins)**
    *   **Task 1:** Import the dataset into Jamovi.
    *   **Task 2:** Reproduce descriptive statistics for [Q_Categorical] and [Q_Scale] using `Exploration` -> `Descriptives`. Compare output with Excel.
    *   **Task 3 (Guided Inferential):**
        *   *Scenario:* "Does [Q_Scale]'s average response differ between groups defined by [Q_GroupingVariable]?" (e.g., Satisfaction by Gender).
        *   *Action:* Run an Independent Samples T-test. Identify the group means and the p-value. Interpret the p-value (significant or not?).
        *   *(Optional/Alternative Scenario):* "Is there an association between [Q_Categorical1] and [Q_Categorical2]?" Run a Chi-Square test. Interpret the p-value.
*   **Facilitation:** Provide clear step-by-step guidance. Troubleshoot installation/software issues quickly. Encourage questions.

**IX. Interpretation: Beyond the Numbers (5 mins)**

*   **Crucial Skill:** Statistics provide numbers; researchers provide meaning.
*   **Connect Back to Research Questions:** What does a mean score of 3.8 on satisfaction *actually tell us* about how users feel? How does the frequency distribution answer our initial query?
*   **Statistical vs. Practical Significance:**
    *   A result can be statistically significant (p < 0.05) but practically meaningless.
    *   *Example:* A large survey finds a statistically significant difference of 0.05 points on a 1-5 satisfaction scale between two groups. Is this difference large enough to warrant different strategies or interventions? Probably not.
    *   Consider the **magnitude** of the effect (e.g., difference in means, strength of association) alongside the p-value.
    *   Requires **domain knowledge** and **judgment**.
*   **Context is Key:** Interpret findings within the context of the study population, the specific questions asked, and potential limitations (e.g., sampling method, response rate).

**X. Key Takeaways & Conclusion (5 mins)**

*   **Recap the Core Messages:**
    *   **Data Prep is Foundational:** Clean, coded, organized data is essential for reliable analysis.
    *   **Descriptives First:** Always start by summarizing your data (frequencies, means, SDs) to understand basic patterns.
    *   **Excel for Basics:** Useful for quick summaries, tables, and standard charts.
    *   **Jamovi for Accessibility & Power:** Free, user-friendly interface built on R, makes descriptive and inferential statistics (like t-tests, chi-square) accessible without coding.
    *   **Interpretation is Paramount:** Go beyond p-values; consider practical significance and context to draw meaningful conclusions.
*   **Encouragement:** Analysis is a skill that develops with practice. These tools provide the means, but critical thinking drives the insights.
*   **Q&A:** Open floor for final questions.
*   **Thank You & Next Steps (if any).**

---

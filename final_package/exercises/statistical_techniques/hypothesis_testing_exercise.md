# Interactive Exercise: Hypothesis Testing with Survey Data

## Overview
This exercise provides hands-on experience with formulating and testing hypotheses using survey data. Participants will learn to apply appropriate statistical tests, interpret results, and draw valid conclusions based on survey responses.

## Duration
45 minutes

## Materials Needed
- Sample survey datasets with variables suitable for hypothesis testing
- Hypothesis testing worksheet
- Computer with statistical software (Excel with Data Analysis add-in, SPSS, R, or similar)
- Reference guide for common statistical tests
- Calculator (if computers unavailable)

## Group Size
Pairs or groups of 3

## Instructions for Facilitator

1. Divide participants into pairs or small groups
2. Distribute the sample datasets and hypothesis testing worksheets
3. Review the hypothesis testing process and key concepts
4. Guide participants through each step of the exercise
5. Facilitate group discussion about results and interpretations
6. Conduct a final debrief to reinforce key concepts

## Exercise Structure

### Phase 1: Hypothesis Formulation (10 minutes)

Participants will:
1. Review the survey data and research context
2. Identify relationships or differences to investigate
3. Formulate null and alternative hypotheses
4. Determine appropriate significance level (α)

### Phase 2: Test Selection and Execution (20 minutes)

Participants will:
1. Select appropriate statistical tests based on:
   - Research question
   - Data types (nominal, ordinal, interval, ratio)
   - Sample characteristics
2. Check test assumptions
3. Perform the selected statistical tests
4. Calculate p-values and test statistics

### Phase 3: Interpretation and Conclusions (15 minutes)

Participants will:
1. Interpret test results in context of the hypotheses
2. Make decisions about rejecting or failing to reject null hypotheses
3. Discuss practical significance vs. statistical significance
4. Present findings to the larger group

## Sample Research Scenarios

### Scenario 1: Customer Preferences by Demographics
Research Question: Do preferences for product features differ by age group?
- Dataset includes customer ratings of product features and demographic information
- Potential tests: ANOVA, Chi-square test of independence

### Scenario 2: Employee Satisfaction Factors
Research Question: Is there a relationship between work-life balance satisfaction and overall job satisfaction?
- Dataset includes employee ratings on various satisfaction measures
- Potential tests: Correlation analysis, regression analysis

### Scenario 3: Marketing Campaign Effectiveness
Research Question: Did the new marketing campaign increase purchase intent compared to the previous campaign?
- Dataset includes purchase intent ratings from two different time periods
- Potential tests: Independent samples t-test, Mann-Whitney U test

## Hypothesis Testing Worksheet

### Part 1: Hypothesis Formulation

**Research Scenario**: ________________

**Research Question**: ________________

**Variables of Interest**:
- Independent/Grouping Variable: ________________
- Dependent/Outcome Variable: ________________

**Null Hypothesis (H₀)**: ________________

**Alternative Hypothesis (H₁)**: ________________

**Significance Level (α)**: ________________

### Part 2: Test Selection

**Selected Statistical Test**: ________________

**Rationale for Test Selection**:
- Data type considerations: ________________
- Sample size considerations: ________________
- Distribution assumptions: ________________
- Other factors: ________________

**Test Assumptions**:
1. ________________
2. ________________
3. ________________

**Are all assumptions met?** Yes / No / Partially
If not, how will you address this? ________________

### Part 3: Test Execution

**Test Statistic Calculation**:
- Formula used: ________________
- Calculated value: ________________

**Degrees of Freedom** (if applicable): ________________

**P-value**: ________________

**Critical Value** (if applicable): ________________

### Part 4: Interpretation

**Decision**: Reject H₀ / Fail to reject H₀

**Statistical Interpretation**:
- What does this result mean statistically? ________________
- Confidence interval (if applicable): ________________
- Effect size (if calculated): ________________

**Practical Interpretation**:
- What does this result mean in the context of the research question? ________________
- How strong/meaningful is the effect? ________________
- What are the practical implications? ________________

**Limitations**:
- What factors might affect the validity of these conclusions? ________________
- How might the results be different under other conditions? ________________

## Common Statistical Tests Reference Guide

### For Comparing Groups

| Test | When to Use | Data Types | Example Research Question |
|------|-------------|------------|---------------------------|
| Independent Samples t-test | Compare means between two unrelated groups | IV: Categorical (2 groups)<br>DV: Interval/Ratio | Do men and women differ in satisfaction scores? |
| Paired Samples t-test | Compare means between two related measurements | IV: Categorical (2 time points/conditions)<br>DV: Interval/Ratio | Did satisfaction scores change after the intervention? |
| One-way ANOVA | Compare means between three or more unrelated groups | IV: Categorical (3+ groups)<br>DV: Interval/Ratio | Do satisfaction scores differ among age groups? |
| Chi-Square Test | Compare frequency distributions between categorical variables | IV: Categorical<br>DV: Categorical | Is product preference associated with gender? |
| Mann-Whitney U | Compare distributions between two unrelated groups (non-parametric) | IV: Categorical (2 groups)<br>DV: Ordinal | Do two groups differ in their rankings? |
| Kruskal-Wallis | Compare distributions between three or more unrelated groups (non-parametric) | IV: Categorical (3+ groups)<br>DV: Ordinal | Do multiple groups differ in their rankings? |

### For Examining Relationships

| Test | When to Use | Data Types | Example Research Question |
|------|-------------|------------|---------------------------|
| Pearson Correlation | Measure linear relationship between two variables | Two Interval/Ratio variables | Is age related to satisfaction score? |
| Spearman Correlation | Measure monotonic relationship between two variables (non-parametric) | Two Ordinal (or higher) variables | Is rank in company related to job satisfaction ranking? |
| Simple Linear Regression | Predict one variable based on another | IV: Interval/Ratio<br>DV: Interval/Ratio | Can we predict satisfaction from number of purchases? |
| Multiple Regression | Predict one variable based on multiple others | IVs: Interval/Ratio<br>DV: Interval/Ratio | Which factors best predict customer satisfaction? |
| Logistic Regression | Predict categorical outcome based on one or more predictors | IVs: Any<br>DV: Categorical | What factors predict whether a customer will purchase again? |

## Debrief Discussion Questions

1. What challenges did you face in formulating clear hypotheses?
2. How did you decide which statistical test was most appropriate?
3. What surprised you about the results of your hypothesis tests?
4. How would you explain your findings to someone without statistical knowledge?
5. What additional analyses might help strengthen your conclusions?
6. How might these findings influence business decisions or strategies?
7. What are the limitations of the hypothesis testing approach you used?

## Tips for Facilitator

- Emphasize the importance of formulating clear, testable hypotheses before looking at the data
- Remind participants to check test assumptions before interpreting results
- Encourage discussion about the difference between statistical and practical significance
- If participants are struggling with calculations, focus on conceptual understanding
- Highlight common misinterpretations of p-values and statistical significance
- Connect hypothesis testing back to the broader research questions and business context
- For advanced groups, introduce concepts like effect size, power analysis, or multiple comparisons

## Extension Activities (if time permits)

1. **Effect Size Calculation**: Have participants calculate and interpret effect sizes for their tests
2. **Alternative Tests**: Ask groups to identify what test they would use if assumptions were violated
3. **Power Analysis**: Introduce the concept of statistical power and sample size determination
4. **Multiple Hypotheses**: Discuss the implications of testing multiple hypotheses and potential corrections
5. **Bayesian Perspective**: Briefly introduce Bayesian alternatives to traditional hypothesis testing

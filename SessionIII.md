**Lecture Notes: Session 3 - Advanced Data Analysis (Python & R)**


**I. Introduction: Beyond Point-and-Click (5 mins)**

*   **Welcome & Recap:** "Welcome to our final session. We've covered survey design (Session 1) and foundational analysis using Excel and the user-friendly Jamovi (Session 2). Recall that Jamovi uses the powerful R language behind the scenes."
*   **Today's Goal:** "This session introduces you to the world of **programmatic data analysis** using **Python** and **R**. We'll explore *why* researchers use code, see *how* basic analysis looks in these languages, and understand the benefits for more complex, reproducible research."
*   **Learning Objectives (Reiterate):**
    *   Discover Python/R for advanced, reproducible survey analysis.
    *   Understand advantages of scripts (reproducibility, automation, flexibility).
    *   See basic coding workflow: read data -> transform -> analyze/visualize.
    *   Demystify code by running simple scripts & interpreting output.
*   **Setting Expectations:** "This is an *introduction*, not a full programming course. The aim is to demystify coding and show its potential, empowering you to explore further if interested."

**II. Why Use Code for Data Analysis? (10 mins)**

*   **Limitations of GUI Tools (Excel, Jamovi):**
    *   Excellent for interactive exploration and standard analyses.
    *   Can become cumbersome for:
        *   Very large datasets.
        *   Highly repetitive tasks (e.g., analyzing 50 similar questions).
        *   Complex, multi-step cleaning/transformation processes.
        *   Custom or non-standard statistical methods/visualizations.
        *   Ensuring *exact* reproducibility months later or by others.
*   **Advantages of Script-Based Analysis (Python/R):**
    *   **1. Reproducibility:**
        *   The script *is* the documentation. Every step (cleaning, filtering, analysis, plotting) is explicitly recorded.
        *   Anyone (including your future self) can re-run the *exact* analysis. Crucial for verification, publication, building on prior work.
        *   Enhances transparency and credibility of research findings.
    *   **2. Automation:**
        *   Easily handle repetitive tasks (loops, functions). Analyze dozens of variables or datasets with minimal extra effort.
        *   Efficiently process large datasets that might crash spreadsheet software.
    *   **3. Flexibility & Power:**
        *   Access to a vast ecosystem of libraries/packages for virtually any statistical technique (basic to cutting-edge).
        *   Perform complex data manipulations ("data wrangling") easily.
        *   Create highly customized visualizations beyond standard chart types.
        *   Integrate analysis with other tasks (e.g., report generation, web scraping).
    *   **4. Collaboration:** Scripts can be easily shared, reviewed, and modified by collaborators (supports version control like Git).

**III. Introducing the Tools: Python & R (10 mins)**

*   **Two Leading Languages for Data Science & Research:** Both are free, open-source, and have large, active communities.
*   **Python:**
    *   *Characteristics:* General-purpose language known for readable syntax. Strong in data science, machine learning, web development, automation. Gentle learning curve for basics.
    *   *Key Data Analysis Libraries:*
        *   **Pandas:** Core library for data manipulation and analysis (DataFrames).
        *   **NumPy:** Fundamental package for numerical computation.
        *   **Matplotlib / Seaborn:** Popular libraries for data visualization.
        *   **Statsmodels / Scikit-learn:** For statistical modeling and machine learning.
    *   *Environment:* Often used with Jupyter Notebooks (interactive coding) or IDEs like VS Code, PyCharm. Google Colab for easy cloud access.
*   **R:**
    *   *Characteristics:* Created *specifically* for statistics and data visualization. Vast collection of packages for statistical modeling. Steeper initial learning curve for some, but powerful for stats.
    *   *Key Data Analysis Packages (often within the 'Tidyverse'):*
        *   **dplyr:** Data manipulation verbs (filter, mutate, group_by, summarize).
        *   **ggplot2:** Powerful and flexible data visualization system (grammar of graphics).
        *   **readr / readxl:** For reading data files.
        *   **Base R:** Also contains powerful functions for stats and plotting.
        *   **Specialized Packages:** `lme4` (mixed models), `tidytext` (text analysis), thousands more on CRAN.
    *   *Environment:* Primarily used with RStudio (an excellent IDE). Can also run R code within Jamovi's syntax mode.
*   **Which to Choose?** No single "best" answer. Depends on background, specific needs, community you work with. Both are excellent. Seeing both helps understand the common *concepts*.

**IV. Basic Workflow Demo: Python & R (15 mins)**

*   **Goal:** Show a simple, parallel analysis in both languages using the familiar survey dataset.
*   **Scenario:** "Load the survey data (CSV). Calculate the average satisfaction score (Q5) for different groups based on another question (e.g., Q1_Gender). Create a bar chart visualizing this comparison."
*   **Python Demo (using Jupyter Notebook / Google Colab):**
    *   *(Live Code / Show Pre-written Code Step-by-Step)*
    *   `import pandas as pd` # Load the pandas library
    *   `df = pd.read_csv('survey_data.csv')` # Read data into a DataFrame
    *   `print(df.head())` # Display first few rows to check
    *   `# Calculate mean satisfaction per group`
    *   `mean_satisfaction = df.groupby('Q1_Gender')['Q5_Satisfaction'].mean()`
    *   `print(mean_satisfaction)` # Show the result table
    *   `# Create a simple bar chart`
    *   `import matplotlib.pyplot as plt`
    *   `mean_satisfaction.plot(kind='bar')`
    *   `plt.title('Average Satisfaction by Gender')`
    *   `plt.ylabel('Mean Satisfaction Score')`
    *   `plt.show()` # Display the plot
    *   *Explanation:* Explain each line simply ("import brings in tools", "read_csv loads data", "groupby groups rows", ".mean() calculates average", ".plot makes the chart").
*   **R Demo (using RStudio / Jamovi Syntax Mode):**
    *   *(Live Code / Show Pre-written Code Step-by-Step)*
    *   `library(dplyr)` # Load dplyr package
    *   `library(ggplot2)` # Load ggplot2 package
    *   `df <- read.csv("survey_data.csv")` # Read data
    *   `print(head(df))` # Display first few rows
    *   `# Calculate mean satisfaction per group`
    *   `mean_satisfaction <- df %>%`
    *   `  group_by(Q1_Gender) %>%`
    *   `  summarize(avg_satisfaction = mean(Q5_Satisfaction, na.rm = TRUE))` # na.rm handles missing values
    *   `print(mean_satisfaction)` # Show the result table
    *   `# Create a bar chart using ggplot2`
    *   `ggplot(mean_satisfaction, aes(x = Q1_Gender, y = avg_satisfaction)) +`
    *   `  geom_bar(stat = "identity") +`
    *   `  labs(title = "Average Satisfaction by Gender", y = "Mean Satisfaction Score", x = "Gender")`
    *   *Explanation:* Explain the pipe `%>%` ("take the data and then..."), `group_by`, `summarize`, and the layered approach of `ggplot2`.
*   **Key Point:** Both languages achieve the same result with slightly different syntax but similar underlying logic (load -> group -> aggregate -> plot).

**V. Reproducible Research in Practice (5 mins)**

*   **The Script is the Record:** Saving your Jupyter Notebook (.ipynb) or R script (.R) captures *everything*.
*   **Benefits Revisited:**
    *   Run the *exact* same analysis tomorrow, next year, or on updated data.
    *   Share with colleagues for verification or collaboration.
    *   Submit code as supplementary material for publications (increasingly common/required).
    *   Adapt the script easily for similar future projects.
*   **Beyond Just Saving:** Mention version control systems like Git/GitHub as the next level for managing code changes and collaboration (optional, brief mention).

**VI. Hands-On Activity: Guided Script Execution (10 mins)**

*   **Goal:** Demystify running code; show that you can use existing scripts.
*   **Setup:** Participants provided with simple, pre-written Python (.ipynb) and R (.R) scripts performing the demo task. Suggest Google Colab for Python (no install needed) or RStudio/Jamovi Syntax Mode for R.
*   **Guided Walkthrough:**
    1.  Open the script (in Colab, RStudio, etc.).
    2.  Facilitator explains the first block/chunk of code.
    3.  Participants execute that block (e.g., "Run Cell" in Colab/Jupyter, "Run" button in RStudio).
    4.  Observe the output (data loading, table, plot).
    5.  Repeat for subsequent blocks.
    6.  **Small Modification:** Ask participants to change something simple (e.g., change `Q5_Satisfaction` to another numeric question variable name in the script, change the plot title) and re-run to see the effect.
*   **Focus:** Build confidence by successfully running code and seeing immediate results. Frame errors as normal parts of coding and debugging. Provide support. Emphasize that starting with examples and modifying them is a valid learning strategy.

**VII. Unleashing Advanced Capabilities (Brief Mention) (3 mins)**

*   **The Power of Libraries/Packages:**
    *   The simple examples barely scratch the surface.
    *   **Need complex modeling?** R: `lme4`, `brms`. Python: `statsmodels`, `scikit-learn`.
    *   **Need text analysis on open-ended questions?** R: `tidytext`, `quanteda`. Python: `NLTK`, `spaCy`.
    *   **Need interactive visualizations?** R: `shiny`. Python: `plotly`, `bokeh`.
    *   **Need machine learning?** Both have extensive libraries.
*   **Takeaway:** Programming opens doors to sophisticated analyses tailored to specific research questions, going far beyond standard GUI options.

**VIII. Key Takeaways & Conclusion (7 mins)**

*   **Recap Core Messages:**
    *   **Code = Flexibility & Reproducibility:** Scripting analysis (Python/R) ensures transparency, allows easy re-runs, and handles complex tasks.
    *   **Automation & Advanced Analysis:** Efficiently process large data; access cutting-edge statistical methods and custom visualizations.
    *   **Coding is Approachable:** Start small, modify examples (like today's!). You don't need to be an expert overnight. View it as another tool.
    *   **Rich Ecosystems (Python & R):** Both are free, powerful, widely supported, with vast libraries. Choose based on preference/needs.
    *   **Practice Builds Confidence:** Experiment with the provided scripts. Explore online tutorials (DataCamp, Coursera, free resources). The learning curve is manageable with persistence.
*   **Final Encouragement:** "You now have a glimpse into how programming can enhance your research. Don't be intimidated! Even basic scripting skills can significantly boost your analytical capabilities. Consider this the start of a potential new learning journey."
*   **Q&A:** Open floor for final questions.
*   **Thank You & Course Wrap-up:** Thank participants for attending all sessions. Provide contact information.

---

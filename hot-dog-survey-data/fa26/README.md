# Hot Dog Sandwich Survey

## Overview

This project explores opinions about the question:

> **Is a hot dog a sandwich?**

The dataset contains survey responses collected through live, in-person interviews at a football game. The analysis focuses on the overall distribution of responses and whether responses differ across academic years.

---

# Data Provenance

The data were collected through **live, in-person interviews conducted at a football game**.

Respondents included:

- Members of the marching band
- Approximately **250–300 additional people approached at the football game**

Each participant was asked whether they believed a hot dog is a sandwich. Responses were recorded along with the respondent's academic year.

## Sampling Method and Limitations

The dataset is best described as a **convenience sample**. Respondents were interviewed from people available at the football game rather than selected through a formal probability-based random sampling procedure.

Potential limitations include:

- **Convenience sampling:** People attending the football game were more accessible than people outside the event.
- **Event-specific population:** Football attendees may not represent the broader population.
- **Marching band representation:** Marching band members represent a specific subgroup within the sample.
- **Response bias:** Because the question is subjective and informal, respondents may interpret the meaning of "sandwich" differently.

Therefore, results should primarily be interpreted as describing **the people interviewed at this football game**, rather than the opinions of the entire population.

---

# Data Dictionary

| Variable | Type | Description |
|---|---|---|
| `Last Name` | Text | Respondent's last name or identifying field |
| `First name` | Text | Respondent's first name or identifying field |
| `Year` | Integer | Respondent's academic year, coded from 1 to 4 |
| `Is a hotdog a sandwhich?` | Categorical | Respondent's answer: `Yes` or `No` |

## Privacy Note

Names are not necessary for the statistical analysis and should be excluded from analysis when possible.

---

# Exploratory Data Analysis

## Plot 1: Overall Responses

The first plot shows the overall distribution of responses to the question, **"Is a Hotdog a Sandwich?"**

![Overall Yes vs. No Responses](images/overall_responses.png)

**Figure 1.** Overall Yes and No responses. The pie chart provides a visual summary of the proportion of surveyed respondents who considered a hot dog to be a sandwich versus those who did not.

---

## Plot 2: Responses by Academic Year

The second plot compares Yes and No responses across academic years.

![Responses by Academic Year](images/responses_by_year.png)

**Figure 2.** Yes and No responses by academic year. The chart allows comparison of the response distribution among Years 1 through 4.

### Summary by Academic Year

| Year | Yes | No | Total | Percent Yes |
|---|---:|---:|---:|---:|
| 1 | 39 | 98 | 137 | 28.5% |
| 2 | 41 | 97 | 138 | 29.7% |
| 3 | 30 | 91 | 121 | 24.8% |
| 4 | 34 | 89 | 123 | 27.6% |

The percentage answering Yes was relatively similar across all four academic years, ranging from approximately **24.8% to 29.7%**.

---

# Quantification of Uncertainty

## Sample Proportion

The proportion of respondents answering Yes is calculated as:

\[
\hat{p} = \frac{\text{Number of Yes responses}}{\text{Total number of responses}}
\]

Using the Excel formulas included in the analysis, the project can calculate:

- Total sample size
- Number of Yes responses
- Observed proportion answering Yes
- Standard error
- Lower and upper bounds of a 95% confidence interval

## 95% Confidence Interval

A standard approximate 95% confidence interval for a proportion is:

\[
\hat{p} \pm 1.96\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
\]

### Important Interpretation

Because this dataset was collected using a **convenience sample**, the confidence interval should be interpreted cautiously. It quantifies sampling variability under standard statistical assumptions but does **not** account for potential bias caused by the sampling method.

Therefore, the results should not automatically be generalized to all students or the general population.

---

# Conclusions

1. This dataset was collected through live, in-person interviews at a football game.
2. The majority of surveyed respondents answered No when asked whether a hot dog is a sandwich.
3. The proportion answering Yes was relatively similar across the four academic years, ranging from approximately 24.8% to 29.7%.
4. The two visualizations summarize both the overall response distribution and differences across academic years.
5. Because the survey used a convenience sample, the findings are best interpreted as describing the interviewed respondents rather than a broader population.

---

# Reproducibility

The analysis can be reproduced by:

1. Opening `hotdog_data_parkhurst.xlsx`.
2. Excluding name fields from statistical analysis.
3. Calculating overall Yes and No counts.
4. Creating the academic-year summary table.
5. Creating Plot 1 and Plot 2 in Excel.
6. Calculating the sample proportion and 95% confidence interval.
7. Interpreting the findings while considering the convenience sampling method.

---

# Files

- `hotdog_data_parkhurst.xlsx` — Original survey dataset
- `README.md` — Project documentation
- `images/overall_responses.png` — Plot 1: Overall responses
- `images/responses_by_year.png` — Plot 2: Responses by academic year


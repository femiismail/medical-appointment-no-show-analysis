# Medical Appointment No-Show Analysis

**Tools:** Google Sheets | **Project type:** Exploratory Data Analysis, Data Cleaning, Dashboard Development

[https://docs.google.com/spreadsheets/d/1enPJjsOmjqEk92vnQ-ezKi1OMBHFSSeP-JDz2fY9-YM/edit?usp=sharing]

## Project Overview

Missed medical appointments can disrupt clinic schedules, waste healthcare resources, and reduce access to care for other patients. Understanding the patterns associated with missed appointments can help healthcare providers identify areas for improvement.

In this project, I analysed 110,527 medical appointments using Google Sheets. I cleaned and prepared the data, created calculated fields, analysed appointment outcomes using pivot tables, and built a dashboard to communicate the findings.

The goal was to identify patterns in attendance and recommend practical interventions for further investigation.

## Business Questions

- What proportion of scheduled appointments are missed?
- Which age groups have the highest no-show rates?
- How do no-show rates vary by weekday?
- Is a longer waiting period associated with a higher no-show rate?
- How do no-show rates differ by SMS reminder status across waiting periods?

## Tools and Methodology

**Tool:** Google Sheets

The analysis involved:

- Preparing date fields and calculating waiting days.
- Creating an attendance status and a binary `No_Show_Flag`, where 1 represents a missed appointment and 0 represents an attended appointment.
- Grouping patients into age categories and appointments into waiting-period categories.
- Using pivot tables to compare no-show rates across different groups.
- Creating charts and metric cards for an interactive dashboard.

The no-show rate was calculated as the average of `No_Show_Flag`, allowing comparisons between groups of different sizes.

## Key Findings

### Overall Attendance

| Metric | Result |
|---|---:|
| Total appointments | 110,527 |
| Missed appointments | 22,319 |
| No-show rate | 20.19% |
| Attendance rate | 79.81% |

Approximately one in five appointments was missed.

### No-Show Rate by Age Group

| Age group | No-show rate |
|---|---:|
| 0–17 | 21.90% |
| 18–34 | 23.98% |
| 35–49 | 20.54% |
| 50–64 | 16.72% |
| 65+ | 15.50% |

The 18–34 age group recorded the highest no-show rate at 23.98%, while patients aged 65 and above recorded the lowest at 15.50%.

This suggests that attendance barriers may differ across age groups and warrants further investigation.

### No-Show Rate by Weekday

| Weekday | No-show rate |
|---|---:|
| Monday | 20.65% |
| Tuesday | 20.09% |
| Wednesday | 19.69% |
| Thursday | 19.35% |
| Friday | 21.23% |
| Saturday | 23.08% |

Saturday had the highest observed no-show rate at 23.08%, while Thursday had the lowest at 19.35%. Sunday was absent from the analysis, and the reason has not been independently verified.

### No-Show Rate by Waiting Period

| Waiting period | No-show rate |
|---|---:|
| 0–2 days | 8.93% |
| 3–7 days | 24.98% |
| 8–14 days | 30.47% |
| 15+ days | 32.74% |

The observed rates increased across the longer waiting-period categories. However, the date calculations and group assignments require final validation, particularly for the 0–2-day category, before this pattern is treated as a definitive finding.

### SMS Reminders and Waiting Periods

| Waiting period | No SMS | SMS received |
|---|---:|---:|
| 0–2 days | 8.92% | No records |
| 3–7 days | 26.59% | 23.76% |
| 8–14 days | 33.76% | 28.11% |
| 15+ days | 37.11% | 29.95% |

Among appointments in the 3–7, 8–14, and 15+ day groups, the observed no-show rates were lower among patients who received SMS reminders.

This is an association, not proof that SMS reminders caused better attendance. The 0–2-day group had no records with SMS reminders, preventing a comparison for that category.

## Recommendations

1. **Investigate attendance barriers among younger adults.** Explore whether work commitments, transportation, appointment timing, or other factors may contribute to their higher observed no-show rate.
2. **Evaluate SMS reminders.** Consider a controlled pilot to measure whether reminder interventions improve attendance.
3. **Investigate longer waiting periods.** Test appointment reconfirmation or reminder schedules for patients with longer waits.
4. **Review Saturday appointment patterns.** Examine scheduling practices and appointment characteristics to understand the higher observed rate.
5. **Monitor attendance over time.** Track no-show rates across patient groups and appointment characteristics to assess the impact of future interventions.

## Limitations

- The analysis identifies associations and does not establish causation.
- Six records with negative waiting days were excluded from the cleaned analysis; the exclusions should be documented.
- An invalid age value of -1 was identified and treated as missing for age-specific analysis.
- Sunday was absent from the weekday results, and the reason was not independently verified.
- Waiting-period calculations and group assignments require final validation.
- Findings from this dataset may not generalise to all healthcare facilities.

## Conclusion

This project used Google Sheets to analyse medical appointment attendance and identify patterns across age groups, weekdays, waiting periods, and SMS reminder status.

The findings highlight areas for further investigation and demonstrate how data cleaning, exploratory analysis, pivot tables, and dashboard visualisation can support practical, data-informed decisions.

## Skills Demonstrated

- Data cleaning and preparation
- Date handling and calculated columns
- Data quality checks
- Pivot table analysis
- Rate and percentage calculations
- Exploratory data analysis
- Dashboard development
- Insight generation and business recommendations

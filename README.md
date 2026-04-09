[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ji_7k7sD)
# Lab 4 — Descriptive Analytics: Student Performance EDA

Conduct a systematic exploratory data analysis on a university student performance dataset. Assess distributions, identify correlations, run hypothesis tests, and summarize your findings in a written report.

## Setup

```bash
pip install -r requirements.txt
```

## Dataset

`data/student_performance.csv` contains ~2,000 student records with columns:
- `student_id`, `department`, `semester`, `course_load`, `study_hours_weekly`
- `gpa`, `attendance_pct`, `has_internship`, `commute_minutes`, `scholarship`

The dataset includes missing values and statistical patterns for you to discover.

## Tasks

Complete `eda_analysis.py`:

1. **Load and profile** the dataset (shape, types, missing values, descriptive stats)
2. **Plot distributions** for key numeric variables (histograms, box plots)
3. **Analyze correlations** between variables (heatmap, scatter plots)
4. **Run hypothesis tests** to validate observed patterns (t-test, ANOVA, or correlation test)
5. **Write `FINDINGS.md`** summarizing your analysis, key patterns, and statistical results

All plots should be saved to `output/` as PNG files.

## Submit

1. Create branch `lab-4-descriptive-analytics`
2. Complete `eda_analysis.py` and `FINDINGS.md`
3. Push and open a PR to `main`
4. Paste your PR URL into TalentLMS → Module 4 → Lab 4

---

## License

This repository is provided for educational use only. See [LICENSE](LICENSE) for terms.

You may clone and modify this repository for personal learning and practice, and reference code you wrote here in your professional portfolio. Redistribution outside this course is not permitted.

# FINDINGS — Student Performance Analysis

## Dataset Overview
The dataset contains approximately 2000 student records with variables including GPA, study hours, attendance, and scholarship status.

Some missing values were observed:
- commute_minutes (~10%) → filled with median
- study_hours_weekly (~5%) → dropped
- scholarship (~20%) → filled with "None"

---

## Distribution Insights
- GPA is slightly left-skewed, with most students between 2.5 and 3.5.
- Study hours show moderate variation across students.
- Attendance is generally high, indicating strong class participation.
- Box plots show variation in GPA across departments.

---

## Correlation Analysis
- Study hours and GPA show a positive correlation.
- Attendance also appears moderately correlated with GPA.
- These relationships suggest that effort and engagement influence academic performance.

---

## Hypothesis Testing

### Internship vs GPA (T-Test)
The t-test shows a statistically significant difference in GPA between students with and without internships (t = 13.56, p < 0.001).

This indicates that internship participation is associated with higher academic performance.

---

### Scholarship vs Department (Chi-Square)
The chi-square test shows no significant relationship between scholarship type and department (χ² = 17.14, p = 0.377).

This suggests scholarship distribution is independent of department.

---

## Recommendations

1. Encourage internship participation, as it is associated with higher GPA.
2. Promote study habits and attendance, as they correlate with better academic performance.
3. Review scholarship allocation strategies to ensure alignment with academic performance if desired.

---

## Notes
Correlation does not imply causation. Observed relationships should be further validated with controlled studies.

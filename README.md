# Examing Relationship Between Financial Aid and Timely Graduation at UT Austin

A chi-square test of independence examining whether financial aid status is associated with on-time graduation rates among first-time, full-time bachelor's degree-seeking students who entered UT Austin in 2018.

---

## Overview

This project analyzes a random sample of UT Austin students to determine whether receiving a Pell Grant, a Direct Subsidized Loan, or no federal financial aid is associated with graduating within 150% of normal time (6 years). The analysis was conducted in Excel using a contingency table and chi-square test.

---

## Dataset

- **Source:** IPEDS publicly avaliable data (file name: gr2024_pell_ssl.xlsx)
- **Population:** Full-time, first-time bachelor's degree-seeking students who entered UT Austin in 2018
- **Sample size:** 180 students (60 per financial aid group, randomly sampled)
- **Variables:**
  - `Graduated within 150% of normal time` — Yes or No
  - `Financial Aid Status` — Pell Grant, Subsidized Loan, or None

> **Note:** Students who withdrew due to death, permanent disability, military service, federal volunteer programs, or official church missions are excluded from all counts per federal reporting standards.

---

## Methodology

### 1. Data Reconstruction
Using counts from the source data set, a new table was constructed to unaggregate counts and focus on UT Austin's cohort.

### 2. Sampling
Students were randomly assigned a generated number and sorted within each financial aid group. 60 students were selected from each group (Pell Grant, Subsidized Loan, None) for a balanced sample of 180 total.

### 3. Contingency Table

Observed counts of graduation outcomes by financial aid group:

|  | None | Pell Grant | Subsidized Loan | Total |
|--|------|------------|-----------------|-------|
| **Did not graduate** | 6 | 11 | 10 | 27 |
| **Graduated** | 54 | 49 | 50 | 153 |
| **Total** | 60 | 60 | 60 | 180 |

### 3. Chi-Square Test of Independence
Expected counts were calculated under the null hypothesis of no association between financial aid status and graduation outcome. Cell-level chi-square contributions were computed and summed to produce the test statistic.

| Metric | Value |
|--------|-------|
| **Chi-Square Statistic** | 1.830 |
| **Degrees of Freedom** | 2 |
| **Critical Value (α = 0.05)** | 5.991 |
| **P-Value** | 0.401 |

### 4. Visualization
Using the sample a 100% stacked bar chart was created to compare graduation outcomes across financial aid status.

<img width="514" height="307" alt="image" src="https://github.com/user-attachments/assets/7bc526d7-6e8f-4627-8289-7dc9819536ce" />

### 5. Conclusion
Since the chi-square statistic (1.830) is well below the critical value (5.991) and the p-value (0.401) far exceeds the 0.05 significance threshold, we **fail to reject the null hypothesis**. There is no statistically significant association between financial aid status and graduating within 150% of normal time in this sample.

---

## Files

```
├── Final_Stats_Project_Data.xlsx    # Full dataset, calculations, and chi-square test
│   ├── Key                          # Variable definitions and exclusion criteria
│   ├── UT Austin Sorted Data        # Randomly sampled student records
│   └── Calculations                 # Contingency table and chi-square analysis
├── gr2024_pell_ssl.xlsx             # Full aggregated dataset from IPEDS
└── README.md
```

---

## Tools Used

- Microsoft Excel — random sampling, pivot tables, chi-square calculations

---

## Author

Built as part of a statistics course portfolio, in collaboration with Sadiqa Islam and Xymmena De La Pena

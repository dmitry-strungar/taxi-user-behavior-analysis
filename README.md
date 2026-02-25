# Taxi User Behavior Analysis

## 📌 Project Overview

This project analyzes user behavior in a taxi service platform, focusing on trip distance preferences across different service classes.

The goal is to investigate whether users tend to choose Comfort class over Economy for longer trips.

---

## 🎯 Business Question

Do users prefer Comfort class instead of Economy for long-distance trips?

---

## 🔬 Hypothesis

- **H0 (Null Hypothesis):** There is no difference in trip distance distributions between Economy and Comfort classes.
- **H1 (Alternative Hypothesis):** Comfort trips tend to have longer distances than Economy trips.

---

## 📊 Methodology

1. Exploratory Data Analysis (EDA)
   - Dataset structure inspection
   - Descriptive statistics
   - Class distribution analysis

2. Distribution Visualization
   - Kernel Density Estimation (KDE)
   - Boxplot comparison

3. Normality Testing
   - Shapiro–Wilk test (sampling approach)

4. Statistical Testing
   - Mann–Whitney U test (non-parametric)

---

## 📈 Key Findings

- Distance distributions are not normally distributed.
- Comfort trips show a higher concentration of longer distances.
- Mann–Whitney U test indicates statistically significant difference (p < 0.05).
- Trip distance is associated with taxi class choice.

---

## 💼 Business Implication

Users are more likely to choose Comfort class for longer trips.

The company may:
- Promote Comfort class for long-distance routes
- Optimize pricing strategy for extended trips
- Personalize recommendations based on trip distance patterns

---

## 🛠 Tools Used

- Python
- Pandas
- NumPy
- Seaborn / Matplotlib
- SciPy (statistical testing)

---

## ⚠️ Limitations

- The analysis does not control for time-related factors (seasonality).
- Trip purpose is unknown (business vs personal).
- Distance alone may not fully explain class choice.
- The dataset structure may not represent the full population of users.

---

# Taxi User Behavior Analysis

## Project Overview

This project analyzes user behavior in a taxi service platform, focusing on trip distance preferences across different service classes.

The goal is to investigate whether users tend to choose Comfort class over Economy for longer trips.

---

## Business Question

Do users prefer Comfort class instead of Economy for long-distance trips?

---

## Hypothesis

- **H0 (Null Hypothesis):** There is no difference in trip distance distributions between Economy and Comfort classes.
- **H1 (Alternative Hypothesis):** Comfort trips tend to have longer distances than Economy trips.

---

## Methodology

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

## Key Insights

### Distribution Analysis

Distance distributions for Economy and Comfort trips are right-skewed and non-normal.  
This justifies the use of a non-parametric statistical test (Mann–Whitney U test).


### Median Comparison

- Economy median distance: **23.80 km**
- Comfort median distance: **28.08 km**
- Absolute difference: **+4.28 km**
- Relative increase: **+17.98%**

A typical Comfort trip is nearly 18% longer than a typical Economy trip.


### Mean Comparison

- Economy mean distance: **26.28 km**
- Comfort mean distance: **29.76 km**
- Mean difference: **+3.48 km**
- Relative mean increase: **+13.22%**

The shift is consistent across both medians and means, indicating a stable structural difference.


### Mann–Whitney U Test Results

- U-statistic: **139702**
- p-value: **0.000642**

Since p-value < 0.05, the null hypothesis is rejected.

Comfort distance distribution is statistically significantly shifted to the right compared to Economy.


### Effect Size (Probability of Superiority)

Probability that a randomly selected Comfort trip is longer than a randomly selected Economy trip:

**0.559**

This means that in **55.9% of cases**, a Comfort trip is longer than an Economy trip.

This represents a real behavioral shift, not merely statistical significance.


### Robustness Check

After removing the top 1% of extreme distances:

- p-value: **0.000521**
- Probability of Superiority: **0.560**

The effect remains statistically significant and practically unchanged.

This confirms that the observed difference is not driven by extreme long-distance outliers.


## Behavioral Interpretation

1. Users systematically select Comfort for longer trips.
2. A 4.28 km median difference represents economically meaningful segmentation.
3. Probability of superiority above 0.5 confirms a genuine distribution shift.
4. The effect remains stable after trimming extreme values.


## Implications

The findings suggest:

- Trip distance is a statistically significant determinant of taxi class choice.
- Price sensitivity decreases as trip distance increases.
- Comfort can be strategically promoted for longer routes.
- Distance can serve as a predictive feature in class selection models.
- Dynamic upselling of Comfort for trips above Economy median distance may increase revenue.

The study identifies a statistically significant behavioral pattern.  
However, it remains observational and does not establish causality.

---
## Business Value
Identifies behavioral differences between Economy and Comfort segments  
Confirms statistical significance of distance differences  
Supports pricing and service positioning strategy  
Helps optimize segmentation and product offering  

## Stakeholders
Product Team  
Pricing Analysts  
Marketing Team  
Data Analysts  

---

## Business Implication

Users are more likely to choose Comfort class for longer trips.

The company may:
- Promote Comfort class for long-distance routes
- Optimize pricing strategy for extended trips
- Personalize recommendations based on trip distance patterns

---

## Tools Used

- Python
- Pandas
- NumPy
- Seaborn / Matplotlib
- SciPy (statistical testing)

---

## Limitations

- The analysis does not control for time-related factors (seasonality).
- Trip purpose is unknown (business vs personal).
- Distance alone may not fully explain class choice.
- The dataset structure may not represent the full population of users.

---

# Applied Metrics – Problem Set 04  
## Matching Methods in Observational Studies

This repository contains the solution to **Problem Set 04** of the *Applied Metrics (MSc)* course (Spring 2025).  
The project applies a wide range of **matching and weighting methods** to estimate causal effects in an observational setting using employee-level data.

---

## Files

- **applied-metrics-matching-causal-inference.md**  
  Main analysis file containing all conceptual answers, empirical results, tables, and interpretations.

- **ps4.pdf**  
  Official problem set description.

---

## Dataset

- **Employee_Performance.csv**
- Observational employee-level dataset including:
  - Demographics (age, gender, education)
  - Job characteristics (department, job title, projects, overtime)
  - Training participation and intensity
  - Promotions
  - Salary, performance, satisfaction, resignation status
  - Team-level training measures

---

## Methods Covered

This project implements and compares the following causal inference techniques:

- Propensity Score Matching (PSM)
- Nearest Neighbor Matching (NNM)
- Mahalanobis Distance Matching
- Exact Matching
- Inverse Probability Weighting (IPW)
- Stabilized Inverse Probability Weighting (SIPW)
- Multinomial IPW for multi-valued treatments

---

## Project Structure and Analysis

### Section 1 – Conceptual Foundations
- Threats to causal identification in observational studies
- Conditional Independence Assumption (CIA)
- Overlap and common support
- Balance diagnostics
- Curse of dimensionality in exact matching
- Comparison of ATE, ATT, and ATU
- IPW vs SIPW and weight instability

---

### Section 2 – Effect of Training on Salary (Binary Treatment)

- Estimation of propensity scores using logistic regression
- Visualization of propensity score distributions
- 1-to-1 nearest neighbor matching with caliper
- Balance assessment using:
  - Standardized Mean Differences (SMD)
  - Graphical diagnostics (PS histograms, love plots)
- Estimation of ATT using:
  - Mean differences
  - OLS regression on matched samples
- Comparison with full-sample regression
- Analysis of training intensity and diminishing returns

---

### Section 3 – Remote Work Frequency  
**Nearest Neighbor vs Mahalanobis Matching**

- Binary treatment defined using top and bottom quartiles
- Propensity score estimation and balance diagnostics
- Comparison of:
  - Nearest Neighbor Matching
  - Mahalanobis Distance Matching
- Estimation of treatment effects on:
  - Performance score (OLS)
  - Resignation probability (Logit)
- Method comparison and interpretation

---

### Section 4 – Multi-level Promotions  
**Exact Matching, IPW, and SIPW**

- Exact matching across three promotion levels
- Trade-off between match strictness and sample size
- Pairwise IPW and SIPW estimation
- Multinomial logistic regression for treatment assignment
- Multinomial IPW and SIPW weighted regressions
- Comparison across estimation strategies

---

### Section 5 – Team Training Spillovers

- Analysis restricted to untrained employees
- Definition of team-level treatment
- IPW estimation of spillover effects
- Logistic regression for team treatment assignment
- Weighted OLS estimation of peer effects on performance
- Discussion of policy implications for HR training design

---

## Key Concepts Demonstrated

- Selection on observables
- Balance vs overlap
- Bias–variance trade-off
- Weight instability and stabilization
- Multi-valued treatments
- Spillover and peer effects

---

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>

# Matching and Weighting Estimators for Causal Effects in Observational Data

A comparison of **matching and inverse-probability-weighting estimators** for causal effects without random assignment. The application is employee-level data: the effect of training participation on salary and performance, extended to multi-valued treatment intensities.

## Methods implemented

| Family | Estimators |
|---|---|
| **Matching** | Propensity-score matching, nearest-neighbour matching, Mahalanobis-distance matching, exact matching |
| **Weighting** | Inverse probability weighting (IPW), stabilised IPW, multinomial IPW for multi-valued treatments |
| **Estimands** | ATE, ATT and ATU, and the conditions under which they differ |

## Diagnostics

- Overlap and common-support checks on the estimated propensity score
- Covariate-balance tables before and after matching
- Weight-instability analysis (IPW vs stabilised IPW)
- The curse of dimensionality in exact matching

The write-up also discusses the identifying assumptions (conditional independence and overlap) and the threats to identification in observational settings.

## Repository structure

```
analysis.md   # full analysis: code, balance tables, estimates and interpretation
```

Figures and tables are generated when the code is run; the figure files themselves are not stored in the repository.

## Reproducing

```bash
pip install pandas numpy scikit-learn statsmodels scipy matplotlib seaborn
```

The analysis uses an employee-performance dataset (`Employee_Performance.csv`) with demographics, job characteristics, training participation and outcomes.

## Context

Developed during the MSc in Economics at Sharif University of Technology (Applied Econometrics, Spring 2025).

---
**Shayan Pourmasoomi** · MSc Economics, Sharif University of Technology · [LinkedIn](https://www.linkedin.com/in/shayan-pourmasoomi-8b6206389)

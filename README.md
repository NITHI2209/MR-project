# Report on Multiple Linear Regression Analysis

**Objective:** To examine the impact of Sleep Hours, Hours Studied, Sample Question Papers Practiced and Previous Scores on the Performance Index.

**H0:** Sleep Hours, Hours Studied, Sample Question Papers Practiced and Previous Scores do not influence the Performance Index.

**H1:** Sleep Hours, Hours Studied, Sample Question Papers Practiced and Previous Scores influence the Performance Index.

## Output

### 1. Model Fit Measures

| Model | R     | R²    | Adjusted R² |
|-------|-------|-------|-------------|
| 1     | 0.994 | 0.988 | 0.988       |

*Note. Models estimated using sample size of N = 10,000.*

- R = 0.994 indicates a very strong positive relationship between actual and predicted Performance Index.
- R² = 0.988: 98.8% of the variation in Performance Index is explained by the four predictors together.
- Adjusted R² = 0.988 confirms very high explanatory power after adjusting for the number of predictors.
- The model is significant overall, F(4, 9,995) = 214,748.4, p < .001; H0 is rejected.

### 2. Model Coefficients – Performance Index

| Predictor                        | Estimate | SE     | t       | p       |
|----------------------------------|----------|--------|---------|---------|
| Intercept                        | -33.764  | 0.1268 | -266.19 | < .001  |
| Sleep Hours                      | 0.476    | 0.0122 | 39.19   | < .001  |
| Hours Studied                    | 2.853    | 0.0080 | 358.40  | < .001  |
| Sample Question Papers Practiced | 0.195    | 0.0072 | 27.15   | < .001  |
| Previous Scores                  | 1.019    | 0.0012 | 857.02  | < .001  |

- Previous Scores (β = 1.019, p < .001) has the strongest positive effect: each extra point adds about 1.02 to the Performance Index.
- Hours Studied (β = 2.853, p < .001): each extra hour adds about 2.85 points.
- Sleep Hours (β = 0.476) and Sample Question Papers Practiced (β = 0.195) also have significant but smaller positive effects (both p < .001).
- Therefore, all four variables are significant predictors of Performance Index.

## Assumption Checks

### 3. Normality of Residuals (Q–Q Plot)

The standardized residuals lie very close to the reference line, with only slight deviation at the extreme tails (skewness = 0.009, excess kurtosis = 0.067); residuals are approximately normal.

### Normality Test (Shapiro-Wilk)

| Statistic | p     |
|-----------|-------|
| 0.9999    | 0.811 |

*Note. With N = 10,000 the Shapiro-Wilk test is only approximate; the Q–Q plot is the more reliable guide.*

Maximum Cook's Distance = 0.002, far below the threshold of 1. Therefore, no observation is highly influential.

### Collinearity Statistics

| Predictor                        | VIF  | Tolerance |
|----------------------------------|------|-----------|
| Sleep Hours                      | 1.00 | 1.000     |
| Hours Studied                    | 1.00 | 1.000     |
| Sample Question Papers Practiced | 1.00 | 1.000     |
| Previous Scores                  | 1.00 | 1.000     |

All VIF values (≈ 1.00) are well below 5 and all Tolerance values (≈ 1.000) are above 0.20, so there is no multicollinearity. Therefore, the four predictors can be reliably included together in the model.

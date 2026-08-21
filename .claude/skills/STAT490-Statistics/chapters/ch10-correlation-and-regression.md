# Chapter 10: Correlation and Regression

## Core Idea

For paired quantitative data: draw a scatterplot; judge direction, form, strength, spread, clusters, and outliers; quantify linear association with `r`; fit and diagnose a least-squares line; measure `r^2` and prediction uncertainty; and extend only when warranted. Association and prediction are not causation: lurking variables, aggregation, and shared time trends can mislead.

## Frameworks Introduced (exact named concepts, when to use, how)

1. **Scatterplot-first workflow.** Plot `(x_i, y_i)` before calculating, with explanatory `x` horizontal and response `y` vertical. Read direction, form, strength, spread, clusters, and outliers. A curve, cluster, or funnel changes the analysis; a curve is evidence against a straight-line method, not proof of no relationship.

2. **Linear Correlation Coefficient `r` (Pearson product moment correlation coefficient).** Use `r` for the direction and strength of a linear association in paired quantitative sample data:

   ```text
                 n Sum(xy) - Sum(x)Sum(y)
   r = ------------------------------------------------------------
       sqrt([n Sum(x^2) - (Sum(x))^2][n Sum(y^2) - (Sum(y))^2])
   ```

   `-1 <= r <= 1`; the population parameter is `rho`. Units and swapping x and y do not change `r`, but one influential outlier can change it greatly. A near-zero `r` rules out only a linear pattern. For inference, use a simple random sample of paired quantitative observations, an approximately linear plot, and no unexamined outliers; the formal model treats the pair as bivariate normal.

3. **Test for correlation and causality.** For a two-sided test, use `H0: rho = 0` and `H1: rho != 0`. Software uses

   ```text
              r
   t = ----------------------,     df = n - 2
       sqrt((1 - r^2)/(n - 2)).
   ```

   Reject when the P-value is at most `alpha` (or compare `|r|` with the critical value). A small P-value supports a nonzero linear association, not causation, practical importance, or a nonlinear relationship. Check lurking variables, group averages, and time order; causal claims require design and subject-matter reasoning.

4. **Regression equation and least squares.** After the plot supports a line, fit

   ```text
   y_hat = b0 + b1x,       b1 = r(s_y/s_x),       b0 = y_bar - b1x_bar.
   ```

   `b1` is the predicted change in `y` for a one-unit increase in `x`; it is not proof that manipulating `x` causes that change. For observation `(x, y)`, `e = y - y_hat`. The least-squares line minimizes `Sum(e^2) = Sum(y - y_hat)^2` among all straight lines. The model requires random quantitative data, an approximately straight mean relationship, approximately normal y-values at fixed x, a common standard deviation, independent errors, and no unexamined influential points.

5. **Residual diagnostics and standard error of estimate.** Plot `(x, e)` against zero. Residuals should be random, even-width noise: curvature suggests the wrong form, a funnel unequal variance, and time or cluster patterns dependence or collection problems. Use a histogram or normal quantile plot for approximate normality. An outlier is unusual; an influential point changes the line when removed, especially when far horizontally from `x_bar`. Investigate and compare refits; remove only known errors. Typical vertical scatter is

   ```text
              sqrt(Sum(y - y_hat)^2)
   s_e = ------------------------------.
                    sqrt(n - 2)
   ```

6. **Coefficient of determination `r^2`.** In simple regression,

   ```text
   r^2 = explained variation / total variation.
   ```

   Thus `r^2 = 0.76` means the fitted linear relationship explains an estimated 76% of sample variation in `y`. It does not mean that `x` causes 76% of changes, nor does it guarantee precise individual predictions.

7. **Prediction interval and extrapolation.** For a defensible `x0`, predict `y_hat = b0 + b1x0`. If the line is not useful, use `y_bar` as the simple fallback, regardless of x. For an individual future response, use

   ```text
   y_hat +/- E,
   E = t_(alpha/2,n-2) s_e
       sqrt[1 + 1/n + n(x0 - x_bar)^2 /
                    (n Sum(x^2) - (Sum(x))^2)].
   ```

   The interval widens with residual scatter, small `n`, and distance from `x_bar`. A confidence interval for the mean response omits the leading `1`; it is narrower and answers a different question. Predicting beyond the observed x-range is **extrapolation** and can fail even when the line fits inside the data.

8. **Multiple regression.** With two or more predictors, use `y_hat = b0 + b1x1 + ... + bkxk`. Each coefficient changes predicted `y` per predictor unit with others fixed. Retain random data, linearity, approximately normal and equal-variance errors, and independence. `R^2` measures response variation explained by all predictors. Test `H0: beta1 = ... = betak = 0`; a small P-value supports predictive usefulness, not causality. Ordinary `R^2` cannot decrease when predictors are added, so compare models with

   ```text
   adjusted R^2 = 1 - [(n - 1)/(n - (k + 1))](1 - R^2).
   ```

   Prefer useful variables, a set, meaningful adjusted-`R^2` improvement, relevant tests, and low redundancy. Individual coefficient tests use `t = b_j/s_bj` with `df = n - (k + 1)`. Highly correlated predictors destabilize coefficients. Code a two-category predictor as a dummy `0/1`; a binary response calls for logistic regression, `ln[p/(1 - p)] = beta0 + beta1x1 + ... + betakxk`, not ordinary linear regression.

9. **Mathematical model selection.** Use the plot to choose linear `y = a + bx`, quadratic `y = ax^2 + bx + c`, logarithmic `y = a + b ln(x)`, exponential `y = ab^x`, or power `y = ax^b`. Transform when appropriate, then compare residuals, residual sum of squares, and `R^2` (or adjusted `R^2`). Reject implausible shapes or predictions; a high fit statistic cannot replace diagnostics or extrapolation caution.

## Key Concepts (5-10)

1. `r` summarizes one linear feature of a map; the scatterplot remains primary.
2. Linear association is narrower than association, and association is not causation.
3. The regression line estimates typical `y`; the residual is the individual departure, and least squares minimizes total squared vertical error.
4. `r^2` describes fit, `s_e` residual spread, and a prediction interval individual uncertainty.
5. Residual structure and added predictors reveal why diagnostics, adjusted fit, and simplicity matter.

## Mental Models

- **Map before measure:** inspect the scatterplot before trusting a number.
- **Compass, not cause detector:** the sign shows how variables move together, not why.
- **Line plus noise:** `y_hat` is systematic prediction; `e = y - y_hat` is case-specific departure.
- **Distance costs precision:** uncertainty grows with residual scatter, small samples, and distance from `x_bar`.
- **Residuals are feedback:** random residuals support the form; patterns require revision.

## Anti-patterns

- Computing `r` without a scatterplot or using it to detect every relationship.
- Treating significance, a high `r^2`, or a slope as causal evidence.
- Ignoring aggregation, time dependence, clusters, outliers, or influence; deleting a legitimate unusual point without sensitivity analysis.
- Fitting through curvature or a funnel, or reporting a line without residual diagnostics.
- Extrapolating far beyond the x-range or reporting only a point estimate for an individual.
- Adding predictors merely because ordinary `R^2` rises, using linear regression for a binary response, or rounding intermediate calculations.

## Worked Example (study depth, reconstruct a scatterplot/correlation/regression prediction)

For pizza cost `x` and subway fare `y`, use `(0.15,0.15)`, `(0.35,0.35)`, `(1.00,1.00)`, `(1.25,1.35)`, `(1.75,1.50)`, and `(2.00,2.00)`. Plot pizza cost horizontally first. The points are strongly uphill and roughly straight; `(1.75,1.50)` is below trend but not an obvious error. This supports investigating linear association, not causation.

For `n = 6`, `Sum(x) = 6.50`, `Sum(y) = 6.35`, `Sum(x^2) = 9.77`, `Sum(y^2) = 9.2175`, and `Sum(xy) = 9.4575`. The correlation formula gives `r = 0.988`. With `alpha = 0.05`, the two-sided critical value is about `+/-0.811`; reject `H0: rho = 0` under the stated conditions. Here `r^2 = 0.976`, so the line explains about 97.6% of sample fare variation, not 97.6% of causal change.

Using `x_bar = 1.083333` and `y_bar = 1.058333`,

```text
b1 = r(s_y/s_x) = 0.945,     b0 = y_bar - b1x_bar = 0.0346
y_hat = 0.0346 + 0.945x.
```

At `x = 0.15`, `y_hat = 0.17635` and `e = 0.15 - 0.17635 = -0.02635`, so the line overpredicts slightly. For a pizza cost of `$2.25`, `y_hat = 2.16`. With `s_e = 0.122987` and `t_(0.025,4) = 2.776`,

```text
E = 2.776(0.122987) sqrt[1 + 1/6 +
    6(2.25 - 1.083333)^2/(6(9.77) - 6.50^2)] = 0.441.
```

The 95% individual prediction interval is `2.16 +/- 0.441`, or `1.72 <= y <= 2.60`. Because `$2.25` exceeds the observed maximum `$2.00`, this is extrapolation and deserves caution. If diagnostics failed, use the fallback `y_bar = $1.06` rather than the line.

## Key Takeaways (3-7 actionable)

1. Plot first; identify form, spread, clusters, and influence.
2. Use `r` only for linear association and state that it is not causal evidence.
3. Fit a line only after its assumptions and residuals are defensible; use `r^2`, `s_e`, and intervals to report uncertainty.
4. Avoid extrapolation and use `y_bar` when a line is not useful.
5. For multiple or nonlinear models, prioritize diagnostics, adjusted fit, practicality, and realistic predictions.

## Connects To

- **Matched pairs:** Earlier methods study mean differences; this chapter studies association, line fitting, and prediction.
- **Exploratory graphics:** Scatterplots and residual plots make calculations interpretable.
- **Normal distributions and t procedures:** These support correlation tests and prediction intervals.
- **Variation, causality, and modeling:** Explained variation connects to interval logic; design addresses causation; multiple and nonlinear models extend fit-diagnose-predict with greater validation needs.

# Chapter 15: Stage 4 - Measures of Association

## Core Idea

Association analysis answers whether variables occur together, how strongly and in what direction they move, what shape their relationship takes, and whether one variable can predict another. Correlation is symmetric and describes linear association; regression assigns predictor and dependent roles and produces an equation for prediction. Neither correlation nor regression, by itself, establishes causation. Visual inspection, measurement level, distributional assumptions, subgroup structure, statistical significance, practical significance, and the size of common variance must all be considered before a coefficient becomes an insight.

## Frameworks Introduced

**Relational hypothesis.** State that variables occur together in a specified manner without implying that one causes the other. Use this frame when the research question asks whether two or more variables are related, rather than whether a treatment produces an outcome.

**Bivariate correlation analysis.** Use for two continuous variables measured at the interval or ratio level. The coefficient treats X and Y symmetrically, so `r_xy` and `r_yx` have the same interpretation. It summarizes direction and magnitude of a linear relationship but does not select an independent and dependent variable.

**Pearson's Product Moment Coefficient r.** Use Pearson's r for a linearly related pair of continuous interval-ratio variables from a random sample with a bivariate normal distribution. The coefficient ranges from -1 through 0 to +1. The sign describes direction; the absolute value describes magnitude.

**Scatterplots for exploring relationships.** Plot paired observations before calculating or interpreting r. Use the plot to inspect direction, linearity, curvature, clusters, influential points, constant X values, and outliers. Summary statistics can be identical for data sets with very different structures.

**Coefficient of determination r^2.** Square the correlation to summarize the proportion of common or shared variance in a linear relationship. In regression it is the proportion of Y variability explained by the least-squares line based on X.

**Simple linear regression.** Use when X is an independent predictor and Y is a dependent criterion and the aim includes estimation or prediction. The model is `Y_i = beta_0 + beta_1 X_i + error_i`. The slope is the expected change in Y for a one-unit change in X; the intercept is the estimated Y when X is zero.

**Method of Least Squares.** Select the line that minimizes the sum of squared vertical prediction errors. Compute the slope and intercept from the observed X-Y pairs, then use the equation to draw the line and predict Y.

**Residual diagnostics and prediction/confidence bands.** A residual is `Y_i - Y-hat_i`. Standardized residuals should be roughly between -2 and +2, randomly distributed around zero, and pattern-free. Use diagnostic plots and checks for normality, linearity, equal variance, and independence. Point prediction bands are wider than confidence bands for a mean response, and both widen as X moves farther from its mean.

**Goodness of fit.** Test whether the slope is zero using a t-test with `n - 2` degrees of freedom. In bivariate regression the model F test gives the same decision because `t^2 = F`. Test and interpret r^2 as evidence that the regression improves prediction over using the mean of Y.

**Chi-square-based measures of association.** Use phi for a 2-by-2 nominal table, Cramer's V for tables of any shape, and the contingency coefficient C when flexible table and distribution conditions are important. These describe strength, not direction or causation.

**Proportional Reduction in Error (PRE).** Use lambda and Goodman and Kruskal's tau when the question is how much knowledge of one nominal variable improves prediction of another. Lambda is asymmetric or symmetric depending on the direction of prediction; tau emphasizes table marginals.

**Concordant-discordant pair framework.** Use gamma, Kendall's tau b and tau c, and Somers's d for ordered data. Let P be concordant pairs and Q be discordant pairs. The balance and difference between P and Q determine direction and strength; the variants handle ties, table dimensions, and the direction of the dependent variable differently.

**Spearman's rho.** Rank two ordered variables and calculate a rank correlation. Use it when data are ordinal or when continuous values contain outliers, transformations, or other abnormalities that make raw-score Pearson correlation unsuitable. Assign average ranks to ties and consider a tie correction when ties are substantial.

## Key Concepts

### Association is not causation

A correlation can be consistent with several explanations: X causes Y; Y causes X; a third variable activates both; or X and Y influence each other reciprocally. Ex post facto association studies rarely have the design strength to distinguish these explanations. Experimental control can provide more rigorous causal evidence.

Use a relational hypothesis such as "higher advertising expenditure is associated with higher sales," not a causal claim unless the design supports it. A statistically significant coefficient is not automatically practically meaningful, and a coefficient's magnitude is not remarkable solely because a large sample makes its p value small.

### Pearson's r: direction, magnitude, and shape

Pearson's r ranges from -1 to +1. A positive sign means that large values of one variable tend to accompany large values of the other; a negative sign means that large values of one tend to accompany small values of the other. The signs of `+.40` and `-.40` indicate opposite directions, but their magnitudes are the same. A coefficient near zero means no linear relationship, not necessarily no relationship of any form.

Pearson's r is a measure of linear association. A curved, parabolic, or compound relationship can produce a small r even when the variables are strongly related. Conversely, one influential point or one leverage point can create or destroy an apparent line. Four data sets can have nearly identical means, standard deviations, r, r^2, and standard error while their scatterplots show a clean line, a curve, an influential point, or nearly constant X values. Plot first.

The main assumptions are:

- **Linearity:** a straight line is a plausible summary of the data cloud.
- **Bivariate normality:** the paired observations come from a random sample in which X and Y are jointly normally distributed.
- **Measurement level:** both variables are continuous and measured at interval or ratio level.

When these assumptions or levels are not defensible, choose a nonlinear or nonparametric measure rather than treating r as a universal association index.

For a sample of paired observations, one useful form of Pearson's coefficient is:

`r = sum[(X - X-bar)(Y - Y-bar)] / [(n - 1) S_x S_y]`

The numerator is shared deviation or covariance in unscaled form; the denominator expresses the maximum potential variation that the two distributions share. The resulting ratio is standardized to the -1 to +1 range.

To test a sample r against a population correlation of zero, use independent random pairs from a bivariate normal population and:

`t = r * sqrt(n - 2) / sqrt(1 - r^2)`

with `n - 2` degrees of freedom. Choose a one-tailed test only when direction was specified in advance; otherwise use the two-tailed result.

### Common variance and interpretation

The coefficient of determination is `r^2`. It is the proportion of shared variance in X and Y and, in simple regression, the proportion of Y variance explained by X. For example, `r = .93` gives approximately `r^2 = .86`, so 86 percent of the variance is shared in the linear description. This is not the percentage of cases correctly predicted, and it does not imply that X causes Y.

Interpret direction, magnitude, statistical significance, common variance, study objectives, sample characteristics, and limitations together. Large samples can make small coefficients significant. The chapter notes that values below .30 may still be interesting in some business studies, but reporting depends on the phenomenon and the decision context.

Watch for **artifact correlations**. Aggregating distinct sectors or subgroups can create an overall positive relationship even when each sector has little or no relationship. Conversely, a subgroup such as financial firms can dominate a sales-assets plot and change the overall coefficient. Inspect subgroup plots and consider partial or multiple correlation or regression when confounding variables are plausible.

### Correlation versus regression

Both techniques usually require continuous interval-ratio variables and a linear relationship, but their questions differ:

- Correlation treats X and Y symmetrically and describes association; reversing the labels does not change r.
- Regression treats Y as dependent and X as independent; regression of Y on X differs from regression of X on Y.
- Correlation's `r^2` describes common variance; regression's `r^2` describes Y variability explained by its least-squares prediction from X.
- Correlation is not inherently a prediction equation; regression produces an equation and an error term for prediction.

The basic line is:

`Y-hat = b_0 + b_1 X`

where `b_1` is the slope and `b_0` is the intercept. The slope can be computed as the change in Y divided by the corresponding change in X in a perfectly linear illustration, and in general by the least-squares formula. The intercept is:

`b_0 = Y-bar - b_1 X-bar`

Do not give the intercept a substantive interpretation when X = 0 is outside the observed or meaningful range.

### Least squares and residuals

For imperfect data, several lines may look plausible. Least squares selects the line that minimizes:

`sum(e_i^2)`, where `e_i = Y_i - Y-hat_i`.

Squaring makes positive and negative errors comparable and penalizes large errors. After fitting, inspect residuals rather than trusting the equation. A residual plot with a curve, funnel, cluster, or sequential pattern signals that a straight-line model, equal-variance assumption, independence assumption, or measurement process may be inappropriate. Standardized residuals make cases comparable across the model.

Predictions farther from `X-bar` have wider uncertainty because the prediction and confidence bands bow outward. A point prediction estimates one future observation and includes individual error; a confidence interval for the mean response estimates the average Y for all cases at a selected X and is narrower.

### Testing fit and predictive usefulness

The most important bivariate regression test is often `H0: beta_1 = 0`. A zero slope can mean no systematic relationship, constant Y, or a relationship that is nonlinear and therefore poorly represented by a line. A two-tailed t-test is used because the true slope could be positive, negative, or zero. In the bivariate case, the regression F test tests the same linear model and equals the square of the slope t statistic.

Partition total variation into:

- Explained variation: the squared deviations of predicted Y from the mean of Y.
- Unexplained variation: the squared residual deviations of observed Y from predicted Y.
- Total variation: the squared deviations of observed Y from the mean of Y.

The coefficient of determination can be written as:

`r^2 = SS_regression / SS_total = 1 - SS_error / SS_total`.

The chapter suggests that predictive accuracy often begins to fall off below an r^2 of about .80, but this is a context-dependent guide, not a universal acceptance threshold. A model can have a significant slope and still be too imprecise for a decision.

### Nominal measures of association

Nominal measures describe strength in cross-classification tables. There is no universally best measure: coefficients respond differently to table shape, cell count, marginal distributions, sample size, and data distribution.

**Chi-square-based measures:**

- **Phi:** `phi = sqrt(chi-square / N)`. It is best for a 2-by-2 table and can exceed +1 in larger tables, so do not use it indiscriminately.
- **Cramer's V:** `V = sqrt(chi-square / [N(k - 1)])`, where k is the lesser number of rows or columns. It is bounded by 1 for tables of different shapes.
- **Contingency coefficient C:** `C = sqrt(chi-square / [chi-square + N])`. It works with many data forms but has a table-size-dependent upper limit, so its value is not directly comparable across table shapes.

These coefficients do not provide direction and do not imply causation. Test whether a relationship exists with chi-square, then use an appropriate coefficient to describe its strength.

**PRE measures:**

- **Lambda:** predict a nominal variable by always selecting its modal category, then see how much knowing another nominal variable reduces classification errors. It can be asymmetric, with opinion dependent on occupation for example, or symmetric.
- **Goodman and Kruskal's tau:** also uses table marginals and expresses the reduction in prediction error from knowing the other variable. Its asymmetric direction must be stated.
- **Uncertainty coefficient:** listed for multidimensional tables; treat it as an information-oriented alternative when the table structure and prediction question call for it.
- **Kappa:** listed as an agreement measure; use it when the substantive question is agreement rather than general association.

PRE has an intuitive interpretation:

`PRE = (P1 - P2) / P1`,

where P1 is the error probability without the predictor and P2 is the error probability with the predictor. A value of .39 means that knowledge of the predictor removes about 39 percent of the initial classification error in the stated direction.

### Ordinal measures of association

Ordinal measures preserve order and usually range from -1 to +1. For a pair of observations, a higher rank on one variable paired with a higher rank on the other is **concordant**; a higher rank paired with a lower rank is **discordant**. Let P be concordant pairs and Q be discordant pairs.

- **Goodman and Kruskal's gamma:** `gamma = (P - Q) / (P + Q)`. It has a PRE interpretation and ignores tied pairs in the basic denominator. Its sign shows direction and its absolute value shows strength.
- **Kendall's tau b:** adjusts for tied pairs on the row or column variables and is suited to square tables. It retains a -1 to +1 scale but does not use the same PRE interpretation as gamma.
- **Kendall's tau c:** adjusts the P-Q relationship for table dimensions and is suitable for tables of any size.
- **Somers's d:** adjusts for tied ranks and makes the direction of the dependent variable explicit. Report symmetric d or the appropriate asymmetric version depending on the prediction question.
- **Spearman's rho:** correlates ranks between two ordered variables. It is a rank form of Pearson correlation, relatively resistant to outliers and raw-score transformations, but sensitive to tied ranks.

For gamma, if discordant pairs greatly exceed concordant pairs, the coefficient is negative. The absolute value can be read as a proportional reduction in error when predicting concordance versus discordance rather than guessing. Kendall and Somers statistics use the same pair counts but alter the denominator to account for ties and direction. Spearman's rho uses rank differences:

`rho = 1 - [6 sum(d_i^2) / (n^3 - n)]`,

when there are no problematic ties. Assign tied observations their average ranks and use an available tie correction when ties materially affect the result.

The chapter's KeyDesign illustration makes the distinctions concrete: 172 concordant pairs and 992 discordant pairs produce `gamma = -.70`; after tie adjustments, Kendall's tau b is about `-.51`, tau c about `-.50`, and Somers's d is about `-.51` symmetrically, `-.53` when fitness is dependent, and `-.50` when management level is dependent. In the KDL recruiting illustration, panel and psychologist ranks have `sum(d^2) = 57` for 10 applicants, producing Spearman's `rho = .654`. The coefficient indicates moderately high agreement, not identical measurement or causal influence.

## Mental Models

**Plot, then coefficient, then decision.** A scatterplot or cross-tabulation reveals the structure. The coefficient compresses that structure. The significance test evaluates sampling evidence. The practical interpretation decides whether the compressed relationship is useful. Skipping the first step makes the later steps fragile.

**Correlation is a compass; regression is a route estimate.** Correlation indicates direction and strength without assigning roles. Regression chooses a predictor, draws a route through the data, and estimates where Y may be for a selected X, with uncertainty around that route.

**Residuals are the model's receipts.** The regression equation claims to explain observed Y. Residuals show what it failed to explain. Random, modest residuals support the model; patterns reveal missing structure, nonlinearity, unequal variance, dependence, or data problems.

**Association coefficients are lenses, not rulers.** Phi, V, C, lambda, tau, gamma, and rho answer different questions and respond differently to table shape, ties, marginals, and direction. There is no single universal categorical coefficient whose value can be compared without regard to design.

**Aggregation can manufacture a story.** A coefficient calculated after merging heterogeneous sectors may describe group composition rather than within-group movement. Always ask whether the relationship survives reasonable subgroup or control-variable inspection.

## Anti-patterns

- Writing a causal conclusion from a correlation or regression coefficient alone.
- Calculating Pearson's r before inspecting a scatterplot.
- Treating r near zero as proof of no relationship when curvature or subgroup structure is possible.
- Ignoring linearity, bivariate normality, measurement level, outliers, influential points, or leverage.
- Reporting statistical significance without magnitude, r^2, uncertainty, practical significance, or sample limitations.
- Aggregating distinct sectors and interpreting an artifact correlation as a within-sector relationship.
- Using correlation when the question is prediction, or using regression without specifying the dependent variable and predictor.
- Extrapolating far beyond the observed X range or reporting a point prediction without its prediction uncertainty.
- Treating a high r^2 as proof that the model is causal, unbiased, or useful for every subgroup.
- Applying nominal measures to ordinal data when the order is substantively important.
- Using phi for a large non-2-by-2 table, or comparing contingency coefficients across tables with different upper limits.
- Choosing gamma, tau, Somers's d, or rho without stating how ties, table shape, or the dependent direction were handled.
- Ignoring tied ranks in Spearman's rho or treating ranks as if they retained the original metric distances.
- Removing a legitimate outlier solely because it weakens the coefficient.

## Worked Example

**From growing-season temperature to wine-price prediction.** A simplified four-point illustration in the chapter shows price rising exactly with temperature, but a realistic ten-observation wine sample is used to fit a probabilistic line. The sample has mean temperature `X-bar = 19.61 C`, mean price `Y-bar = 3,598.80 EUR`, and `SS_x = 198.25`.

1. **Inspect and choose the model.** The scatterplot is approximately linear, so a simple linear regression is plausible. Temperature is X, price is Y; the variables are not being treated symmetrically because the goal is prediction.
2. **Fit the least-squares line.** The calculated coefficients are `b_1 = 216.439` and `b_0 = -645.569`, giving:

   `Y-hat = -645.57 + 216.44X`.

3. **Predict.** At 21 C, the point prediction is `Y-hat = 3,899.67 EUR`. The chapter's 95 percent point-prediction calculation gives approximately `3,899.67 +/- 1,308.29 EUR`, or about 2,591 to 5,208 EUR. The corresponding interval for the mean price at 21 C is narrower, about `3,899.67 +/- 411.42 EUR`, because it does not include the full individual-observation error.
4. **Test fit.** The standard error of the slope is 34.249, so `t = 216.439 / 34.249 = 5.659` with 8 degrees of freedom. Rejecting `H0: beta_1 = 0` supports a linear relationship. The regression ANOVA gives `F = 32.02` with df `(1, 8)` and `p < .005`; in this bivariate case it gives the same decision because `t^2 = F`.
5. **Assess explanatory power and diagnostics.** `r^2 = .80`, so about 80 percent of observed price variance is explained by the fitted temperature relationship in this sample. Standardized residuals are mostly between -2 and +2, with one around -2.2 and no strong pattern, but normality, linearity, equal variance, and independence still require diagnostic checks. The relationship does not prove that temperature causes price: rainfall, region, reputation, supply, and other factors could influence both the observed prices and the model.

The same workflow changes only its coefficient when the measurement level changes. For a nominal 2-by-2 campaign table, use chi-square and phi; for a larger table, Cramer's V; for an ordinal ranking problem, compare concordant and discordant pairs or use Spearman's rho. The design question, not the software menu, selects the measure.

## Key Takeaways

- A relational hypothesis specifies co-occurrence without silently claiming causation.
- Pearson's r requires continuous interval-ratio variables and a defensible linear, bivariate-normal model; inspect the scatterplot first.
- The sign of r gives direction, the absolute value gives magnitude, and r^2 gives common variance.
- A small or nonsignificant r can hide nonlinear structure; a large r can be an artifact of an influential point or aggregation.
- Correlation is symmetric; regression assigns X and Y roles and produces a least-squares prediction equation.
- Least squares minimizes squared residuals; residual plots test whether the line is an adequate model.
- Predictions farther from the mean of X have wider uncertainty, and point predictions are less precise than mean-response predictions.
- Test a regression slope of zero with t or the model with F; in bivariate regression `t^2 = F`.
- Nominal measures include phi, Cramer's V, contingency coefficient C, lambda, Goodman and Kruskal's tau, uncertainty coefficient, and kappa; choose based on table shape and prediction or agreement purpose.
- Ordinal measures include gamma, Kendall's tau b and tau c, Somers's d, and Spearman's rho; account for order, ties, and direction.
- Statistical significance, predictive accuracy, common variance, practical significance, and causal validity are different claims and must be reported separately.

## Connects To

- **Chapter 13, Collect, Prepare, and Examine Data:** scatterplots, boxplots, cross-tabulations, coding, outlier checks, and measurement levels are prerequisites for selecting an association measure.
- **Chapter 14, Hypothesis Testing:** tests of r, the regression slope, F, chi-square, and ordinal coefficients use the six-step logic of H0, alpha, calculated statistic, critical or p value, and interpretation.
- **Sampling and research design:** random paired observations, independence, experimental control, matching, and subgroup definitions determine whether association can be generalized or interpreted.
- **Research reports:** present the plot or table, coefficient, uncertainty and significance, practical meaning, limits, and a noncausal interpretation before making a recommendation.

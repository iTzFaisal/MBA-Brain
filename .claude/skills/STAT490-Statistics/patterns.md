# Patterns and Procedures

## Study Audit: Design Before Calculation
**When to use**: Any reported study or planned analysis.
**How**: State context and target population; identify source and sampling; classify measurement level; identify parameter and design; check bias, nonresponse, confounding, and ethics; then choose a method.
**Trade-offs**: More design work prevents invalid inference. A large but biased sample cannot compensate for poor selection.

## CVDOT Exploration
**When to use**: Before confidence intervals, tests, or modeling.
**How**: Inspect center, variation, distribution, outliers, and time. Use matching graphs and report results in original units. Investigate unusual values instead of deleting them automatically.
**Trade-offs**: Graphs reveal structure but do not prove causes; numerical summaries are compact but can hide shape and time order.

## Frequency-to-Graph Pipeline
**When to use**: Raw data are too large to inspect directly or a distribution must be communicated.
**How**: Build nonoverlapping, complete classes; calculate frequency, relative frequency, and cumulative frequency; use boundaries and equal widths; select histogram, polygon, ogive, dotplot, stemplot, bar/Pareto/pie, scatterplot, or time-series graph by data structure.
**Trade-offs**: Grouping improves readability but loses detail. Relative frequencies support unequal-size comparisons; cumulative frequencies answer cutoff questions.

## Probability Rule Router
**When to use**: A chance problem contains "not," "or," "and," conditions, or sequences.
**How**: Define the sample space and reference set. Use a complement for "not" or "at least one"; addition for inclusive same-trial "or"; multiplication with updated conditional factors for sequential "and"; Bayes to reverse a conditional after evidence; counting rules when equally likely outcomes must be enumerated.
**Trade-offs**: Direct formulas are exact when the model is correct. Simulation is flexible for complicated procedures but gives an estimate whose precision depends on repetitions.

## Discrete Model Check
**When to use**: A count is being modeled theoretically.
**How**: For binomial, verify fixed `n`, independent trials, two outcomes, and constant `p`; use `P(x)=C(n,x)p^x(1-p)^(n-x)`. For Poisson, verify random independent occurrences at a stable rate over a defined interval; use `P(x)=m^x e^(-m)/x!`.
**Trade-offs**: Exact binomial is preferred when feasible. Poisson is simpler for rare event rates and approximates binomial when `n >= 100` and `np <= 10`.

## Normal and Sampling-Distribution Workflow
**When to use**: A continuous probability or sample-mean probability is requested.
**How**: Sketch and shade; standardize; use a cumulative-left table or software; reverse standardization for a percentile. For `xbar`, use `sigma/sqrt(n)`, not `sigma`; check CLT conditions and apply finite-population correction when `n > 0.05N`.
**Trade-offs**: Normal methods are efficient when shape and sample-size conditions hold. A small, strongly nonnormal sample needs another method.

## Confidence-Interval Workflow
**When to use**: Estimate a population parameter with uncertainty.
**How**: Identify parameter and design; check assumptions; choose z, t, or chi-square; calculate `estimate +/- critical value*SE`; retain precision; round limits at the end; interpret confidence as repeated-procedure coverage. Round planned `n` up.
**Trade-offs**: Higher confidence or lower error requires a larger sample. Variance intervals are asymmetric because chi-square is skewed.

## Hypothesis-Test Workflow
**When to use**: Evaluate a claim about a population parameter.
**How**: Write `H0` with equality and `H1` with the claim direction; choose `alpha` in advance; check requirements; calculate the null-based statistic; use P-value or critical region; reject when `P <= alpha`; state the conclusion in context and report practical significance/power.
**Trade-offs**: A small P-value is evidence against `H0`, not proof of a cause. Failure to reject is not proof of equality.

## Two-Sample Design Router
**When to use**: Compare two groups or two measurements.
**How**: Decide independent versus paired. Use two-proportion z, unpooled two-mean t by default, matched-pairs t on differences, or F for variances only with normal populations. Pool only when the null/model requires it.
**Trade-offs**: Pairing can remove subject variation but is invalid without real matches. Pooling can increase efficiency but is fragile if equal variances are not credible.

## Correlation and Regression Workflow
**When to use**: Predict or describe association between paired quantitative variables.
**How**: Plot first; assess linearity, clusters, outliers, and spread; calculate `r`; fit least squares only when justified; inspect residuals; report `r^2`, `s_e`, and prediction intervals; avoid extrapolation and causal language.
**Trade-offs**: A line is interpretable and efficient for a linear pattern, but nonlinear structure, influential points, confounding, and out-of-range prediction can make it misleading.

## Categorical Chi-Square Router
**When to use**: Data are frequency counts.
**How**: One categorical variable -> goodness-of-fit with `E=np_i`, `df=k-1`. Two classifications in one population -> independence with `E=(row total)(column total)/grand total`, `df=(r-1)(c-1)`. Separate groups -> homogeneity. Matched binary pairs -> McNemar using discordant cells. Require expected counts at least 5 or use an appropriate exact method.
**Trade-offs**: Chi-square is broadly useful for counts but identifies association or unequal proportions, not causation. Similar tables can require different hypotheses.

## ANOVA and Multiple Comparisons
**When to use**: Compare three or more quantitative group means.
**How**: Check design, independence, normality, and variance; compute `F=MS(treatment)/MS(error)`; interpret a significant omnibus result as "at least one differs"; use Bonferroni or another adjusted follow-up to locate differences. In two-way ANOVA test interaction first.
**Trade-offs**: ANOVA controls the initial familywise decision efficiently, but follow-up tests need adjustment. Interaction can make averaged main effects misleading.

## Nonparametric Substitution
**When to use**: Parametric shape or measurement assumptions are not credible.
**How**: Sign test for direction/median; Wilcoxon signed-ranks for paired differences with approximate symmetry; rank-sum for two independent samples; Kruskal-Wallis for three or more; Spearman for monotone association; runs test for sequence randomness. Remove zeros and average tied ranks as required.
**Trade-offs**: Robustness costs information: signs discard magnitude and ranks discard distances. These methods are not assumption-free.

## Statistical Process Control
**When to use**: A characteristic is repeatedly measured in meaningful time order.
**How**: Start with a run chart. For equal normal subgroups use R for spread and x-bar for center; for equal-size binary attributes use a p chart. Investigate a nonrandom pattern, point beyond a limit, or run of eight; distinguish stability from specifications.
**Trade-offs**: Reacting to every fluctuation causes tampering. A stable process can still miss specifications, while an improvement can correctly trigger a signal that should be investigated and retained.

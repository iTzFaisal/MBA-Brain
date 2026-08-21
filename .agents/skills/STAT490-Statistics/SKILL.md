---
name: STAT490-Statistics
description: "Knowledge base from Elementary Statistics, 11th Edition, by Mario F. Triola. Use when applying statistical thinking, descriptive statistics, probability, confidence intervals, hypothesis tests, regression, ANOVA, nonparametric methods, or statistical process control."
---

<!-- argument-hint: [topic, procedure, formula, or chapter number] -->

# Elementary Statistics
**Author**: Mario F. Triola | **Edition**: 11th Edition (Technology Update) | **Pages**: ~784 PDF pages | **Chapters**: 15 instructional chapters + appendices | **Generated**: 2026-08-21

## How to Use This Skill

- **Without arguments** - use the core workflow and decision rules below.
- **With a topic or procedure** - find it in the Topic Index, then read the linked chapter file.
- **With a chapter** - ask for `ch07`, `chapter 10`, or a chapter title to load its formulas, assumptions, and worked example.
- **For formulas and thresholds** - check [cheatsheet.md](cheatsheet.md), then verify the chapter context.
- **For definitions or method trade-offs** - use [glossary.md](glossary.md) and [patterns.md](patterns.md).

## Core Frameworks & Mental Models

### 1. Design before mathematics

Start with **context, source, sampling method, measurement level, target population, parameter, and study design**. A large sample cannot repair voluntary response, undercoverage, nonresponse, bad measurement, or confounding. Random sampling supports generalizing from a sample to a population; random assignment supports attributing treatment differences to a treatment. They solve different problems. Treat the design as an evidence ceiling: describe what the data show, generalize only when selection supports it, and claim causation only when the experiment controls competing explanations.

### 2. Explore with CVDOT

Use the named checklist **CVDOT** before formal inference: **Center, Variation, Distribution, Outliers, Time**. Choose a display that matches the data: histogram, dotplot, stemplot, or boxplot for one quantitative variable; bar/Pareto/pie for categories; scatterplot for paired quantitative data; time-series or run chart when order matters. A graph is a diagnostic, not proof. Check axes, class boundaries, missing values, selection bias, and whether a suspicious observation is an error or a legitimate case.

### 3. Model uncertainty with the right probability structure

Define the procedure, sample space, event, and reference set before choosing a rule. Use complements for "not" and often for "at least one"; use the addition rule for inclusive **or** and the multiplication rule for sequential **and**. Conditional probability changes the denominator: `P(B | A)` is calculated only among outcomes in A. Use independence only when the probability is unchanged; for sampling without replacement, the book's 5% guideline permits an approximation when the sample is no more than 5% of the population. Bayes' theorem updates a prior by evidence; it does not swap `P(B | A)` with `P(A | B)`.

### 4. Validate the distribution model

Use a **binomial** model only for a fixed number of independent binary trials with constant success probability. Use **Poisson** for independent random occurrences at a stable rate over a defined interval. Use a **normal** model when area, z scores, and the distribution's shape are justified. For sample means, distinguish the sampling distribution from the raw-data distribution: `mu_xbar = mu` and `sigma_xbar = sigma/sqrt(n)`. Apply the central limit theorem only after checking random sampling, population shape, sample size, and finite-population correction. For a normal approximation to a binomial, verify `np >= 5` and `nq >= 5` and use the continuity correction.

### 5. Estimate with standard error and critical value

The reusable confidence-interval pattern is **estimate +/- (critical value)(standard error)**. Use `phat` for a population proportion, `xbar` for a mean, `s^2` for a variance, z for a proportion or known-sigma mean, t for an unknown-sigma mean, and chi-square for a normal-population variance or standard deviation. Confidence is a long-run property of the interval-producing procedure, not a probability assigned to a fixed parameter after the interval is calculated. For planning, convert percentage points to decimals, use a conservative planning proportion of 0.5 when no estimate exists, and round sample sizes up.

### 6. Test claims as controlled decisions

Write equality in `H0` and the directional or two-sided claim in `H1`; the alternative determines the tail before the data are inspected. Check design and assumptions, calculate the statistic under the null, and compare the P-value with preselected `alpha`: `P <= alpha` means reject `H0`; otherwise fail to reject it. Never say "accept" or "prove" a hypothesis. Report the original claim in context, then separate statistical significance from practical significance and consider power, effect size, and uncertainty.

### 7. Let structure choose comparisons

For two samples, first decide whether observations are independent or naturally paired. Use a two-proportion z method, unpooled two-mean t method by default, matched-pairs t on within-pair differences, or an F method for variances only under normality. Pool proportions for an equality-null test, not for a proportion confidence interval; pool mean variances only when a common variance is justified. For three or more means, use one-way ANOVA to compare between-group with within-group variation, then Bonferroni or another adjusted procedure to locate differences. In two-way ANOVA, test interaction first; do not interpret isolated main effects when factor effects depend on one another.

### 8. Use robust alternatives when assumptions fail

Nonparametric methods are not assumption-free. Use the sign test for direction/median claims, Wilcoxon signed-ranks for paired differences with approximate symmetry, Wilcoxon rank-sum (Mann-Whitney) for two independent samples, Kruskal-Wallis for three or more independent groups, Spearman rank correlation for monotone association, and the runs test for sequence randomness. Remove zeros where required, average tied ranks, preserve the design, and interpret rejection as evidence that the null is not adequate, not as proof of a specific cause.

### 9. Treat association and process data differently

For correlation and regression, **plot first**. `r` measures linear association, not causation; `r^2` is explained sample variation, not a causal percentage. Fit a line only when the pattern and residual diagnostics support it, avoid extrapolation, and use a prediction interval for an individual outcome. For time-ordered process data, use SPC: run chart first, then R chart for within-subgroup spread, x-bar chart for center, and p chart for binary attributes. A point beyond a control limit, an obvious nonrandom pattern, or a run of eight signals instability. Control limits describe process behavior, not customer specifications; investigate signals instead of tampering with noise.

## Chapter Index

| # | Title | Key frameworks |
|---|---|---|
| [ch01](chapters/ch01-introduction-to-statistics.md) | Introduction to Statistics | statistical thinking, sampling, design, measurement |
| [ch02](chapters/ch02-summarizing-and-graphing-data.md) | Summarizing and Graphing Data | CVDOT, frequency distributions, graph selection, bad graphs |
| [ch03](chapters/ch03-describing-exploring-and-comparing-data.md) | Statistics for Describing, Exploring, and Comparing Data | center, variation, z scores, quartiles, boxplots |
| [ch04](chapters/ch04-probability.md) | Probability | complements, addition/multiplication, conditional probability, Bayes |
| [ch05](chapters/ch05-discrete-probability-distributions.md) | Discrete Probability Distributions | expected value, binomial, Poisson, tail probabilities |
| [ch06](chapters/ch06-normal-probability-distributions.md) | Normal Probability Distributions | z scores, sampling distributions, CLT, continuity correction |
| [ch07](chapters/ch07-estimates-and-sample-sizes.md) | Estimates and Sample Sizes | confidence intervals, z/t/chi-square, margin of error |
| [ch08](chapters/ch08-hypothesis-testing.md) | Hypothesis Testing | null/alternative, P-values, errors, power, significance |
| [ch09](chapters/ch09-inferences-from-two-samples.md) | Inferences from Two Samples | two proportions, two means, matched pairs, F variance |
| [ch10](chapters/ch10-correlation-and-regression.md) | Correlation and Regression | r, least squares, residuals, prediction, multiple regression |
| [ch11](chapters/ch11-goodness-of-fit-and-contingency-tables.md) | Goodness-of-Fit and Contingency Tables | chi-square, independence, homogeneity, McNemar |
| [ch12](chapters/ch12-analysis-of-variance.md) | Analysis of Variance | one-way/two-way ANOVA, F, interaction, Bonferroni |
| [ch13](chapters/ch13-nonparametric-statistics.md) | Nonparametric Statistics | sign, Wilcoxon, Kruskal-Wallis, rank correlation, runs |
| [ch14](chapters/ch14-statistical-process-control.md) | Statistical Process Control | run, R, x-bar, p charts, stability |
| [ch15](chapters/ch15-projects-procedures-and-perspectives.md) | Projects, Procedures, Perspectives | project workflow, procedure routing, statistical literacy |

## Topic Index

- **ANOVA** -> ch12, ch15
- **Bayes' theorem** -> ch04
- **Binomial distribution** -> ch05, ch06, ch07, ch08
- **Boxplots and outliers** -> ch02, ch03, ch15
- **Central limit theorem** -> ch06, ch07, ch08
- **Chi-square methods** -> ch07, ch08, ch11
- **Confidence intervals** -> ch07, ch09, ch10
- **Correlation and causality** -> ch01, ch10, ch13, ch15
- **Control charts and SPC** -> ch14, ch15
- **Critical thinking and bias** -> ch01, ch02, ch15
- **Data levels and types** -> ch01, ch02, ch03, ch15
- **Descriptive statistics** -> ch02, ch03
- **Experimental design** -> ch01, ch09, ch12
- **F distribution and variance** -> ch07, ch08, ch09, ch12
- **Frequency distributions and graphs** -> ch02
- **Goodness-of-fit and contingency tables** -> ch11
- **Hypothesis testing** -> ch08, ch09, ch10, ch11, ch12, ch13
- **Measurement and sampling** -> ch01, ch15
- **Nonparametric statistics** -> ch13
- **Normal distribution and z scores** -> ch03, ch06, ch07, ch08
- **Poisson distribution** -> ch05
- **Probability and conditional probability** -> ch04
- **Regression and prediction** -> ch10
- **Sample size and margin of error** -> ch07, ch08
- **Sampling distributions** -> ch06, ch07
- **Statistical significance and power** -> ch01, ch08
- **Two-sample inference** -> ch09
- **Variation and standard deviation** -> ch03, ch12, ch14

## Supporting Files

- [glossary.md](glossary.md) - alphabetized terms and concise chapter references
- [patterns.md](patterns.md) - procedures, decision routes, and trade-offs
- [cheatsheet.md](cheatsheet.md) - compact formulas, thresholds, and diagnostic tells

## Scope & Limits

This skill is an educational synthesis of Triola's textbook and its examples. It does not replace course instructions, current statistical guidance, subject-matter expertise, study-specific design review, or professional advice. Formulas and thresholds are presented in the book's introductory context; verify assumptions, software conventions, data provenance, and the intended population before applying any procedure.

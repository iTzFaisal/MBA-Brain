# Research Decision Cheatsheet

## Frame the Study

| If the request is... | Do this | Do not do this |
|---|---|---|
| A symptom or opportunity | Build the question hierarchy | Jump straight to a survey |
| About what/how much | Use descriptive, survey, record, or observational evidence | Infer why from a percentage |
| About why/how | Explore qualitatively, model the process, or test a causal design | Treat a dashboard correlation as cause |
| An expensive or risky action | Add methods, controls, pilots, and replication | Use the cheapest method by default |
| Unlikely to change the decision | Reject or narrow the study | Approve it because data are interesting |

## Choose the Design

| Need | First choice | Critical qualification |
|---|---|---|
| Meaning, motive, process | IDI, focus group, case study | Stop at saturation; do not generalize statistically |
| Overt behavior or context | Observation | Code facts separately from inference |
| Attitudes, intentions, memory | Survey | Select mode by privacy, access, probing, speed, cost, and error |
| Effect of an intervention | Experiment | Check covariation, time order, alternatives, assignment, and validity |
| Population estimate | Probability sample | Audit frame coverage before sample size |
| Hidden or atypical cases | Purposive or snowball sample | Label findings as nonprobability insight |

## Measurement Defaults

- Use `construct -> operational definition -> indicant -> mapping rule -> variable`.
- Nominal: classify and count. Ordinal: rank and use medians/ranks. Interval: equal distances without a true zero. Ratio: meaningful zero and ratio operations.
- Scan participant, situation, measurer, and instrument error separately.
- Require validity, reliability, and practicality; reliability alone does not establish validity.
- Start scales and questions from the planned dummy table, not from familiar wording.

## Sampling Rules

- Accuracy before precision: more cases cannot repair a biased frame.
- Probability sampling supports known error and projection; nonprobability sampling supports access, discovery, or relevance.
- Stratify for subgroup precision; cluster for access cost; systematic sample with a random start and a checked skip interval.
- Choose the largest sample requirement among critical variables and subgroups.
- Never allow untracked interviewer substitutions.

## Data-Quality Gate

1. Preserve `CaseID` and a codebook.
2. Post-code text with explicit context, sampling, and recording units.
3. Edit for complete, accurate, and appropriately coded data.
4. Diagnose MCAR, MAR, or NMAR before deletion or replacement.
5. Inspect frequencies, plots, outliers, bases, and percentage direction.
6. Use EDA to find clues; reserve CFA for planned evidence.

## Test Selection

| Branch | Typical choices |
|---|---|
| One sample | one-sample t/Z, binomial, chi-square |
| Two independent samples | independent t/Z, chi-square/Fisher, Mann-Whitney |
| Two related samples | paired t, McNemar, sign/Wilcoxon |
| k independent samples | ANOVA, chi-square, Kruskal-Wallis |
| k related samples | repeated ANOVA, Cochran Q, Friedman |

Always state `H0`, `HA`, tail, alpha, statistic, p/critical value, assumptions, effect size, practical meaning, and limitations. Say “fail to reject H0,” never “prove” or “accept H0.”

## Association Rules

- Plot or cross-tabulate first.
- Pearson `r`: linear interval/ratio association; inspect outliers and bivariate normality.
- Regression: assign X and Y, inspect residuals, prediction range, and uncertainty.
- Nominal: phi for 2-by-2, Cramer's V for varied tables, PRE measures for prediction-error reduction.
- Ordinal: gamma, Kendall tau, Somers d, or Spearman rho; state tie and direction handling.
- Association, significance, common variance, prediction, practical value, and causation are separate claims.

## Report Quality

- Define the desired audience effect before selecting tables or charts.
- Map every recommendation to the minimum evidence needed to support it.
- Use a zero baseline or disclose a truncated scale; avoid decorative 3-D and misleading pie/time-series use.
- Combine Ethos, Logos, and Pathos without replacing evidence with emotion.
- Report response rates, missingness, nonresponse limits, conflicting findings, and scope.
- Protect participant identity, sponsor confidentiality, and authorized distribution.

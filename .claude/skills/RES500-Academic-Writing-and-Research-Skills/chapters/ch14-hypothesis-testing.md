# Chapter 14: Stage 4 - Hypothesis Testing

## Core Idea

Hypothesis testing uses sample evidence and probability to decide whether an observed difference or relationship is plausibly more than random sampling variation. The researcher tests the null hypothesis, chooses a procedure that matches the sample structure, measurement level, and assumptions, sets the significance level in advance, computes and evaluates the statistic, and reports the decision without confusing statistical significance with practical importance. The correct conclusion is usually to reject the null or fail to reject it, not to claim that a null hypothesis has been proved.

## Frameworks Introduced

**Classical statistics and Bayesian statistics.** Classical inference bases the decision on the sampling data and rejects or fails to reject an established hypothesis. Bayesian statistics also uses sample data but adds prior information, subjective estimates, costs, decision rules, and expected outcomes. Use the classical framework for the chapter's standard significance tests; use the Bayesian distinction to remember that sample-only inference is not the only possible decision framework.

**Induction and deduction.** Induction moves from sample facts toward tentative population conclusions and therefore needs probability to qualify confidence. Deduction moves from valid premises toward a conclusion. Hypothesis testing is primarily an inferential use of induction: the sample supplies evidence about a target population.

**Null and alternative hypothesis logic.** State a null hypothesis (H0) of no difference or no change for the statistical test and an alternative hypothesis (HA) that is its logical opposite. A nondirectional alternative creates a two-tailed test; a directional alternative creates a one-tailed test. The null is the presumption to challenge, not a claim that can normally be proved true.

**Type I error, Type II error, and power of the test.** A Type I error (alpha) rejects a true H0. A Type II error (beta) fails to reject a false H0. The power of the test is 1 - beta: the probability of correctly rejecting a false null under specified conditions. Use this framework to make the tradeoff between decision risks explicit before interpreting a result.

**Six-step hypothesis testing procedure.** Apply the chapter's sequence: state H0; choose the statistical test; select the significance level; compute the calculated difference value; obtain the critical test value; interpret the test. The sequence forces test choice and alpha decisions before the result is known.

**p-value decision rule.** A p value is the probability, assuming H0 is true, of observing a sample result as extreme as or more extreme than the result obtained. Compare p with alpha: if p < alpha, reject H0; if p >= alpha, fail to reject H0. The p value supplements, but does not replace, a clearly stated hypothesis, test direction, and practical interpretation.

**Parametric and nonparametric test families.** Parametric tests are preferred for interval and ratio data when independence, distributional, variance, and measurement assumptions are reasonable. Nonparametric tests are appropriate for nominal and ordinal data and for metric data whose parametric assumptions are not defensible. The tradeoff is usually power versus fewer and less stringent assumptions.

**Test-selection criteria.** Start with three questions: Is there one sample, two samples, or k samples? If there are two or k samples, are cases independent or related? What is the measurement scale? Then check sample size, equality of sample sizes, weighting, transformations, population assumptions, and the desired power.

**ANOVA variance partition.** Analysis of variance (ANOVA) separates total variability into between-groups variability, which can reflect a treatment or factor, and within-groups variability, which represents subject variation and error. The F ratio compares their mean squares. A large F indicates that between-group variation is large relative to error, but a significant omnibus result does not identify every differing pair.

**A priori contrasts and multiple comparison tests.** Use an a priori contrast when a particular comparison was specified before testing. If pairwise questions arise only after a significant ANOVA, use a post hoc or multiple-comparison procedure rather than a series of unadjusted t-tests. Scheffe's S is presented as a conservative, robust option in the chapter's airline illustration.

**Two-way and repeated-measures ANOVA.** A two-way model tests two main effects and their interaction; inspect the interaction before interpreting main effects. Repeated-measures ANOVA handles related trials in which the same subjects or units are measured more than once and serves as a multi-level extension of the paired-samples logic.

## Key Concepts

### Statistical and practical significance

A statistically significant difference is one for which there is good reason to believe the population difference is not only random sampling fluctuation. A census makes the distinction clear: if the population average mileage has moved from 60 to 61 mpg, the population change is established statistically, but a manager may judge one mpg to have little practical importance. With a sample mean of 64 from 25 vehicles, the researcher must decide whether the evidence is strong enough to infer a population change or whether the result could be sampling error.

Always ask "So what?" after rejecting H0. Report the size and operational consequences of a change, not only its p value. Very large samples can make trivial differences statistically significant; a nonsignificant result can still matter if the study had low power or a consequential Type II risk.

### H0, HA, tails, and decision language

For a benchmark population mean of 60 mpg, the alternatives could be:

- Two-tailed: HA: the mean is not 60; either increase or decrease matters.
- Upper one-tailed: HA: the mean is greater than 60; only an increase matters.
- Lower one-tailed: HA: the mean is less than 60; only a decrease matters.

In a two-tailed test with alpha = .05, the rejection probability is divided between the two tails. In a one-tailed test, the full rejection probability is placed in the direction specified by HA. Direction must be justified by the research question before seeing the data, not selected because it makes the observed result easier to reject.

Use "fail to reject H0" rather than "accept H0" when writing a formal conclusion. Failure to reject means that the evidence did not cross the selected decision boundary; it does not prove that no difference exists. If H0 is rejected, HA is supported, but inductive testing still does not prove the alternative with deductive certainty.

### Errors, alpha, beta, and power

At the chosen alpha, the critical values divide the sampling distribution into a rejection region and a region in which H0 is not rejected. With a two-tailed 5 percent test, alpha is .025 in each tail. A Type I error is the risk of rejecting an innocent or true null. A Type II error is the risk of not rejecting a false null. The probability of beta depends on the true parameter value, alpha, whether the test is one- or two-tailed, the standard deviation, and sample size. Power depends on the same design conditions.

Increase sample size to reduce standard error and generally increase power. A less conservative critical boundary can reduce beta, but it increases alpha, so the decision should reflect the relative costs of the two errors. Better measurement, observation, recording, or sampling can reduce variability and improve both error risks. The chapter notes 80 percent as a commonly recommended minimum power target, not as a substitute for a study-specific power analysis.

### The six steps in use

1. **State the null hypothesis.** Write H0 for the no-change or no-difference claim and HA for its logical alternative. Identify the direction if a one-tailed test is justified.
2. **Choose the statistical test.** Match the test to sample structure, measurement level, distribution, independence or relatedness, and power efficiency.
3. **Select the desired level of significance.** Set alpha before collecting or examining the final results. Common choices are .05 and .01; .10, .025, and .001 are also possible when justified.
4. **Compute the calculated difference value.** Apply the selected formula or obtain the statistic from software after data preparation and diagnostics.
5. **Obtain the critical test value.** Use the relevant distribution, degrees of freedom, tail direction, and alpha to locate the boundary.
6. **Interpret the test.** Reject H0 when the statistic enters the rejection region or when p < alpha; otherwise fail to reject H0. State what the result means for the population claim and the practical question.

### Choosing a test

The first branch is the number of samples:

- **One sample:** compare an observed distribution, proportion, or mean with a specified population or theoretical distribution. For interval-ratio data use a one-sample Z test or t-test; for nominal two-category data use a binomial test; for nominal multi-category data use a one-sample chi-square test; for ordinal or distributional questions, the chapter lists the one-sample Kolmogorov-Smirnov and runs tests.
- **Two independent samples:** cases in one sample do not determine cases in the other. For interval-ratio data use a Z test in large samples or when population variance is known, and a t-test for smaller normally distributed samples with equal variances. For nominal data use chi-square or Fisher exact when counts are small. For ordinal data use the median test or Mann-Whitney U.
- **Two related samples:** cases are matched, measured twice, or otherwise dependent. For interval-ratio data use the paired-samples t-test; for nominal before-after data use McNemar; for ordinal data use the sign test or Wilcoxon matched-pairs test.
- **k independent samples:** three or more independent groups require one-way or n-way ANOVA for suitable interval-ratio data, chi-square for nominal data, or Kruskal-Wallis one-way ANOVA by ranks for ordinal or assumption-violating metric data. The median extension is another ordinal alternative.
- **k related samples:** repeated measures on the same cases use repeated-measures ANOVA for interval-ratio data, Cochran Q for nominal outcomes, or the Friedman two-way ANOVA for ordinal outcomes.

Decision trees and expert systems can make the choice systematic, but they do not replace the researcher's responsibility to understand the data, assumptions, and question. A powerful test used outside its conditions is not a powerful design.

### Parametric assumptions and diagnostics

Parametric tests assume independent observations, populations that are normally distributed, equal population variances where required, and measurements at least at the interval level so arithmetic operations are meaningful. Check these conditions rather than assuming them because a software menu offers the procedure.

Use a normal probability plot to compare observed values with normal expectations. A roughly straight, narrow band supports normality; a detrended plot should show points randomly distributed around zero. A spread-and-level plot can diagnose equal variance. Histograms, boxplots, and other EDA displays provide additional evidence. Some parametric tests are robust to modest violations, but departures from linearity or equal variance can threaten specific tests.

Nonparametric tests do not require normally distributed populations or equal variances, although some still require independent cases or other conditions. They are the only technically appropriate general family for nominal data and are appropriate for ordinal data. They may also be used for interval-ratio data, but categorizing or ranking metric data can discard information. When parametric assumptions hold, the parametric test is normally more power-efficient; the chapter notes that nonparametric efficiency can still be high.

### Common test mechanics

For a one-sample mean when the population standard deviation is unknown, the t statistic is:

`t = (X-bar - mu0) / (s / sqrt(n))`

Use `n - 1` degrees of freedom. The t distribution has more tail area than the Z distribution because a sample standard deviation is being used as an estimate of the unknown population standard deviation. As sample size becomes large, t and Z become nearly identical.

For a one-sample or contingency-table chi-square test, use counts, not percentages:

`chi-square = sum[(O_i - E_i)^2 / E_i]`

where `O_i` is an observed count and `E_i` is the count expected under H0. For a one-sample k-category test, degrees of freedom are `k - 1`; for an r-by-c contingency table, they are `(r - 1)(c - 1)`. Expected frequencies must be large enough for the approximation: the chapter's traditional rule is at least 5 in each cell when df = 1, and for df > 1 no more than 20 percent of expected cells below 5 and none below 1. Combine adjacent categories by recoding when substantively defensible; use a binomial test for a small two-category sample.

For related samples, calculate the difference within each matched pair and analyze the set of differences as a one-sample problem. The paired-samples t statistic is `t = D-bar / (S_D / sqrt(n))`, with `n - 1` degrees of freedom. The McNemar test uses a two-by-two before-after table and focuses on the off-diagonal changes; with A and D as the two change cells, its continuity-corrected form is:

`chi-square = (|A - D| - 1)^2 / (A + D)`

### ANOVA and interactions

One-way ANOVA uses one fixed factor, such as airline or store type, and a continuous dependent variable. The factor levels are specified in advance, so inference does not automatically extend to unobserved levels. The model partitions total squared deviation into between-groups and within-groups components. The F ratio is:

`F = MS_between / MS_within`

with numerator degrees of freedom `k - 1` and denominator degrees of freedom `n - k`. If H0 is true, F should be near 1; larger values indicate that group means differ more than expected from within-group error. A significant F says that at least two means differ, not which ones.

Do not respond to a significant omnibus F by running every possible unadjusted t-test. A priori contrasts are appropriate for comparisons specified before testing. Post hoc multiple-comparison procedures evaluate pairwise differences while addressing the increased error from multiple comparisons. A two-way ANOVA tests factor A, factor B, and A-by-B interaction in one model. Inspect the interaction first: if it is significant, the main effects cannot be interpreted as if the other factor were irrelevant. Parallel cell-mean lines suggest no interaction; crossing or nonparallel lines suggest one.

Repeated-measures ANOVA treats each subject as its own control and removes the correlated-measure contribution before forming the F ratio. Its hypotheses can include a group effect, a trial or time effect, and a group-by-trial interaction. For nominal related outcomes, use Cochran Q; for ordinal related outcomes, rank each case across conditions and use Friedman two-way ANOVA.

## Mental Models

**The legal presumption.** H0 is like presumed innocence: retain the presumption until evidence crosses a predefined burden. Rejecting H0 is a decision under uncertainty, not an absolute proof of HA; failing to reject is not a declaration of innocence or no effect.

**The decision boundary.** Alpha fixes the amount of tail area that will count as unusually extreme if H0 is true. The test statistic locates the observed result relative to that boundary. Changing alpha, tail direction, sample size, or variability moves the boundary or changes how precisely the result is located.

**Test selection as a branching tree.** Branch first on one, two, or k samples; then on independent versus related cases; then on measurement scale; then on assumptions and sample details. Do not start with the statistic that is most familiar.

**ANOVA as a signal-to-noise ratio.** Between-groups mean square is the treatment or group signal; within-groups mean square is the error and natural variation. F asks whether the signal is large relative to noise, not whether every group pair is different.

**Inference and action are two filters.** Statistical significance filters out results that are plausibly sampling noise under H0. Practical significance filters for size, cost, risk, and managerial usefulness. A result should pass both filters before becoming a recommendation.

## Anti-patterns

- Treating a statistically significant difference as automatically important or causal.
- Writing that H0 was proved or accepted when the evidence only failed to reject it.
- Choosing a one-tailed direction after seeing the observed difference.
- Selecting alpha, changing tails, or changing the test to rescue a preferred conclusion.
- Reporting a p value without stating H0, HA, tail direction, sample structure, or practical magnitude.
- Treating a p value as the probability that H0 is true rather than as a tail probability under H0.
- Using a parametric test without checking independence, normality, equal variance, and measurement level.
- Applying chi-square to percentages rather than counts, or ignoring small expected frequencies.
- Using an independent-samples test for matched or repeated observations.
- Treating nominal or ordinal data as metric without a defensible reason, or discarding metric information through unnecessary categorization.
- Running many pairwise t-tests after ANOVA and allowing the familywise Type I error to grow.
- Interpreting main effects before checking whether factors interact.
- Interpreting a nonsignificant result as proof that the populations are identical when the study may have low power.
- Using A/B testing or repeated small optimizations as a substitute for a needed strategic change.

## Worked Example

**Testing whether hybrid-vehicle mileage increased.** A manufacturer historically reports a population mean of 50 mpg. A random sample of 100 vehicles has `X-bar = 52.5` mpg and `s = 14` mpg. The research question is directional: has average mileage increased?

1. **State hypotheses.** `H0: mu = 50 mpg`. `HA: mu > 50 mpg`, so this is a one-tailed test.
2. **Choose the test.** Mileage is ratio data, the sample is random, observations are treated as independent, and the population is assumed sufficiently normal. Use a one-sample t-test because the population standard deviation is unknown.
3. **Set alpha.** Choose `alpha = .05` before using the result.
4. **Calculate.**

   `t = (52.5 - 50) / (14 / sqrt(100)) = 1.786`, with `df = 99`.

5. **Find the critical value.** The one-tailed .05 critical t value is approximately 1.66.
6. **Interpret.** Because `1.786 > 1.66`, reject H0 and conclude that the sample provides statistically significant evidence that the population mean mileage increased. The conclusion is not proof of a permanent change, and the practical question remains whether a 2.5 mpg sample difference justifies the cost of the manufacturing response.

The same six-step structure applies to a chi-square test, independent or paired t-test, McNemar test, and ANOVA. Only the sampling structure, formula, degrees of freedom, assumptions, and critical distribution change.

## Key Takeaways

- Hypothesis testing generalizes from a sample to a population with explicit error probabilities; it does not deliver deductive certainty.
- H0 is the testable no-change or no-difference statement; HA supplies the logically opposite claim and determines tail direction.
- Alpha is the planned Type I risk; beta is the Type II risk; power is `1 - beta`.
- Use the six steps in order and set alpha and the tail direction before interpreting the data.
- A p value is a tail probability conditional on H0; compare it with alpha, then report magnitude and practical meaning.
- Select a test by number of samples, independent or related cases, measurement scale, distribution, variance, sample size, and power.
- Parametric tests are efficient when their assumptions hold; nonparametric tests protect against unsuitable distribution and measurement assumptions.
- Chi-square requires counts and adequate expected frequencies; paired tests require differences within matched cases.
- ANOVA compares between-group signal with within-group error. Follow a significant omnibus F with planned contrasts or controlled multiple comparisons.
- Inspect interactions before main effects in factorial ANOVA and account for dependence in repeated measures.
- Transparent reporting of uncertainty, decision risks, and practical significance is both a methodological and ethical responsibility.

## Connects To

- **Chapter 13, Collect, Prepare, and Examine Data:** EDA, editing, missing-data decisions, coding, and cross-tabulation determine whether a significance test is valid.
- **Chapter 15, Measures of Association:** hypothesis tests for correlation, regression slope, chi-square association, and ordinal measures use the same H0/HA, alpha, statistic, and interpretation logic.
- **Research design and sampling:** independence, random selection, matching, random assignment, and population definition determine which inference is justified.
- **Research reports:** a defensible result must communicate the test, decision, uncertainty, effect or difference, practical significance, and limitations rather than only a software p value.

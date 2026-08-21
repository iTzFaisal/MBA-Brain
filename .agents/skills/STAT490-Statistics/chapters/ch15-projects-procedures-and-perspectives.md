# Chapter 15: Projects, Procedures, Perspectives

## Core Idea

Statistical work is a complete investigation, not a calculator command. Define the question, context, source, sampling, and design; explore; route the study to a procedure matching measurement level, populations, dependence, and parameter; and communicate only supported conclusions. Statistical literacy means judging computer output with context, common sense, and practical awareness.

## Frameworks Introduced

### Suggested Final Project Format

**When to use:** For a real application combining several statistical ideas.

**Workflow:**
1. State the question, target population, variables, data collected, and how observations were obtained.
2. Describe the analysis and show relevant graphs, statistics, and software or calculator output.
3. State the findings in plain language.
4. Explain error sources, limits on generalization, and improvements that additional time or money could make.

Use a brief written report, not a term paper. Groups of three to five can give a coordinated 10- to 15-minute oral report; every member participates.

### Context, Source, Sampling Method

**When to use:** Before selecting an analysis or trusting a result.

**Audit:** Define what the data describe and the real-world question; inspect the source for bias; and assess whether the sampling method could produce a representative sample. Voluntary response (self-selection) is a serious threat because respondents may differ from nonrespondents. A sophisticated procedure cannot repair a biased sample.

### Exploring, Comparing, Describing

**When to use:** Immediately after collection and before confidence intervals or hypothesis tests.

**Checklist:** Match graphs to data: use a histogram, normal quantile plot, or boxplot for single-value numerical data; use a scatterplot for paired variables. Check:
- **Center:** mean and median.
- **Variation:** range and standard deviation.
- **Distribution:** shape and whether a normal population is plausible.
- **Outliers:** verify possible errors; retain valid extremes and transparently examine sensitivity to excluding them.
- **Time:** determine whether a population or process is stable or changing.

### Inferences: Estimating Parameters and Hypothesis Testing

**When to use:** After exploration, when sample data are used to say something about a population.

**How:** Decide whether to estimate a parameter with a confidence interval, test a claim with a hypothesis test, or do both. For changing process data, use a control chart first; ordinary inference requires statistical stability.

### Figure 15-1: Selecting the Appropriate Procedure

Use this decision tree instead of plugging data into a familiar procedure:

| Decision | Route |
|---|---|
| 1. Is the process stable? | If it may change over time, check with a control chart; proceed with ordinary inference only if stable. |
| 2. What is the measurement level? | **Interval/ratio:** numerical measurements such as height or weight. **Ordinal:** ranks. **Nominal:** categories summarized by proportions or counts. |
| 3. How many populations or groups? | One, two, or more than two; identify whether observations are independent or matched pairs. |
| 4. What is the target parameter or claim? | Mean, variance, proportion, difference in means or proportions, correlation/regression, or category frequencies. |
| 5. What is the purpose? | Estimate with the matching confidence interval, test with the matching hypothesis test, or use both. |

Procedure families implied by the tree:

| Data/design | Target | Procedure family |
|---|---|---|
| Interval/ratio, one population | Mean or variance | One-population mean or variance inference |
| Interval/ratio, two populations | Difference in means or comparison of variances | Two-population mean or variance inference |
| Interval/ratio, more than two populations | Several means | Multi-population/ANOVA; use the relevant rank method when the data/design require it |
| Numerical paired variables | Association or prediction | Correlation/regression; association is not causation |
| Ordinal data | Rank-based one-, two-, or multi-population comparison | Nonparametric/rank procedures |
| Nominal, one population | One proportion or category distribution | One-proportion inference or goodness-of-fit for one row of counts |
| Nominal, multiple populations/categories | Proportions or joint category counts | Two-population proportion inference or a contingency table for multiple rows/columns |
| Two related observations | Within-subject change/difference | Matched-pairs procedure |

### Conclusions and Practical Implications

**When to use:** At the end of every analysis and in the report or presentation.

Translate results for readers unfamiliar with statistical terminology, stay within what the design justifies, and state practical meaning. Report an estimate and uncertainty or the test outcome. Correlation describes a relationship; it does not establish causation.

### Statistical Literacy and “The Educated Person”

**When to use:** When reading surveys, media reports, professional studies, or computer-generated output.

Ask about context, source, sampling, center, variation, distribution, outliers, stability, parameter estimation, and claims. A carefully planned sample of about 1,200 voters may inform, while a much larger self-selected survey may be worthless. Critical thinking and clear communication are practical outcomes.

## Key Concepts

- **Context:** The real-world setting and question that give data meaning.
- **Source and sampling method:** Where data came from and how observations were selected; both affect bias and representativeness.
- **Voluntary response sample:** A self-selected sample especially vulnerable to systematic bias.
- **Exploratory analysis:** Graphs and descriptive statistics examining shape, center, variation, outliers, and stability before inference.
- **Level of measurement:** Interval/ratio, ordinal, or nominal classification limiting valid procedures.
- **Population parameter:** A feature such as a mean, variance, or proportion that sample data may estimate or test.
- **Statistical stability:** A process whose relevant characteristics are not changing over time.
- **Practical implication and statistical literacy:** A supported decision consequence and critical judgment of data claims.

## Mental Models

- **Validity has a sampling ceiling:** Advanced computation cannot rescue an unrepresentative sample.
- **Explore before infer:** Graphs and descriptive statistics diagnose assumptions, outliers, and instability first.
- **Procedure selection is routing, not guessing:** Measurement level, populations, dependence, parameter, and purpose determine the method.
- **Software is an instrument, not an interpreter:** A computer can answer an ill-posed question; context must judge the result.

## Anti-patterns

- **Mindless procedure selection:** Choosing a test before defining the question, measurement level, groups, parameter, and purpose.
- **Treating self-selection as random sampling:** Voluntary response can overrepresent strong opinions or unusual experiences.
- **Skipping exploration:** A summary or p-value can hide skewness, outliers, nonnormality, or change over time.
- **Deleting valid outliers silently:** Verify extreme values and examine exclusion transparently rather than concealing its effect.
- **Reading causation into correlation:** Association alone does not show that one variable produces changes in another.
- **Trusting output or omitting limitations:** Machine results may be nonsensical; projects need error sources, practical use, and improvements.

## Worked Example

Route the survey question, “Do students who exercise vigorously have different pulse rates from students who do not?” The example demonstrates decisions without inventing findings.

1. **Design and document.** Define the target population, outcome (heartbeats counted for one minute), and grouping variable (vigorous exercise for at least 20 minutes at least twice a week: yes/no). Record observations, conditions, who was contacted, and how.
2. **Audit context, source, and sampling.** Classmates are a convenience subset, not automatically all students; an open call creates a voluntary response sample. State the selection bias and restrict the population claim. A better study would use a representative sample and standardized pulse measurement.
3. **Explore before testing.** Use separate histograms or boxplots; compare means, medians, ranges, and standard deviations; inspect shape and outliers; verify suspicious values. This fixed-time survey does not establish a time trend. Repeated process data need a stability check first.
4. **Route the procedure.** Pulse rate is interval/ratio data, there are two groups, and observations are independent if each student contributes one measurement. The target is the difference between population means: use a two-population mean confidence interval and corresponding two-mean test. Same-student before/after measurements require matched pairs; ranks require the relevant ordinal/rank method.
5. **Conclude and report.** State the estimated difference and uncertainty or test result plainly: the sample may provide evidence of a difference, or may not provide sufficient evidence; it does not prove identical groups. This observational, potentially biased survey cannot show that exercise caused the difference. Include data/collection, analysis, displays, conclusion, limitations, and improvements in the brief report, with every member presenting a component.

## Key Takeaways

1. Define context, source, sampling method, and population before analyzing.
2. Explore center, variation, distribution, outliers, and time stability before inference.
3. Route procedures by measurement level, number of populations, dependence, parameter, and purpose.
4. Use confidence intervals to estimate and hypothesis tests to evaluate claims.
5. Treat voluntary response and other sampling flaws as validity problems that computation cannot repair.
6. Communicate plainly, state practical implications and limitations, and never turn correlation into causation.
7. Read computer output critically; statistical literacy requires context and common sense.

## Connects To

- **Chapters 1–3:** Context, sources, sampling, graphs, center, variation, distribution, and outliers provide the project foundation.
- **Chapters 7–13:** Confidence intervals, tests, two-population inference, correlation/regression, goodness-of-fit, contingency tables, and nonparametric procedures fill the routing framework.
- **Chapter 14:** Control charts establish stability before ordinary procedure selection for changing processes.
- **Research methods:** Sampling design, measurement quality, bias, observational limits, and reporting determine whether conclusions generalize.

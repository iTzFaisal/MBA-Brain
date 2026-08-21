# Chapter 1: Introduction to Statistics

## Core Idea

Statistics is disciplined reasoning from data to a defensible conclusion, not mainly calculation. Define the population and question, collect data that can represent that population, match methods to the data, inspect bias and design, and separate what evidence shows, suggests, and cannot establish. Distinguish statistical significance (unlikely under a no-effect explanation) from practical significance (large or useful enough to matter).

## Frameworks Introduced (exact named concepts, when to use, how)

- **Statistical Thinking**: Use whenever a study produces a result, including a study conducted by someone else. Ask: What is the context and goal? Who supplied the data? How were subjects sampled or assigned? Are variables measured appropriately? What conclusion is justified, and does it matter in practice?
- **Population, Sample, Census, Parameter, and Statistic**: Use to map a claim to its target. A population is the complete group of interest; a sample is the selected subcollection; a census measures every population member; a parameter describes a population; and a statistic describes a sample. The inference assumption is that the sample and measurement process represent the target well enough to generalize a statistic to a parameter.
- **Four Levels of Measurement**: Use before calculating or graphing. **Nominal** data are labels; **ordinal** data are ordered categories without meaningful differences; **interval** data have meaningful differences but no natural zero; **ratio** data also have a natural zero, making statements such as "twice" meaningful. Do not average identifiers or coded categories just because they contain digits.
- **Sampling Methods**: Use to plan selection and judge representativeness. A **simple random sample** of `n` gives every possible sample of size `n` an equal chance. A **random sample** gives each individual an equal chance; a **probability sample** gives each individual a known chance. **Systematic sampling** selects a start and every `k`th unit. **Stratified sampling** samples within every internally similar stratum; **cluster sampling** randomly selects clusters and includes all members of selected clusters. **Convenience sampling** uses accessible units, and **multistage sampling** combines methods across stages. Stratified sampling covers all strata; cluster sampling uses only selected clusters.
- **Observational Study versus Experiment**: Use to determine the allowable conclusion. An observational study measures without modifying subjects; an experiment applies a treatment and observes effects. An observational study may be **cross-sectional** (one point), **retrospective/case-control** (past records or recall), or **prospective/longitudinal/cohort** (follows groups forward). A causal claim requires a design that controls competing explanations, usually through random assignment and control.
- **Design of Experiments**: Use when assigning treatments. **Randomization** uses chance to form comparable groups; **replication** applies each treatment to enough subjects; **blinding** keeps subjects, investigators, or both from knowing assignments; **control** limits competing effects. A completely randomized design assigns all subjects by chance. A randomized block design forms similar blocks and randomizes within each. A matched pairs design compares treatments on paired similar subjects or within-subject before/after measurements.
- **Statistical Literacy and Critical Thinking**: Use this checklist for any reported study: identify its goal, population, and type; inspect source, sponsorship, and possible bias; evaluate sampling, nonresponse, wording, and setting; check definitions, measurement, confounding, graphs, and missing data; then test whether the conclusion meets the goal and has practical significance.

## Key Concepts

- **Data**: Collections of observations, including measurements, categories, and survey responses.
- **Quantitative data**: Counts or measurements. **Discrete** data take finite or countable values; **continuous** data can take any value on a gap-free scale.
- **Categorical data**: Names, labels, or attributes. Numerical codes remain categorical when they do not count or measure anything.
- **Percentages**: Keep the denominator visible: `percentage = part / total * 100%`. A large percentage says little when the sample or comparison base is poor.
- **Bias**: A systematic tendency for selection or measurement to misrepresent the population. More observations do not automatically remove it.
- **Voluntary response sample**: A self-selected sample in which people choose whether to participate; strong opinions are often overrepresented.
- **Confounding**: A situation in which effects of different factors cannot be separated, so an observed difference cannot be assigned to one factor confidently.
- **Sampling error versus nonsampling error**: Sampling error is chance fluctuation between a sample and population result. Nonsampling error comes from biased selection, nonresponse, poor measurement, recording, or analysis.
- **Correlation versus causality**: Correlation is association; it does not establish that one variable causes another. A third variable, reverse direction, or selection process may explain the pattern.
- **Ethics in statistics**: Obtain informed consent, protect confidentiality, and put subjects' well-being ahead of possible social benefit. Fabrication, selective omission, undisclosed conflicts, and deceptive reporting violate responsible practice.

## Mental Models

- **Garbage in, garbage out**: A correct formula applied to irrelevant, biased, or mismeasured data still produces an unreliable answer.
- **Representativeness beats volume**: Ask "Who had a chance to be included, and who chose to respond?" before asking how large `n` is. A large biased sample can be worse than a smaller well-designed one.
- **Sampling versus assignment**: Random sampling supports generalization from sample to population; random assignment supports attributing treatment-group differences to the treatment. They solve different problems.
- **Evidence ladder**: Data describe a sample; a good sample supports a population inference; a randomized controlled experiment may support a causal inference. Do not climb higher than the design permits.
- **Significance has two tests**: Ask first whether the result is unlikely by chance under no effect, then whether the effect is meaningful in real life.

## Anti-patterns

- **Treating a large response count as proof of quality**: Voluntary response, undercoverage, or nonresponse can dominate millions of observations.
- **Generalizing from convenience or self-selected respondents**: These data may describe participants, not the intended population.
- **Confusing association with cause**: A third variable, reverse direction, or selection process may explain the relationship.
- **Ignoring context, units, or measurement level**: The same digits can represent weights, labels, ranks, or temperatures and require different operations.
- **Trusting self-reported behavior without checking**: Recall, social desirability, or incentives can make reports differ from observed behavior.
- **Hiding denominator, subgroup size, or sponsor**: Percentages without a base, tiny subgroups, and financial interests can make weak evidence look authoritative.
- **Calling a statistically significant result useful automatically**: A tiny detectable effect may not be worth acting on.
- **Sacrificing participants for a result**: Consent, confidentiality, and welfare are constraints, not optional trade-offs.

## Worked Example

**The Literary Digest/Gallup sampling failure (1936).** Literary Digest mailed about 10 million ballots and received roughly 2.3 million replies. The replies predicted Alf Landon with 57%, yet Franklin D. Roosevelt won about 61% of the popular vote. The apparent strength of the poll was its enormous `n`, but its sampling frame leaned toward magazine subscribers, registered car owners, and telephone users. During the Great Depression those groups contained disproportionately more affluent, Republican voters. On top of that coverage problem, respondents self-selected, so people with stronger or more favorable interest were more likely to return a ballot.

George Gallup used a much smaller poll, about 50,000 people, selected to represent relevant demographic factors, and correctly predicted Roosevelt. The lesson is not that small samples are always better; selection quality and response bias matter before sample size. Audit a poll by asking: (1) Does the frame cover the target population? (2) Did relevant types of people have a fair, known chance of selection? (3) Who declined or chose to respond? The Digest failed these checks; Gallup's approach was better aligned with the population.

## Key Takeaways

1. Define the population and actual question before touching a formula.
2. Treat representativeness and measurement quality as prerequisites for inference; `large n` cannot repair systematic bias.
3. Identify whether a claim concerns a parameter or statistic, and classify the data by type and measurement level.
4. Use random sampling for population representation and random assignment for treatment comparability; do not confuse them.
5. Check source, sponsorship, nonresponse, wording, confounding, and missing data.
6. Report only conclusions justified by the design: correlation is not causation, and statistical significance is not practical significance.
7. Protect participants through informed consent, confidentiality, and priority for their well-being.

## Connects To

- **Descriptive statistics and graphs**: Data type, units, context, and measurement level determine suitable summaries and displays.
- **Statistical inference**: A statistic can estimate a population parameter only when sampling and measurement errors are controlled well enough.
- **Hypothesis testing**: Statistical significance formalizes chance-versus-effect reasoning; practical significance ties the decision to consequences.
- **Correlation and regression**: The warning that correlation does not imply causality remains a central interpretation rule.
- **Experimental design**: Randomization, replication, blinding, blocking, matching, and control support credible causal comparisons.

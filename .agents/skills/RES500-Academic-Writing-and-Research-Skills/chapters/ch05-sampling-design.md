# Chapter 5: Stage 2 - Sampling Design

## Core Idea

Sampling design answers: From whom or what does the data need to be collected, how will cases be reached, and how many are needed? A defensible design aligns the target population, population parameters, frame, case count, selection method, and recruitment protocol with the intended inference. Probability sampling supports precision estimates and generalization; nonprobability sampling is often the practical choice when the goal is exploration, access is limited, or population representation is not required.

## Frameworks Introduced

- **Six tasks of Sampling Design**: Complete these in relation to the investigative questions.
  1. **Define the target population and a case**: Specify the collective population possessing the needed information and the single entity drawn from it.
  2. **Define population parameters of interest**: Decide which population proportions, means, variances, or subgroup estimates the study must produce.
  3. **Identify and evaluate the sample frame**: Find or construct the list of cases from which selection will actually occur.
  4. **Define the number of cases needed**: Choose a census or sample and determine sample size where needed.
  5. **Define the sampling method**: Choose probability or nonprobability and the appropriate technique.
  6. **Define selection and recruitment protocols**: Standardize how cases or gatekeepers are selected, contacted, convinced, followed up, and replaced, if replacement is allowed.

- **Target population, case, parameter, statistic, and frame alignment**: Define the entity type before calculating a sample. Business populations may be people, organizations, events, objects, settings, or texts. A population parameter describes the target population; a sample statistic estimates it; the sample frame is the list actually used to draw cases. A frame that is outdated, omits members, or includes other populations creates coverage problems that a larger sample cannot repair.

- **Measurement level and estimator**: For interval or ratio variables, use the sample mean and standard deviation to estimate population mean and dispersion. For nominal or ordinal variables, use the sample incidence proportion, p, and pq for variance, where q = 1 - p. The parameter needed by the investigative question therefore affects the sample design and its size.

- **Sample versus census and the two premises of sampling theory**: Use a sample when cases are sufficiently similar that a subset can represent the population and when underestimates and overestimates tend to offset. Sampling usually improves cost, speed, access, and sometimes quality. A census is more defensible when the population is small, accessible, and highly variable, or when every case must be examined.

- **Accuracy and precision**: A valid sample requires both. **Accuracy** means little bias or systematic variance; **precision** means a small sampling error or standard error of estimate. Larger samples can reduce random error, but they do not correct a biased frame or selection process. Nonsampling error includes inappropriate sampling method, measurement-instrument errors, and behavioral effects, and can exceed sampling error.

- **Probability versus nonprobability sampling**: In probability sampling, every population case has a known nonzero chance of selection. It permits confidence estimates, error ranges, and population generalization when procedures are followed. Do not permit interviewers to alter selections, include unselected cases, or substitute cases except under predetermined rules. Nonprobability sampling is subjective and gives unknown selection probabilities; use it when representation is not the aim, the population or frame is unavailable, exploration needs atypical cases, or time and cost make probability sampling infeasible.

- **Unrestricted versus restricted sampling**: In unrestricted sampling, cases are drawn from the target population without selection criteria beyond the sampling method. In restricted sampling, selection follows additional rules, as in complex probability designs or purposive controls.

- **Complex probability sampling**: Use these when simple random sampling is too costly or inefficient.
  - **Simple random sampling**: Every case has an equal known chance. Assign unique numbers and use a random-number generator or table. The selection probability is sample size divided by population size.
  - **Systematic sampling**: Choose a random start, then every kth case, where the skip interval is population or frame size divided by sample size. It is simple and flexible, but check for periodicity and monotonic ordering; randomize the list, vary starts, or replicate samples when needed.
  - **Stratified random sampling**: Divide the population into mutually exclusive strata, sample randomly within each, and weight results when appropriate. Use it to improve efficiency, guarantee subgroup data, or apply different collection methods. Aim for homogeneity within strata and heterogeneity between them. **Proportionate stratified sampling** mirrors population shares and is self-weighting; **disproportionate stratified sampling** intentionally allocates cases differently to secure subgroup precision or respond to differences in variance or cost.
  - **Cluster sampling**: Divide the population into many small groups, randomly select groups, and study their cases. It is economically efficient when individual frames are unavailable or cases are geographically dispersed, but often statistically less efficient because cluster members are alike. **Area sampling** is the geographic form. Consider cluster homogeneity, size, equal versus unequal clusters, and single-stage versus multistage selection.
  - **Double sampling**, also called sequential or multiphase sampling: Collect inexpensive information from a first sample, then stratify or otherwise identify a subsample for more intensive study. Choose it when the cost savings of the first phase outweigh the added design complexity.

- **Nonprobability sampling techniques**:
  - **Convenience sampling** is unrestricted selection of readily available cases. It is cheapest and least reliable, but can be useful for early exploratory idea generation.
  - **Purposive sampling** selects cases by criteria. **Judgment sampling** seeks a particular experience or atypical group; **quota sampling** seeks specified distributions on relevant, known population characteristics. With more than a few controls, use frequency control rather than trying to fill every possible combination through precision control.
  - **Snowball sampling** uses referrals to locate hidden or difficult-to-identify populations and referral networks.

- **Sample-size decision rule**: For probability samples, size increases with population variance, desired precision, narrower error range, higher confidence, and the number of subgroups requiring minimum cases. Decide confidence and acceptable interval from project risk, estimate dispersion from prior research or a pilot, consider finite-population adjustment when the sample exceeds about 5 percent of the population, and use the largest sample required by the critical questions.

- **Selection and recruitment protocol**: Specify how a case is drawn, how each case or gatekeeper is contacted, how participation is encouraged, and what follow-up ensures completion. Mixed-access sampling combines phone, email, mobile, wireless, or addressed-based invitations to reduce coverage and nonresponse problems. Incentives may include money, food, time off, results, or a charitable donation, but promises must be honored.

- **Sampling ethics**: Sponsor nondisclosure and purpose nondisclosure may protect a study, but deception should be controlled through informed consent and, where permitted, post-research debriefing. Researchers owe participants the promised incentive and a quality process; participants owe truthful screening responses and confidentiality when required. In cross-national or culturally varied studies, the frame, method, weighting, and recruitment practice must respect ethnic and cultural differences rather than assuming one technique fits every group.

## Key Concepts

- **Target population**: The complete set of entities to which the study intends to refer.
- **Case**: One element drawn from the target population.
- **Sample frame**: The operational list of cases from which the sample is drawn; it may be too-inclusive or incomplete.
- **Population parameter**: A summary descriptor of a population variable, such as a mean, variance, or incidence proportion.
- **Sample statistic**: A descriptor calculated from sample data and used as an estimator of a population parameter.
- **Census**: Measurement of every case in the defined population.
- **Sampling error**: The difference between a sample estimate and the population parameter caused by chance selection.
- **Nonsampling error**: Error caused by other design, measurement, or participant-behavior decisions.
- **Systematic variance**: A known or unknown influence that makes scores lean in one direction.
- **Skip interval**: The k spacing used in systematic sampling.
- **Proportionate stratified sampling**: Allocation to strata in proportion to their population shares.
- **Disproportionate stratified sampling**: Allocation that departs from population shares to meet analytical or efficiency needs.
- **Area sampling**: Geographic cluster sampling using areas such as city blocks.
- **Nonresponse error**: Distortion arising when selected cases cannot be reached or do not participate.
- **Mixed-access sampling**: Recruiting through multiple invitation modes, possibly allowing a different mode for completion.

## Mental Models

- **The frame defines the reachable population.** Before asking whether a sample is representative, compare the desired population with the actual list and screen or rebuild the frame where necessary.
- **Accuracy comes before precision.** More cases tighten estimates around the wrong answer if the frame or selection process is biased.
- **Choose probability for inference, nonprobability for insight or access.** The decision follows the intended use of findings, not a universal hierarchy of methods.
- **Sample size buys precision with diminishing returns.** Set confidence, interval width, variance, and subgroup needs first; do not select a number merely because it is large or a fixed percentage of the population.
- **Economic efficiency is not statistical efficiency.** Cluster sampling may require more interviews for the same precision but still be preferable when travel and access costs dominate.

## Anti-patterns

- **Assuming a large sample is automatically representative**: The Literary Digest failure shows that millions of cases from a biased frame can produce a systematically wrong estimate.
- **Confusing a sample frame with the target population**: An old directory, an omitted subgroup, or a too-inclusive list changes who can be selected.
- **Treating a nonprobability sample as probability evidence**: Unknown selection chances do not support confidence intervals or unqualified population generalization.
- **Ignoring periodicity or list trends in systematic sampling**: A skip interval matching weekly, building, chronological, or size patterns can bias the estimate.
- **Overloading quota controls**: Filling every combination of many characteristics creates expensive cells and still leaves fieldworker judgment at the point of selection.
- **Allowing ad hoc substitutions**: Interviewer convenience and untracked replacement undermine the planned selection probabilities.
- **Focusing only on sampling error**: Poor wording, refusal, inaccurate records, and participant behavior can create larger nonsampling errors.
- **Using deception, coercive incentives, or broken promises**: Sponsor or purpose nondisclosure requires informed consent and, where allowed, debriefing; incentives must be delivered promptly and fairly.

## Worked Example

Metro University is deciding whether to invest in a membership dining club. The target population is currently enrolled students and full- or part-time employees on the main campus, with families considered in the service definition; a student or employee is a case. Critical parameters include meals eaten on or near campus, the proportion interested in joining, and spending per visit. The fall directory is an imperfect spring frame: it may omit new members, retain withdrawals, omit families, and include branch-campus or retired personnel. The researchers therefore combine current registrar and human-resources lists, or screen a broader frame and remove ineligible cases.

Because the investment is substantial and population inference matters, they choose probability sampling. A pilot supplies a standard deviation of 4.1 meals. For meal frequency, they select 95 percent confidence and an interval of plus or minus 0.5 meal, producing a required sample of about 259. For interest in joining, a pilot estimate of 30 percent with a 95 percent confidence interval of plus or minus 10 percentage points requires about 81 cases. Since both questions matter, the design uses the larger requirement, n = 259, rather than averaging or choosing the smaller number. The final protocol specifies the frame, random or stratified selection, contact mode, follow-up, and an incentive that encourages rather than compels participation.

## Key Takeaways

1. Define the population, case, parameters, frame, count, method, and recruitment protocol before drawing cases.
2. A sample is useful only when its selection process supports the inference being made.
3. Probability sampling is the route to known precision and generalization; nonprobability sampling is defensible for exploration, access, or nonrepresentative objectives when its limits are disclosed.
4. Larger samples address random error, not systematic frame or selection bias.
5. Use stratification to represent important subgroups, clustering to reduce access cost, systematic sampling for practical ordered lists, and double sampling to reserve intensive work for informative cases.
6. Set sample size from risk, confidence, interval width, dispersion, and subgroup requirements; take the largest requirement among critical variables.
7. Protect participants through informed consent, honest screening, fair incentives, confidentiality where promised, and disciplined selection procedures.

## Connects To

- **Chapter 4 - Research Design Overview**: Supplies the sampling-design decisions that must align with data collection method, objective, scope, time, and causal claims.
- **Chapter 6 - Qualitative Research**: Applies purposive, convenience, and snowball sampling while replacing statistical representativeness with relevance and data saturation.
- **Measurement design**: The level and scale of the intended measurements determine the population parameters, precision requirements, and sample size.

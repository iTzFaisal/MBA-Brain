# Chapter 10: Measurement Foundations

## Core Idea
Research measurement turns empirical observations into analyzable data by selecting variables, defining mapping rules, and applying those rules consistently. The researcher should measure observable indicants of properties, choose the weakest scale that answers the investigative question without discarding needed information, and evaluate the result for validity, reliability, and practicality while controlling predictable error sources.

## Frameworks Introduced
- **Three Tasks of Measurement**: Use this whenever an abstract research question must become a data-collection rule.
  - Select the variables to measure.
  - Develop mapping rules that assign numbers or symbols to the relevant aspects of each variable.
  - Apply the mapping rules to every observation. Symbols such as `M` and `F` can function as labels, although numerical labels may be used for software convenience.
- **Objects, Properties, and Indicants of Properties**: Distinguish what the study is about from what can actually be observed. Objects may be concrete concepts (a person, automobile, or detergent) or abstract constructs (leadership, lifestyle, or peer pressure). Properties are characteristics of objects. Because a construct or property is often not directly observable, measure an indicant or pointer and state the operational definition that connects the indicant to the construct.
- **Four Measurement Scale Types: Nominal, Ordinal, Interval, and Ratio**: Choose the level required by the analysis plan; the levels add classification, order, distance, and origin in sequence.
  - **Nominal**: Mutually exclusive, collectively exhaustive categories with no order, distance, or meaningful origin. Use counts, frequency distributions, mode, and cross-tabulation to find patterns.
  - **Ordinal**: Categories plus a logical greater-than/less-than order, but unknown distances between ranks and no natural origin. Use median, percentiles or quartiles, and generally nonparametric methods.
  - **Interval**: Classification, order, and equal intervals, but an arbitrary zero. Calendar time and Fahrenheit temperature illustrate why a value cannot be interpreted as a meaningful multiple of another. With a roughly symmetric distribution, use the mean, standard deviation, correlations, t-tests, and F-tests; use median and interquartile range when skewed.
  - **Ratio**: All preceding properties plus an absolute, meaningful zero. Amounts such as sales, profits, distance, elapsed time, and number of employees support all preceding operations plus multiplication, division, geometric or harmonic means, and coefficients of variation.
- **Recoding**: Use during data preparation when a statistical procedure needs a common or simpler data level. Reapply mapping rules to reduce a powerful measure, such as ratio income into ranges. Recoding can lower measurement power, but it cannot manufacture order, equal distance, or a natural zero that was never collected.
- **Four Major Sources of Measurement Differences**: Treat observed variation as potentially contaminated by the **participant**, **situation**, **measurer**, or **instrument**. Participant effects include knowledge, social pressure, fatigue, anxiety, and mood; situational effects include privacy, other people, location, and time pressure; measurer effects include rewording, prompting, stereotypes, recording, coding, and calculation; instrument effects include ambiguity, leading or double-barreled questions, mechanical defects, and incomplete topic coverage.
- **Criteria for Good Measurement: Validity, Reliability, and Practicality**: Apply the three criteria together.
  - **Validity** asks whether the measure captures what the investigative question requires. **Content validity** is adequate coverage of the relevant topic universe and can be judged by experts or a content validity ratio. **Criterion-related validity** concerns prediction or estimation: concurrent validity uses a current criterion, while predictive validity uses a later outcome. A criterion should be relevant, unbiased, reliable, and available. **Construct validity** asks what theoretical construct accounts for the variance; convergent validity expects association with measures of the same construct, while discriminant validity expects separation from different constructs. Factor analysis and multitrait-multimethod analysis can help.
  - **Reliability** is freedom from random or unstable error and consistency of results. **Stability** is consistency across repeated measurement, commonly test-retest. **Equivalence** is agreement across observers or parallel forms; interrater reliability compares judges, and alternative forms compare item samples. **Internal consistency** is homogeneity among items in one administration, assessed with split-half methods, KR20, or Cronbach's alpha. More items can inflate internal-consistency estimates; the Spearman-Brown correction adjusts for test length.
  - **Practicality** is the operational test of **economy**, **convenience**, and **interpretability**. A scientifically excellent measure that is unaffordable, hard to administer, or impossible for others to interpret is not useful in the actual project.

## Key Concepts
- **Concept**: A bundle of meanings or characteristics abstracted from similar objects, events, or behaviors.
- **Construct**: An idea deliberately invented for a research or theory-building purpose, often built from simpler concepts and not directly observable.
- **Variable**: A measurable event, act, trait, or attribute to which values or numerals are assigned; variables may be dichotomous, discrete, or continuous.
- **Operational definition**: A construct definition stated in observable criteria and procedures so competent researchers would classify or count cases in the same way.
- **Mapping rule**: The rule that translates an observed indicant into a symbol or number.
- **Systematic error**: Bias that shifts measurement in a patterned direction.
- **Random error**: Erratic variation that makes repeated results unstable.
- **Internal validity of a measure**: Whether the instrument measures the thing its designer claims it measures; it is distinct from external validity, which concerns generalization across persons, settings, and times.
- **Scale power**: The information added as a measure moves from nominal to ordinal to interval to ratio. Higher levels permit more sensitive statistics, but lower-level recoding loses information.
- **Practicality**: The combined economy, convenience, and interpretability of the measurement process.

## Mental Models
- **Measure the pointer, not the abstraction**: Treat a construct as a theoretical target and ask which observable indicants would make its presence, absence, or degree defensible.
- **Think of scale levels as an information ladder**: Collect at the highest defensible level when future analysis may need it, because a ratio measure can be reduced to ordinal or nominal form, but a nominal label cannot be upgraded after collection.
- **Use the archery test**: Reliability means repeated shots cluster; validity means they cluster around the intended target. A measure can be reliable but consistently wrong, while unreliability prevents confidence in validity.
- **Run an error-source scan before fielding**: Ask separately what the participant may bring, what the setting may induce, what the measurer may change, and what the instrument may omit or distort.

## Anti-patterns
- **Treating category codes as quantities**: `1 = Christian` and `2 = Muslim` do not make religion an interval variable; arithmetic on nominal labels is meaningless.
- **Assuming ordinal gaps are equal**: A rank of 1 is not necessarily twice as favorable as a rank of 2, and adjacent satisfaction categories may not represent equal attitude changes.
- **Writing an operational definition that another researcher cannot reproduce**: Vague constructs produce inconsistent classification and make validity impossible to defend.
- **Leaving coverage gaps in an apparently broad instrument**: Measuring only employment and ecology, for example, does not establish adequate coverage of a corporation's public image if civic leadership, education, philanthropy, or minority issues are relevant.
- **Confusing reliability with validity**: A scale that consistently overstates a value is reliable but not valid; reliability is necessary for validity, not sufficient for it.
- **Trying to create measurement power after collection**: Recoding can reduce a scale's power, not create an order, equal interval, or absolute zero that the original mapping rule did not contain.
- **Optimizing science while ignoring operations**: Excessive length, hard-to-follow instructions, poor layout, or unavailable criteria can make a valid and reliable design unusable.

## Worked Example
An auto-show study wants both the male-to-female ratio of attendees and opinions about a new concept car's styling. The researcher first selects two variables and maps them differently. For gender, the rule is `M` for male and `F` for female. Among five observed attendees, A, B, and C are male and D and E are female, so the descriptive result is three males to two females; the symbols are labels, not quantities. For styling, the rule is `5 = very desirable`, `4 = desirable`, `3 = neither`, `2 = undesirable`, and `1 = very undesirable`. A, B, and C select undesirable and D and E select desirable. This second variable has order, but the researcher should not automatically treat the gap between 1 and 2 as equal to the gap between 4 and 5. The example therefore shows the three tasks of measurement and why the mapping rule, not the appearance of a number, determines the scale and permissible analysis.

## Key Takeaways
1. Define the construct and its observable indicants before writing a measurement question.
2. Select a scale by the properties the mapping rule can defend, not by the statistical technique the researcher prefers.
3. Nominal, ordinal, interval, and ratio scales add classification, order, distance, and meaningful origin; higher levels contain more information.
4. Separate true differences from participant, situational, measurer, and instrument effects.
5. Establish content, criterion-related, and construct validity; then check stability, equivalence, and internal consistency.
6. Treat economy, convenience, and interpretability as design requirements, not afterthoughts.

## Connects To
- **Chapter 11: Measurement Questions**: The scale level and investigative purpose determine whether a question should use rating, ranking, categorization, sorting, or an open response.
- **Chapter 12: Measurement Instruments**: Validity, reliability, and practicality are implemented through the assembled questionnaire, its instructions, sequencing, physical design, and pretests.
- **Hypothesis testing and data preparation**: Mapping rules determine which summaries, association measures, and tests are defensible, while recoding can simplify analysis only by accepting information loss.

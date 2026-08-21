# Chapter 13: Stage 3 - Collect, Prepare, and Examine Data

## Core Idea

Stage 3 ends with a clean data file that is suitable for analysis and interpretation. Collection is not finished when responses arrive: the researcher must create a usable data file, convert open responses into defensible codes, edit for completeness, accuracy, and appropriate coding, and examine the file visually and numerically before confirmatory analysis. The preliminary analysis plan is the guide, but exploratory data analysis (EDA) is deliberately flexible enough to reveal unexpected patterns and to reduce an analysis that is unlikely to be informative.

## Frameworks Introduced

**Stage 3: Collect, Prepare, and Examine Data.** Use this as the end-to-end workflow after the instrument has been designed and pretested: train collectors; set a collection timeline; establish instrument disposition; invite participants; activate the survey; remind participants; enter data; postcode and edit; run EDA; and produce the clean file. Each handoff is a possible source of error, so the workflow is a quality-control sequence rather than a list of administrative tasks.

**Data fields, records, files, and databases.** Treat one variable or measurement response as a data field, all fields for one case as a data record, all records for a study as a data file, and related files as a database. Use a CaseID that links a row back to the original instrument. This is especially useful when a frequency or descriptive summary exposes an impossible code, an omission, or an unusual value.

**Coding scheme (codebook).** Build the codebook before final entry, using pretest information to check the mapping rules. It should identify each variable, its name and label, its location in the record, response codes and labels, and variable type. Use it to make the data file consistent across cases and to determine which statistical procedures are defensible. Closed questions can be precoded; open responses need postcollection coding.

**Content analysis.** Apply content analysis when written, audio, or video material must be converted into quantitative categories so that patterns and inferences can be examined. Start by defining the units of analysis, develop or revise category rules, code consistently, assess reliability, and then summarize the codes with frequencies or export them to a data file. Human judgment remains part of the method even when software performs calculations.

**The data-quality triad: complete, accurate, and appropriately coded.** Use this three-part editing standard after entry. Completeness asks whether all collected information is usable; accuracy asks whether the data are real and were recorded correctly; appropriate coding asks whether the mapping rules are suitable for the analysis plan and comparison data.

**MCAR, MAR, and NMAR missing-data classification.** First examine why and where values are missing; then choose a correction or treatment. The chapter distinguishes data missing completely at random (MCAR), data missing at random (MAR), and data missing but not missing at random (NMAR). The classification determines whether deletion or replacement is likely to distort the result.

**Exploratory Data Analysis (EDA) and Confirmatory Data Analysis (CFA).** EDA searches for clues through frequencies, descriptive summaries, visual displays, recoding, and cross-tabulation. CFA evaluates evidence with formal inference and significance testing. Use EDA first, inspect visually, and cycle between exploration and confirmation rather than treating a numerical summary as sufficient evidence.

**Cross-tabulation and contingency tables.** Use cross-tabulation during EDA to compare classification variables with target variables. Rows and columns define cells; row, column, and total percentages plus marginal totals describe the table. When the same structure is used for formal testing, it is a contingency table and the test asks whether the variables are independent.

**Automatic Interaction Detection (AID).** Use AID when a dependent variable and a set of possible predictors (the chapter allows up to 300) are available and the goal is to find the best successive splits of the data. The computer searches for the best single split, tests that split, and then repeats the search within subgroups. The result identifies important predictors and best- and worst-case segments, not a causal proof.

## Key Concepts

### Collecting and entering data

Data collection is the set of actions that fields the instrument. Train interviewers on the whole instrument, skip directions, likely pitfalls, participant approach, wording emphasis, facial expressions, response aids, bias reduction, and submission procedures. Create a collection timeline that includes activation start and stop times, entry, editing, and the expected ready date for the clean file. Establish in advance how paper instruments, uploads, email submissions, photographs, or videos will be returned and stored.

The invitation builds cooperation and rapport. Prepare the invitation script, email, letter, screening questions, and any compensation information. Survey activation is the decision that the instrument is ready to launch after known measurement problems have been addressed. Reminders can materially improve response rates, but they should follow the probability-sampling and contact procedures established for the study.

Data entry converts primary or secondary data into a medium that can be viewed and manipulated. A spreadsheet may be imported into statistical software, or data may be entered directly. Each participant is one record; each variable is a column. A multi-item rating question requires one variable and one column for each item. Keep the CaseID in the data file and on the source instrument.

Entry technologies can reduce keyboarding effort and error: online or mobile participant entry, barcode and optical recognition, voice recognition, tablets, spreadsheets, and statistical packages. They do not remove the need for a codebook or editing.

### Postcollection coding and content analysis

Open-ended questions should be reassessed after collection even if categories were anticipated during instrument design. Coding begins with three choices:

1. **Context units:** the text relevant to the research objective, such as a performance description in an employee evaluation.
2. **Sampling units:** the text elements to be coded, such as words, phrases, sentences, or paragraphs.
3. **Recording units:** the ideas embedded in the content.

Recording units can be:

- **Syntactical units:** author-defined words, phrases, sentences, or paragraphs. Words are small and reliable units, but their meaning still depends on context.
- **Referential units:** words or phrases that describe an object and can reveal attitudes, values, or preferences.
- **Propositional units:** assertions about an object, such as a claim about savings.
- **Thematic units:** higher-level topics inferred within and across texts, such as packaging, flavor, past behavior, present reaction, or future intention.

Choose among **human coding**, **algorithm-based automated coding**, and **user-guided automated coding** by weighing speed, cost, accuracy, contextual meaning, code control, ability to revise codes, and the reliability burden. Human coders are strongest at complex meaning and context, including sarcasm, but are slower and require attention to intra-rater and, when multiple coders are used, inter-rater reliability. Automated approaches are faster and can process large volumes, but software does not itself establish valid categories or understand every contextual meaning. User-guided automation can combine analyst control with processing speed, but its categories still require review.

For human coding, **intra-rater reliability** means that the same coder applies the same rules consistently; **inter-rater reliability** means that different coders assign the same code to the same text. Establish the rules, test them on a subset, revise ambiguous categories, and document the final rules before counting. Software processes such as stemming, aliasing, and exclusion can normalize word forms, include synonyms, and remove trivial words, but these settings are methodological decisions rather than neutral buttons.

Closed questions are normally precoded, but collected results may show that the original categories are too fine or not useful for the planned analysis. **Recoding** develops new mapping rules by merging initial categories. For example, a seven-point agreement scale may be collapsed to three categories if the data and research objective do not support the original distinctions. Recoding is legitimate when the rule is explicit and defensible; it should not be a way to manufacture a desired result.

### Editing for data quality

Editing verifies that the designated coding scheme was used and that all collected data were entered correctly. Review a descriptive statistical summary for each variable to find omissions, out-of-range values, odd codes, and entry mistakes.

**Completeness** does not mean guessing what a participant intended. Translate interviewer shorthand soon after an interview. If an entry is missing, a callback is preferable to guessing when time and budget allow. A "don't know" response can represent materially different states: lack of knowledge, a request for information the participant does not have, an unformed judgment, lack of information at the moment, reluctance to answer, or a belief that the question is not worth considering. A small DK group may be manageable; a large group may reveal a poor measurement question or a meaningful response category that was omitted. Code legitimate DK responses deliberately and do not automatically mix all DK cases with ordinary missing values.

**Missing data** can result from skipped or refused questions, lack of knowledge, branching, researcher error, software or equipment failure, corrupted files, changed instruments, or dropout from a longitudinal study. Use the two-step process:

1. Explore the pattern to determine which missingness mechanism is plausible.
2. Select a treatment that matches the mechanism and the analysis purpose.

The chapter's three categories are:

- **MCAR:** missingness is not dependent on the missing variable or another variable in the record, as with an inadvertent skipped question.
- **MAR:** missingness is not dependent on the variable itself but is dependent on another recorded variable, as when a branch in an earlier question makes a later question inapplicable.
- **NMAR:** missingness is dependent on the variable itself and may express sensitivity, unanswerability, or an unprovided substantive response such as "no preference."

The chapter describes three ways to salvage affected records:

- **Listwise deletion:** exclude a case with missing data from analyses involving the affected variable. This is least problematic under appropriate MCAR or MAR conditions, but can bias results when the omitted cases represent a meaningful NMAR group.
- **Pairwise deletion:** use an estimate based on cases with data for the variable or pair of variables; the chapter emphasizes its MCAR assumption and potential bias from replacing extreme or systematically missing opinions with a central value.
- **Predictive replacement:** use an observed value on another variable to estimate the missing value; this is associated with MAR but can still inject bias if the surrogate does not measure the same construct.

**Accuracy** includes data validation. Look for suspicious response patterns, recontact a portion of respondents when interviewer error or falsification is suspected, and inspect completion IP addresses and times for online instruments. Similar handwriting can flag questionable paper instruments. Check impossible units, multiple answers to a single-response question, misplaced entries, out-of-range codes, and contradictions. If the correct answer cannot be established, use an editor code such as unknown rather than inventing one.

**Appropriate coding** requires categories that are mutually exclusive, exhaustive, and focused on one dimension. The mapping rules should provide useful partitions for hypothesis tests and relationships and should permit comparison with available data.

### Exploratory data analysis and displays

The preliminary analysis plan determines which frequencies, recodes, cross-tabs, and displays are worth producing. Frequencies may eliminate a planned analysis that cannot reveal anything useful; for example, a variable with 85 percent of cases in one category may have little value in a planned cross-tabulation. Conversely, an unexpected split or concentration can justify an exploratory follow-up.

Start with visual inspection because numerical summaries can conceal skewness, subgroups, outliers, or nonlinear patterns. The main display choices are:

- **Frequency tables:** list value codes from low to high with counts, percent, valid percent adjusted for missing values, and cumulative percent. They are useful for response ranges, repeated values, missingness, and coding errors.
- **Bar charts and pie graphs:** compare nominal categories. Do not use a histogram for a variable whose categories have no order.
- **Histograms:** group ordered interval-ratio values into equal-width intervals. A practical rule from the chapter is to use approximately the square root of the number of observations for the number of intervals, then use the range divided by that number for an approximate interval width. Inspect the shape, modes, gaps, skewness, kurtosis, and detached values.
- **Stem-and-leaf displays:** preserve the actual values and their rank order while showing range, clusters, gaps, shape, and potential outliers. They make it easier to link an unusual value back to a case.
- **Pareto diagrams:** display counts or themes in descending order with percentages summing to 100 percent and a cumulative line. They identify the small number of problems that account for a large share of cases.
- **Boxplots:** summarize the minimum, lower quartile, median, upper quartile, and maximum, showing location, spread, tail length, and outliers. The box contains the central 50 percent; whiskers normally extend to the largest and smallest observations within 1.5 interquartile ranges (IQR) of the hinges. Values beyond the fences deserve investigation, not automatic deletion. Extreme outliers may be entry errors; legitimate outliers may be substantively important.
- **Notched boxplots:** use a notch around the median to compare population medians at a stated confidence level. Nonoverlapping notches support a difference in medians under the plot's assumptions.
- **Mapping and geographic displays:** link files through a common field such as an address, then overlay attitudes, behavior, or demographics on geographic maps. GIS adds contextual data but requires appropriate software, hardware, and expertise.

Median and quartiles are resistant statistics: they change little when a small part of the data becomes extreme. Means and standard deviations are nonresistant, so they can stop representing the main body of an asymmetric distribution. Use this distinction when deciding whether a surprising value is an error, a meaningful case, or a reason to use resistant summaries.

### Cross-tabulation and percentages

In a cross-tabulation, the intersection of a row category and a column category is a cell. Marginals are the row and column totals. Each cell can show its count, row percentage, column percentage, and total percentage. In formal confirmatory analysis, the table becomes a contingency table for testing independence.

Choose the percentage direction before examining the table. A consistent default is to place the hypothesized independent variable in the rows and compare row percentages. If the independent variable is placed in columns, compare column percentages instead. The direction must answer the hypothesis; a column percentage can describe who is in a selected group while saying nothing about whether membership predicts selection.

Interpret every percentage with its base. Counts without denominators are hard to compare across samples. Avoid unweighted averages of percentages; weight each percentage by the size of its source group. Avoid very large percentage changes when a fold-change is clearer, never compute a percentage decrease from the smaller base, and treat impressive percentages based on very small counts cautiously.

When a two-variable table does not explain why a relationship occurs, add a control variable or a nested variable and construct an n-way table. A relationship that is visible in a two-way table may change within control-variable categories. AID is a more automated extension: it repeatedly finds the predictor that produces the most useful statistically supported split and the greatest reduction in unexplained variation within each subgroup.

For presentation, round numbers when precision is not essential, order values to reveal patterns, use totals or percentages to focus comparison, keep like scales together, and use titles that state what, where, when, and the unit of measure. Choose simplicity over a single complex table; whitespace and consistent ordering often make the message more visible.

## Mental Models

**The clean-file pipeline.** Think of raw responses as material moving through gates: collection, entry, postcoding, editing, visual examination, and cross-tabulation. A file is not ready because it opens in software; it is ready when the gates have produced documented, interpretable variables.

**EDA as detective work and CFA as judging evidence.** EDA searches for clues and generates or refines questions. CFA evaluates the strength of evidence against a formal hypothesis. A judge cannot evaluate evidence that the detective never found, and a researcher should not run a confirmatory model before checking what the data actually look like.

**Every percentage has a base and a direction.** Ask "percentage of what?" and "which variable is presumed to influence which?" before interpreting a cell. Changing the row/column orientation can change the apparent story without changing the data.

**Outliers are signals, not verdicts.** An unusual point can be a coding or entry error, a legitimate rare case, or a clue about a subgroup. First trace it to the source using CaseID; then decide whether to correct, retain, display, or analyze it separately.

**A codebook is a contract.** The codebook makes the intended meaning of each field visible to the person entering data, the analyst selecting procedures, and anyone auditing the file. A code that is numerically valid but semantically ambiguous is not quality data.

## Anti-patterns

- Launching an instrument while known measurement or disposition problems remain.
- Treating data entry as clerical work that needs no codebook, CaseID, or validation.
- Guessing a missing answer instead of making a callback or assigning a transparent unknown code.
- Treating every DK response as ordinary missingness without asking what the response means.
- Applying listwise deletion, central-value replacement, or predictive replacement without examining MCAR, MAR, or NMAR implications.
- Assuming online entry eliminates editing, validation, or falsification checks.
- Letting an automated content-analysis category stand without checking its meaning, category boundaries, or reliability.
- Using categories that overlap, omit possible responses, or mix multiple dimensions.
- Skipping visual inspection because a mean, standard deviation, or frequency table has been computed.
- Using a histogram for nominal categories or a pie chart for a high-cardinality continuous variable.
- Deleting every outlier, including legitimate cases, or retaining an obvious data-entry error because it is statistically interesting.
- Reading column percentages when the hypothesis concerns how the row variable predicts the outcome.
- Averaging percentages from groups of different sizes without weighting them, or emphasizing a large percentage based on a tiny denominator.
- Cross-tabulating a nearly constant variable simply because it appeared in the preliminary plan.
- Presenting an opaque n-way table or AID tree as causal evidence rather than as an exploratory aid.

## Worked Example

**A sales survey moves from raw responses to a defensible file.** A manufacturing firm's 100 sales employees answer, "How can company-customer relations be improved?" The researcher first defines the context as the response to that question, uses phrases or complete statements as sampling units, and records the ideas as thematic or referential units. An initial codebook uses locus of responsibility, but the first pass shows that useful action categories also include sales-manager behavior, sales process, customer buying process, salesperson training, technology, environmental conditions, and no action area. The researcher revises the codebook, tests the revised rules on a subset, and checks intra-rater reliability; if a second coder is used, inter-rater reliability is also checked. Frequencies can now summarize the 100 responses without pretending that unstructured text was already quantitative.

The same study contains a ratio variable for average annual purchases among 50 priority customers. With 50 observations, a starting rule gives about 8 histogram intervals; the range from 54.9 to 218.2 suggests an interval width of about 20. The histogram and boxplot reveal a concentrated lower and middle body and extreme upper values around 183.2, 206.9, and 218.2. The analyst traces those cases through their CaseIDs before deciding whether they are legitimate high-value customers or entry errors. A stem-and-leaf display preserves the exact values for that check.

Finally, the assignment table is cross-tabulated by gender. Among 62 men, 22 were selected and 40 were not; among 38 women, 6 were selected and 32 were not. Because gender is the hypothesized independent variable, compare row percentages: 35.5 percent of men versus 15.8 percent of women were selected. Column percentages would answer a different question about the composition of selected and nonselected groups. The table is evidence of a descriptive difference, not proof that gender caused selection; a later contingency-table test would address statistical independence. The output of the workflow is a documented, edited file in which the text codes, purchase outliers, and table denominators can all be audited.

## Key Takeaways

- The operational objective of Stage 3 is a clean, auditable data file, not merely a completed survey.
- Collection quality depends on collector training, a timeline, a disposition process, a clear invitation, controlled activation, reminders, and disciplined entry.
- A codebook maps responses to variables and makes records comparable across cases.
- Content analysis requires explicit units, category rules, and intra-rater and inter-rater reliability where applicable.
- Edit every variable for completeness, accuracy, and appropriate coding; do not guess missing values.
- Diagnose MCAR, MAR, and NMAR before selecting deletion or replacement.
- Use visual EDA to expose shape, spread, subgroups, outliers, and coding problems before confirmatory analysis.
- Cross-tabulations are useful only when cells, bases, percentage direction, and the hypothesized independent variable are made explicit.
- Controls, nested variables, and AID can reveal conditions under which a relationship changes, but they do not by themselves establish causation.
- Ethical interpretation requires transparent handling of missingness, outliers, respondent information, and denominators so that data-quality decisions do not quietly create bias.

## Connects To

- **Chapter 14, Hypothesis Testing:** the clean file, EDA diagnostics, and contingency tables determine whether a later significance test is appropriate and interpretable.
- **Chapter 15, Measures of Association:** cross-tabulations, visual diagnostics, and properly coded measurement levels feed correlation, regression, and nonparametric association measures.
- **Instrument design and measurement:** pretesting and mapping rules determine whether postcollection coding and later tests can work at all.
- **Research reporting:** table order, labels, percentage bases, summaries, and visual displays carry the evidence into the final insight and recommendation.

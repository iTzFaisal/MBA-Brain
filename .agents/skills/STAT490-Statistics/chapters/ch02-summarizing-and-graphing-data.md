# Chapter 2: Summarizing and Graphing Data

## Core Idea

Raw data become useful when a display preserves context while exposing the
distribution:

`raw values -> classes and frequencies -> relative/cumulative summaries -> graph -> interpretation`

Summary answers questions about center, variation, distribution, outliers, and
time. Choose the display from the data and decision, then check scale and
collection method.

## Frameworks Introduced (exact named concepts, when to use, how)

### Characteristics of Data (CVDOT)

Use CVDOT as the first interpretation checklist:

- **Center:** Where is a representative or average value?
- **Variation:** How much do values differ?
- **Distribution:** Is the shape bell-shaped, uniform, skewed, clustered, or otherwise patterned?
- **Outliers:** Are any values far from almost all the others?
- **Time:** Does the characteristic change over time?

Histograms support the first four; a time-series graph is needed for the fifth.

### Frequency Distribution (Frequency Table)

Use a **frequency distribution** to compress quantitative data into classes or
count qualitative observations in categories. A frequency `f` is the number of
observations in a class or category; every observation is counted once.

### Class Limits, Class Boundaries, Class Midpoints, and Class Width

**Lower and upper class limits** are the smallest and largest recorded values
allowed. **Class boundaries** remove gaps between adjacent classes. The **class
midpoint** is `(lower class limit + upper class limit) / 2`; **class width** is
the difference between consecutive lower limits or boundaries.

For `60-69` and `70-79`, boundaries are `59.5`, `69.5`, and `79.5`; width is
10, not `69 - 60 = 9`. Boundaries make histogram bars touch and define ogive
cutoffs.

### Procedure for Constructing a Frequency Distribution

1. Choose 5 to 20 classes. Sturges's optional starting guideline is `1 + (log n)/(log 2)` classes for `n` observations.
2. Compute `(maximum - minimum) / (number of classes)` and round up to a convenient width.
3. Use the minimum, or a convenient value below it, as the first lower class limit.
4. Add the width repeatedly to generate lower limits and determine upper limits.
5. Tally every observation into one class and total the tallies.

Classes should be nonoverlapping, cover every observation, and normally have
equal widths. Include zero-frequency classes so gaps remain visible. Use
open-ended classes only deliberately, since their widths are not uniform.

### Relative Frequency Distribution (Percentage Frequency Distribution)

Use relative frequencies for proportions and unequal-sample comparisons. For
class frequency `f` and total `n`:

`relative frequency = f / n`

`percentage frequency = (f / n) * 100%`

Totals should be approximately 1 or 100%; small discrepancies can be rounding.
Percentages within categories who have an attribute are conditional percentages,
not this distribution, and need not total 100%.

### Cumulative Frequency Distribution

Use cumulative frequency when the question asks how many observations fall below
a cutoff. Add each frequency to the running total, label the results with
`less than` and the corresponding upper class boundary, and verify that the
final cumulative frequency equals `n`.

### Normal Distribution

As a visual screen, an approximately **normal distribution** has frequencies that
start low, rise to one or two high frequencies, and fall again, with approximate
symmetry on both sides. This is judgment, not proof: a roughly bell-shaped but
strongly asymmetric display should not pass a strict screen.

### Graph Selection Rules

- **Histogram / relative frequency histogram:** Quantitative distributions; use equal-width adjacent bars, boundaries on `x`, and frequencies or percentages on `y`, then read CVDOT.
- **Frequency polygon / relative frequency polygon:** Connect midpoint frequencies and close to the axis at both ends; use relative frequencies for unequal samples. **Ogive:** plot boundaries against cumulative frequencies for cutoff questions.
- **Dotplot / stemplot:** Use a dotplot when every value in a small or moderate quantitative set matters. Use a stemplot for sorted values, with a place-value key; split or condense rows without hiding counts.
- **Bar graph / multiple bar graph / Pareto chart / pie chart:** Use bars for qualitative categories; gaps are acceptable, multiple bars compare groups, and Pareto bars descend by frequency. Use a pie chart for parts of a whole; proportion `p` has angle `p * 360` degrees, but Pareto is better for close comparisons.
- **Scatterplot:** Paired quantitative variables on `x` and `y`; inspect association, clusters, gaps, and outliers, not causation. **Time-series graph:** quantitative measurements in chronological order, with time on `x` and measurement on `y`; a histogram erases time order.

### Describing, Exploring, and Comparing Data

Use a graph to **describe** center, variation, shape, outliers, gaps, and
clusters; **explore** relationships or hidden groups; and **compare** distributions
on common axes. Use relative displays for unequal sample sizes.

### Critical Thinking: Bad Graphs

Audit numerical correctness and visual honesty:

- A bar baseline should normally be zero. A truncated axis magnifies differences; disclose it and interpret visual distances cautiously.
- Pictographs and 3-D objects encode area or volume rather than a one-dimensional quantity. A box four times as wide, tall, and deep has 64 times the volume.
- Decorative ink competes with data; make units, categories, scales, and labels explicit. A graph cannot fix voluntary-response sampling, nonrandom missing values, or a biased source.

## Key Concepts (5-10)

1. **Distribution is central:** tables and graphs reveal how observations spread.
2. **Class anatomy controls accuracy:** limits, boundaries, midpoints, and width have distinct jobs.
3. **Frequency types answer different questions:** counts, shares, and running totals serve different decisions.
4. **CVDOT and graph choice organize interpretation:** scan the five characteristics and match the display to structure.
5. **Normal-looking requires rise-and-fall plus approximate symmetry:** one high bar is insufficient.

## Mental Models

### The Compression Ladder

`data list -> frequency table -> relative/cumulative table -> graph`

Each step trades detail for insight; choose the lowest level that answers the
question without hiding an important feature.

### Boundaries Are the Glue

Limits label values; boundaries sit halfway between neighboring limits, remove
gaps, and define histogram and ogive scales.

### CVDOT Scan, Then Question

Scan with CVDOT, then ask whether the decision requires shares, a cutoff count, a
most-common category, a relationship, or change over time. That selects the scale.

### Shape Is Evidence, Not a Verdict

A gap, tail, or repeated last digit is a clue about a split, skew, outlier, or
measurement shortcut, not proof of a cause.

## Anti-patterns

- Calling `upper limit - lower limit` the class width; use consecutive lower limits or boundaries. Allowing overlap, uncovered values, unexplained widths, or omitted zero-frequency classes.
- Putting gaps between histogram bars, using a histogram for categories, or comparing unequal raw counts instead of relative frequencies.
- Accepting frequency totals far from approximately 1 (100%), confusing conditional percentages with a distribution, or calling a distribution normal because of one high bar.
- Using a pie chart for close comparisons, erasing time order, inferring causation from a scatterplot, or exaggerating with nonzero baselines, 3-D dimensions, clutter, or biased samples.

## Worked Example

### Female Pulse Rates: From Data to a Frequency Table

For 40 female pulse rates from 60 to 124 beats per minute, choose 7 classes:

1. Preliminary width: `(124 - 60) / 7 = 9.142857...`; round up to 10.
2. Start at 60 and add 10 to get lower limits `60, 70, 80, 90, 100, 110, 120`.
3. Use upper limits one below the next lower limit, then tally.

| Pulse class | Boundaries | Midpoint | `f` | `%` | Cumulative `f` |
|---|---:|---:|---:|---:|---:|
| 60-69 | 59.5-69.5 | 64.5 | 12 | 30.0% | 12 |
| 70-79 | 69.5-79.5 | 74.5 | 14 | 35.0% | 26 |
| 80-89 | 79.5-89.5 | 84.5 | 11 | 27.5% | 37 |
| 90-99 | 89.5-99.5 | 94.5 | 1 | 2.5% | 38 |
| 100-109 | 99.5-109.5 | 104.5 | 1 | 2.5% | 39 |
| 110-119 | 109.5-119.5 | 114.5 | 0 | 0.0% | 39 |
| 120-129 | 119.5-129.5 | 124.5 | 1 | 2.5% | 40 |

Checks: frequencies total 40, percentages total 100%, final cumulative frequency
is 40, and width is 10. A histogram uses these boundaries.
CVDOT shows a center near 80, most values in 60-89, a sparse right tail, and a
gap from the zero-frequency class; it is not a clean symmetric bell. The table
reports 26 observations below 80 and 37 below 90. Multiples of four suggest
checking for 15-second counting multiplied by four before calling the data wrong.

## Key Takeaways (3-7 actionable)

1. Start with CVDOT and collection context; build complete, nonoverlapping classes and verify totals.
2. Use relative frequencies for unequal samples, cumulative frequencies for cutoff questions, and displays matched to data structure.
3. Treat normality as a judgment-based screen and audit baselines, dimensions, labels, clutter, sampling, and missing data.

## Connects To

- **Chapter 1:** Context, data type, source, and sampling determine whether a summary generalizes.
- **Center, variation, and normal distributions:** CVDOT and the histogram screen prepare for formal measures and models.
- **Correlation, regression, and communication:** Scatterplots begin paired-data analysis; later displays should match the question and use honest scales.

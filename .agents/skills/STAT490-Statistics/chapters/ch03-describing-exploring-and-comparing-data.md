# Chapter 3: Statistics for Describing, Exploring, and Comparing Data

## Core Idea

Descriptive statistics summarize observed **center, variation, shape, outliers, and change over time**. No single number is sufficient: a mean can hide skewness or be pulled by an extreme value, while a compact summary can hide a trend. Choose measures for the data's level and shape, interpret original units, and compare groups on a common scale. These summaries describe the data at hand; they do not establish a population claim.

Use this workflow:

1. Check what values measure, how they were collected, and whether arithmetic is meaningful.
2. Choose a center and pair it with an appropriate spread measure.
3. Inspect shape, outliers, and time order; use z scores, percentiles, or quartiles for relative position.
4. Compare groups with five-number summaries or same-scale boxplots, then state a context-aware conclusion.

## Frameworks Introduced (exact named concepts, when to use, how)

| Named concept | When to use it | How to use it |
|---|---|---|
| **Center choices** | To report a representative value. | Mean: sample `xbar = sum(x) / n`, population `mu = sum(x) / N`; median: sorted middle; mode: most frequent value or category; midrange: `(minimum + maximum) / 2`, only a rough endpoint check. Name the statistic. |
| **Grouped and weighted means** | When observations are grouped or contributions differ. | Grouped: `xbar approx = sum(f * m) / sum(f)`; weighted: `sum(w * x) / sum(w)`. Here `f` is frequency and `m` class midpoint. |
| **Skewness** | To describe asymmetry and the longer tail. | A longer left tail is negative; a longer right tail is positive. Use a graph; mean-median order is not guaranteed. |
| **Variation choices** | To measure spread around a center. | `range = maximum - minimum`; sample `s = sqrt(sum((x - xbar)^2) / (n - 1))`; population `sigma = sqrt(sum((x - mu)^2) / N)`. Variance is `s^2` or `sigma^2` and has squared units. |
| **Range Rule of Thumb** | For a deliberately rough estimate. | Usual values are roughly `mean +/- 2 * standard deviation`; estimate `s approx = range / 4`. It is not a guarantee. |
| **Empirical Rule** | Only for approximately bell-shaped data. | About 68%, 95%, and 99.7% lie within 1, 2, and 3 standard deviations of the mean. |
| **Chebyshev's Theorem** | For any distribution when mean and standard deviation are known. | For `k > 1`, at least `1 - 1 / k^2` lie within `k` standard deviations: at least 75% for `k = 2` and 88.9% for `k = 3`. These are bounds, not exact percentages. |
| **MAD and coefficient of variation (CV)** | To describe average distance or relative spread. | `MAD = sum(abs(x - xbar)) / n`. For nonnegative ratio-scale data, sample `CV = (s / xbar) * 100%` or population `CV = (sigma / mu) * 100%`; compare percentages. |
| **z score** | To compare relative extremeness across units or distributions. | Sample `z = (x - xbar) / s`; population `z = (x - mu) / sigma`. It counts standard deviations above/below the mean; report two decimals. Roughly, `z < -2` or `z > 2` is unusual. |
| **Percentiles, quartiles, and IQR** | To describe relative position and the resistant middle half. | A data value's percentile is `(number less than x / n) * 100`. For `Pk`, sort, calculate `L = (k / 100) * n`, round nonwhole `L` up, or average positions `L` and `L + 1` when whole. `Q1 = P25`, `Q2 = P50`, `Q3 = P75`, `IQR = Q3 - Q1`; five-number summary: `minimum, Q1, median, Q3, maximum`. State the convention. |
| **Boxplot and outlier rule** | To compare center, spread, asymmetry, and unusual values. | On a common scale, box `Q1` to `Q3`, line at median, whiskers to endpoints. Flag below `Q1 - 1.5 * IQR` or above `Q3 + 1.5 * IQR`; modified whiskers stop at extreme non-outliers. |
| **Putting It All Together** | Before a description informs a decision. | Recheck context, source, sampling, center, spread, shape, outliers, time order, and practical consequences. |

### Beyond-the-basics named tools

Use a **trimmed mean** after equal tail removal; a **harmonic mean** for positive rates (`n / sum(1 / x)`); a **geometric mean** for positive growth factors (`(product of x)^(1 / n)`); and **RMS** for physical magnitude (`sqrt(sum(x^2) / n)`). A fixed sample mean leaves `n - 1` free observations. Treat ongoing durations as censored.

## Key Concepts (5-10)

1. **Center is a choice.** Mean is a balance point, median the ordered middle, mode the most frequent value, and midrange an endpoint midpoint. Median often suits skew or outliers.
2. **Pair center with variation.** Equal means can conceal different experiences; range, standard deviation, IQR, and CV answer different spread questions.
3. **Shape controls rules.** Use the empirical rule only for bell-shaped data. Chebyshev applies to any shape but gives only a lower bound.
4. **Standardize and locate.** A z score reports standard deviations below or above a mean; quartiles and boxplots compare ordered positions.
5. **Investigate outliers and weights.** An outlier may be error, rare truth, another population, or a signal; subgroup means need weights when contributions differ.

## Mental Models

- **Mean as a balance point:** An extreme observation pulls the balance point toward itself.
- **Median and IQR as resistant summaries:** The middle position and middle half change less when endpoints move.
- **Standard deviation as a typical radius:** It summarizes distances from the mean after preventing cancellation.
- **z score and boxplot as comparison tools:** One is a universal ruler; the other is a compressed landscape of center, spread, and asymmetry.

## Anti-patterns

- Name the statistic; do not call every center an "average," and do not calculate means for labels or ranks without magnitude.
- Do not confuse median with midrange or report a mean without checking shape, median, and outliers.
- Use `n - 1` for sample standard deviation, not the population denominator.
- Do not apply the empirical rule to skewed data or treat Chebyshev's lower bounds as exact.
- Sort before percentiles or quartiles and state the locator convention.
- Treat an `1.5 * IQR` flag as a prompt to verify context, not proof of an error.
- Use common boxplot scales, weighted subgroup means, preserved time order, and unrounded intermediate calculations; round final z scores to two decimals.

## Worked Example (study depth, reconstruct a center/variation/boxplot comparison)

Waiting times, in minutes, are sampled from two banks. Jefferson Valley uses one line; Providence uses individual teller lines.

```text
Jefferson Valley: 6.5, 6.6, 6.7, 6.8, 7.1, 7.3, 7.4, 7.7, 7.7, 7.7
Providence:       4.2, 5.4, 5.8, 6.2, 6.7, 7.7, 7.7, 8.5, 9.3, 10.0
```

Both samples have `n = 10` and sum to `71.5`, so both means are `xbar = 7.15` minutes. Both medians are `7.20`, modes `7.70`, and midranges `7.10`; calculate spread before concluding.

| Statistic | Jefferson Valley | Providence |
|---|---:|---:|
| Range | 1.20 min | 5.80 min |
| Sample standard deviation `s` | 0.48 min | 1.82 min |
| `Q1`, median, `Q3` | 6.7, 7.2, 7.7 | 5.8, 7.2, 8.5 |
| IQR | 1.0 min | 2.7 min |

The squared-deviation sums `2.045` and `29.865` give `s = 0.48` and `s = 1.82`. The locator convention rounds positions `2.5` and `7.5` up to positions 3 and 8 for `Q1` and `Q3`.

Draw both boxplots on one minute scale. Jefferson Valley is `6.5 -- [6.7 | 7.2 | 7.7] -- 7.7`; Providence is `4.2 -- [5.8 | 7.2 | 8.5] -- 10.0`. The Providence box and whiskers are wider. Its fences are `1.75` and `12.55`; Jefferson Valley's are `5.2` and `9.2`, so neither sample has a `1.5 * IQR` outlier. **Conclusion:** the observed centers are the same, but Providence has substantially more variation and both shorter and longer waits. This descriptive sample result does not alone justify a population claim; consider sampling, source, and the cost of long waits.

## Key Takeaways (3-7 actionable)

1. Confirm context and measurement level before calculating.
2. Report a suitable center with a suitable spread measure.
3. Use sample `s` with denominator `n - 1`, and interpret it in original units.
4. Use the empirical rule only for bell-shaped data; use Chebyshev for a distribution-free minimum.
5. Use z scores, percentiles, and quartiles for relative position.
6. Use same-scale boxplots, investigate outliers, and preserve time trends.

## Connects To

- **Data collection and graphs:** A biased sample can mislead; histograms and dotplots reveal shape, while this chapter adds numerical summaries.
- **Later methods:** Standardization returns in Chapter 6; variance supports analysis of variance and range supports process control.
- **Formal comparisons:** Descriptive bank or word-count comparisons precede tests of population means.
- **Decision making:** Use context, variability, unusual cases, and practical consequences before choosing an action.

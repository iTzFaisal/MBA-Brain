# Chapter 5: Discrete Probability Distributions

## Core Idea

A probability distribution is a theoretical model that assigns a probability to every possible value of a random variable. It describes long-run behavior, not the results of one sample. Use its center, spread, and tail probabilities to estimate expected outcomes and decide whether an observation is unusual.

This chapter focuses on counts. The binomial distribution counts successes in a fixed set of independent, two-outcome trials with a constant success probability. The Poisson distribution counts random, independent occurrences at a stable rate over a specified interval.

## Frameworks Introduced (exact named concepts, when to use, how)

- **Random Variable and Probability Distribution**: Define `X` as a numerical count or measurement produced by a chance procedure, then list its possible values. A discrete random variable has a finite or countable set of values, such as `0, 1, 2, ...`; a continuous variable can take any value along an interval. This chapter develops discrete models. A valid distribution satisfies `0 <= P(x) <= 1` and `sum P(x) = 1`, apart from rounding error. Display it with a table, formula, or probability histogram; with bars of width 1, each bar's area represents its probability.

- **Expected Value and Spread**: For any discrete distribution, calculate the probability-weighted mean and variation with

  `m = E(X) = sum[x * P(x)]`

  `s^2 = sum[(x - m)^2 * P(x)] = sum[x^2 * P(x)] - m^2`

  `s = sqrt(s^2)`.

  Expected value is a long-run average, not a promise about one trial, and it need not be a possible value. Variance uses squared units; standard deviation uses the units of `X` and is easier to interpret. When `X` is recorded as integers, normally report `m`, `s`, and `s^2` to one decimal place, retaining extra precision when needed.

- **Range Rule and Tail-Based Unusual Results**: Use `m +/- 2s` as a quick screening range, while respecting the actual possible values. For a high observation, calculate the upper tail `P(X >= x)`; for a low observation, calculate the lower tail `P(X <= x)`. Do not use only `P(X = x)`, because the result is unusual when it and more-extreme results together are rare. A tail probability of `0.05` or less is a common guideline. Under the Rare Event Rule, such a result is evidence against the assumed model, not proof of a particular alternative cause.

- **Binomial Probability Distribution**: Use this model only when all four conditions hold: (1) the number of trials `n` is fixed, (2) trials are independent, (3) each trial has exactly two relevant outcomes, and (4) the success probability `p` is constant. Define success explicitly; it need not be desirable. For sampling without replacement, the 5% guideline permits an independence approximation when the sample is no more than 5% of a much larger population. Let `x` count successes, `q = 1 - p`, and `x = 0, 1, ..., n`.

- **Binomial Probability Formula (Formula 5-5)**: For exactly `x` successes, use

  `P(X = x) = C(n, x) p^x q^(n - x) = [n! / (x! (n - x)!)] p^x q^(n - x)`.

  The powers give the probability of one particular success/failure order. `C(n, x)` counts all orders with the same number of successes. Use `binompdf(n, p, x)` for an exact probability and `binomcdf(n, p, x)` for `P(X <= x)` when technology is available; round only at the end. Once the conditions hold, use `m = np`, `s^2 = npq`, and `s = sqrt(npq)`.

- **Poisson Distribution**: Use this model when `X` counts occurrences in a defined interval of time, distance, area, volume, or a similar unit. The occurrences must be random, independent, and uniformly distributed over the interval, meaning the rate is stable across comparable portions. If `m` is the mean number of occurrences in the interval, then

  `P(X = x) = (m^x * e^(-m)) / x!`, for `x = 0, 1, 2, ...`,

  where `e` is approximately `2.71828`. A Poisson count has no finite upper limit. Its variance is `s^2 = m`, and its standard deviation is `s = sqrt(m)`. Estimate `m` from total occurrences divided by equal intervals, and rescale it only when a constant rate remains reasonable.

- **Poisson Approximation and Extensions**: Approximate a binomial distribution with Poisson when `n >= 100` and `np <= 10`, setting the Poisson mean to `m = np`; use the exact binomial when practical. The Geometric model changes the question to the trial of the first success, the Hypergeometric model handles sampling without replacement from a finite population, and the Multinomial model handles more than two categories.

## Key Concepts (5-10)

- Convert chance outcomes to numbers with a random variable, then assign probabilities to those values.
- Treat expected value as a probability-weighted center; do not round it into a value that must occur.
- Use variance for calculation and standard deviation for interpretation in the original units.
- Check assumptions before selecting a binomial or Poisson formula.
- For unusual counts, include the entire one-sided tail, not just the exact count.
- Binomial spread is `sqrt(npq)`; Poisson spread is `sqrt(m)`.
- Ordinary variation around an expected count does not by itself disprove a model.

## Mental Models

- **Infinite-run table**: A distribution is the relative-frequency table that repeated trials would approach, not a record of one finite sample.
- **Weighted balance point**: Give each possible `x` a weight of `P(x)`; `E(X)` is the resulting balance point, even when it is fractional.
- **Two layers of binomial probability**: Find one order with `p^x q^(n-x)`, then multiply by `C(n, x)` because exact counts do not specify positions.
- **Tails answer surprise**: `P(X = x)` asks how often one count occurs; a tail asks how often a count at least that extreme occurs.

## Anti-patterns

- Classifying a variable from how data were recorded instead of from its possible values.
- Accepting probabilities outside `[0, 1]` or a table whose probabilities do not total 1.
- Treating a rounded expected value as an attainable outcome or required target.
- Using `P(X = x)` alone to label a high or low result unusual.
- Using binomial shortcuts when trials are not fixed, binary, independent, or constant-probability; keep `x` and `p` tied to the same category.
- Forgetting the `C(n, x)` arrangement factor for an exact binomial count.
- Using Poisson without a defined stable-rate interval, or using its approximation rules without checking both `n >= 100` and `np <= 10`.

## Worked Example (study depth, reconstruct a binomial or Poisson calculation)

### Five Green-Pod Peas

Each offspring pea has probability `p = 0.75` of a green pod. For `n = 5` offspring, find the probability of exactly three green-pod peas and assess whether one is unusually low.

The trials are fixed, independent, binary, and have constant `p`, so use a binomial model. Count green pods as success: `x = 3`, `q = 0.25`.

`P(X = 3) = C(5, 3)(0.75)^3(0.25)^2`

`= 10(0.421875)(0.0625) = 0.263671875 ~= 0.264`.

The factor `C(5, 3) = 10` counts the possible positions of the three successes; multiplying one order alone would be incomplete. Technology verifies this with `binompdf(5, 0.75, 3)`.

The center and spread are

`m = np = 5(0.75) = 3.75`, and `s = sqrt(npq) = sqrt(0.9375) ~= 0.968`.

For one green pod, use the lower tail rather than the exact probability:

`P(X <= 1) = P(X = 0) + P(X = 1)`

`= (0.25)^5 + 5(0.75)(0.25)^4 = 0.015625 ~= 0.016`.

Because `0.016 <= 0.05`, one is unusually low under the model. This is evidence that the assumptions may not fit; it does not prove why the result occurred. The range check agrees: `m +/- 2s` is approximately `1.81` to `5.69`, and `1` is below it.

## Key Takeaways (3-7 actionable)

- Define `X`, its possible values, and the counted category before calculating.
- Validate all four binomial conditions or all four Poisson requirements.
- Keep exact probabilities separate from cumulative tails, and avoid intermediate rounding.
- Use `m = np`, `s^2 = npq`, and `s = sqrt(npq)` only for binomial counts; use the Poisson formula with a defined interval and mean `m`.
- Judge an observed count by its appropriate tail or its variation around the mean, not by its distance from expectation alone.

## Connects To

- **Chapter 4 probability**: Binomial probability combines the multiplication rule for one order with combinations for all orders; complements support tail calculations.
- **Chapters 2 and 3 descriptive statistics**: Probability histograms and probability-weighted means, variances, and standard deviations extend familiar summaries to theoretical distributions.
- **Chapter 6 continuous probability distributions**: This chapter establishes discrete models before continuous models.
- **Inference and applications**: Rare-event reasoning supports hypothesis testing; expected value supports decisions, and Poisson models support arrivals, queues, disease counts, and other rate problems.

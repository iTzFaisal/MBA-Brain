# Chapter 6: Normal Probability Distributions

## Core Idea

Continuous probability is represented by area under a density curve. The normal distribution is symmetric, bell-shaped, and completely determined by its mean `mu` and standard deviation `sigma`. Standardization puts different normal distributions on one reference scale.

Use this workflow:

1. Sketch the curve, mark the boundaries, and shade the requested area.
2. Convert each nonstandard value to a z score and use cumulative-left areas.
3. For a percentile, work backward from the left area to z and then to x.
4. Treat a statistic as a random variable with its own sampling distribution and spread.
5. Check CLT, binomial-approximation, sampling, and normality conditions before calculating.

## Frameworks Introduced (exact named concepts, when to use, how)

- **Density Curve and Uniform Distribution:** For a continuous variable, total area is 1, heights are nonnegative, and `P(a <= X <= b)` is the area over the interval. Since `P(X = a) = 0`, endpoint inclusion does not matter. A uniform model is a rectangle, so probability is `width * height`.

- **Normal Distribution (Formula 6-1):** Use for a symmetric, bell-shaped continuous variable:

  `f(x) = exp(-0.5 * ((x - mu) / sigma)^2) / (sigma * sqrt(2*pi))`

- **Standard Normal Distribution:** This reference distribution has `mu = 0` and `sigma = 1`. Table A-2 reports `P(Z <= z) = Phi(z)`, a cumulative area, not a z score. Thus `P(Z > a) = 1 - Phi(a)` and `P(a < Z < b) = Phi(b) - Phi(a)`.

- **z Score (standard score; Formula 6-2):** Convert a normal value with `z = (x - mu) / sigma`. It is signed distance from the mean in standard-deviation units. Reverse it with `x = mu + z * sigma`.

- **Finding Areas and Probabilities from Known Values:** Sketch first, standardize boundaries, then use a left area, its complement, or a difference. Read wording carefully: `at least` includes the boundary, while `more than` excludes it.

- **Finding a z Score from a Known Area and Critical Values:** Convert the stated percentile or tail to cumulative-left area, locate the closest table entry, and read z. A left-half percentile has a negative z. For `z_alpha`, alpha is the right-tail area, so use left area `1 - alpha`; for example, `z_0.025 = 1.96`. Recover a raw cutoff with `x = mu + z * sigma`; `-1.96` to `1.96` contains about 95%.

- **Sampling Distribution of a Statistic:** Repeated random samples of size n produce a distribution of `xbar`, `s^2`, or `p-hat`, separate from the raw observations. Random sampling matters because a large convenience or biased sample can still be unrepresentative. `s^2` targets `sigma^2`; `p-hat` targets p and can be approximately normal under suitable conditions. Variance distributions may be right-skewed.

- **Sampling Distribution of the Mean and Standard Error:** For sample means, `mu_xbar = mu` and `sigma_xbar = sigma / sqrt(n)`, the **Standard Error of the Mean**. Averaging narrows the distribution as n increases. `xbar`, `s^2`, and `p-hat` are unbiased targets; median, range, and s are presented as biased, although s's bias is often small in large samples.

- **Central Limit Theorem:** For simple random samples, `xbar` approaches normality as n grows while `mu_xbar = mu` and `sigma_xbar = sigma / sqrt(n)`. A normal population gives an exact normal mean for every n. Otherwise use the guideline `n > 30`; strongly nonnormal populations may require more, and `n <= 30` does not support these methods.

- **Correction for a Finite Population:** When sampling without replacement and `n > 0.05N`, multiply the usual standard error by

  `sqrt((N - n) / (N - 1))`

  so `sigma_xbar = (sigma / sqrt(n)) * sqrt((N - n) / (N - 1))`. Do not use it with replacement, an effectively infinite population, or when `n <= 0.05N`.

- **Rare Event Rule for Inferential Statistics:** If an observed result has an exceptionally small probability, often below 0.05, under a claim, regard the claim as questionable; this does not prove it false or establish causation.

- **Normal Distribution as an Approximation to the Binomial Distribution and Continuity Correction:** For a binomial count, verify fixed n, independent trials, two outcomes, constant p, `q = 1 - p`, and `np >= 5`, `nq >= 5`. Then use a normal model with `mu = np` and `sigma = sqrt(npq)`. Apply half-unit boundaries: `X >= x` uses `x - 0.5`; `X > x` uses `x + 0.5`; `X <= x` uses `x + 0.5`; `X < x` uses `x - 0.5`; `X = x` uses `[x - 0.5, x + 0.5]`; and `a <= X <= b` uses `[a - 0.5, b + 0.5]`. If either count condition fails, use the exact binomial method or technology.

- **Normal Quantile Plot and Normality Diagnostics:** Inspect a histogram, outliers, then a normal quantile plot. Reject a dramatically non-bell-shaped histogram or more than one outlier; one outlier warrants caution. Rough symmetry and points near a straight line support normality. For sorted `x_(i)`, `i = 1, ..., n`, use left areas `(2i - 1) / (2n)`, convert to z, and plot `(x_(i), z_i)`; large samples require stricter linearity. A justified `log(x + 1)` transformation may produce approximately normal, lognormal-source data, but must be rediagnosed.

## Key Concepts (5-10)

1. **Area is probability.** Density height alone is not probability, and an exact continuous value has probability 0.
2. **Standardization changes the ruler, not the area.** z expresses location in standard-deviation units; Table A-2 is cumulative-left.
3. **A statistic has its own distribution.** For `xbar`, use the standard error, not the population `sigma`.
4. **Unbiased does not mean exact.** It describes the center of repeated estimates, not one sample's accuracy.
5. **The CLT has conditions.** Population shape, n, and random sampling determine whether a normal approximation is defensible.
6. **Discrete counts need half-unit boundaries.** Continuity correction connects binomial counts to normal areas.
7. **Normality requires converging evidence.** Histogram, outlier, and quantile-plot results should agree.

## Mental Models

- **Standardization as a change of ruler:** Center at zero, then measure in standard deviations.
- **Sampling distribution as machine output:** Repeated samples produce a new center and spread for the statistic.
- **Averaging as noise reduction:** `xbar` stays centered at `mu`, while its standard error shrinks by `sqrt(n)`.
- **Continuity correction as half-unit ownership:** Each integer count owns the interval halfway to its neighbors.

## Anti-patterns

- Read a nonstandard x directly from the z table or confuse a z score with an area; standardize first.
- Use `sigma` instead of `sigma / sqrt(n)` for a sample mean.
- Apply the CLT to a nonnormal population with `n <= 30`, or treat `n > 30` as a guarantee for extreme nonnormality.
- Approximate a binomial without checking `np >= 5` and `nq >= 5`, omit continuity correction, or treat `at least x` as `more than x`.
- Assume a large, convenient, or voluntary-response sample is representative.
- Declare normality from one attractive histogram or ignore an outlier; use all diagnostics and treat a small probability as evidence, not proof.

## Worked Example

**Water-taxi weights: a sample mean.** Male weights are normal with `mu = 172 lb` and `sigma = 29 lb`. Find the probability that 20 randomly selected men have mean weight above 175 lb.

Because the population is normal, `xbar` is normal for `n = 20`; no `n > 30` rule is needed. Its mean and standard error are

`mu_xbar = mu = 172`

`sigma_xbar = sigma / sqrt(n) = 29 / sqrt(20) = 6.4846`

Standardize with the standard error:

`z = (175 - 172) / 6.4846 = 0.4626, approximately 0.46`

Table A-2 gives `Phi(0.46) = 0.6772` to the left. Therefore,

`P(xbar > 175) = 1 - 0.6772 = 0.3228`.

Technology gives about `0.3218`. The result concerns the group's average, not every individual's weight. Since 175 is above the mean, a probability below 0.50 is a useful direction check.

## Key Takeaways (3-7 actionable)

1. Sketch and shade before calculating; it prevents tail and endpoint errors.
2. Use `z = (x - mu) / sigma` for one observation and `z = (xbar - mu) / (sigma / sqrt(n))` for a mean.
3. For a percentile, find cumulative-left area, locate z, and solve `x = mu + z * sigma`.
4. Before using the CLT, check population shape, n, random sampling, and finite-population correction.
5. Before a binomial normal approximation or normal-population method, verify count conditions or compare histogram shape, outliers, and a quantile plot.

## Connects To

- **Earlier foundations:** Chapters 2-5 supply distributions, variation, probability, rare-event reasoning, and binomial models.
- **Chapter 7:** Sampling distributions, unbiased estimators, standard error, percentiles, and the CLT support estimation.
- **Chapter 8:** Rare-event reasoning and standardized sampling distributions support hypothesis tests.
- **Applications:** Normal percentiles guide design and safety limits; diagnostics and transformations determine whether later normal-population methods are defensible.

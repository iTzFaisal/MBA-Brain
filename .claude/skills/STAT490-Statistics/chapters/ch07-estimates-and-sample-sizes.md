# Chapter 7: Estimates and Sample Sizes

## Core Idea

Use a sample to estimate an unknown population parameter. A **point estimate** gives one value; an **interval estimate** gives a range and procedure reliability. Estimate `p`, `mu`, `sigma`, and `sigma^2`, then plan a sample for a desired margin of error.

For proportions and means, use:

```text
estimate +/- (critical value)(standard error)
```

Variance and standard-deviation intervals use asymmetric chi-square, not `estimate +/- E`. Check design and assumptions first: a large sample cannot remove selection bias.

## Frameworks Introduced (exact named concepts, when to use, how)

### Point Estimate

Use `phat` for `p`, `xbar` for `mu`, and `s^2` for `sigma^2`. The sample standard deviation `s` estimates `sigma`, although it is slightly biased; the bias is small for large samples.

### Confidence Interval (or Interval Estimate)

Use a range when a point estimate hides uncertainty. For a proportion or mean, calculate `E` and report `estimate - E < parameter < estimate + E`, or `(lower, upper)`.

### Confidence Level (Degree of Confidence, or Confidence Coefficient)

Set `C = 1 - alpha`; common choices are 90%, 95%, and 99%. A 95% CI means that repeated use of the procedure would capture the fixed parameter in about 95% of intervals. It is not a 95% probability statement about an already-calculated interval.

### Critical Value

For a two-sided interval, split `alpha` between tails. `z_(alpha/2)` has area `alpha/2` to its right; common values are 1.645, 1.96, and 2.576 for 90%, 95%, and 99%. Use `t_(alpha/2)` with `df = n - 1` for an unknown-`sigma` mean. Variance intervals use two chi-square values; right-tail tables reverse the visual left/right lookup.

### Margin of Error (Maximum Error of the Estimate)

Use `E` for the maximum likely difference between statistic and parameter:

```text
E = critical value * standard error

Proportion:         E = z_(alpha/2) * sqrt(phat*qhat/n)
Mean, sigma known:  E = z_(alpha/2) * sigma/sqrt(n)
Mean, sigma unknown: E = t_(alpha/2, n-1) * s/sqrt(n)
```

Here `qhat = 1 - phat`; three percentage points means `E = 0.03`, not `3`.

### Confidence Interval for Estimating a Population Proportion `p`

Use the standard-Wald interval when the sample is simple random, binomial conditions hold (fixed independent trials, two outcomes, constant probability), and there are at least 5 successes and 5 failures:

```text
phat - E < p < phat + E
E = z_(alpha/2) * sqrt(phat*qhat/n)
```

Verify conditions, find `z`, calculate `E`, form both limits, and round only at the end. Adjusted-Wald or Wilson score intervals can perform better for small samples.

### Finding the Sample Size Required to Estimate a Population Proportion

For desired `E`, use a prior study, pilot study, or defensible planning estimate when available:

```text
n = [z_(alpha/2)]^2 * phat*qhat / E^2       (Formula 7-2)
n = [z_(alpha/2)]^2 * 0.25 / E^2            (Formula 7-3, no estimate)
```

With no estimate, `phat = qhat = 0.5` is conservative because their product is largest. Round `n` up; for a large population, confidence, `E`, and variability drive `n`, not population size.

### Confidence Interval for Estimating a Population Mean (with `sigma` Known)

Use `z` when `sigma` is known and the simple random sample comes from a normal population, or when `n >= 30` makes `xbar` approximately normal. The large-sample rule is not a guarantee for extreme nonnormality:

```text
xbar - E < mu < xbar + E
E = z_(alpha/2) * sigma/sqrt(n)
```

### Finding the Sample Size Required to Estimate a Population Mean

When `sigma` is known or estimated conservatively:

```text
n = [z_(alpha/2) * sigma / E]^2                  (Formula 7-4)
```

Round up. If unknown, estimate `sigma` with `range/4`, pilot data, or a previous study. Overestimating `sigma` is safer; halving `E` multiplies `n` by four.

### Student t Distribution

Use Student `t` when `sigma` is unknown and mean assumptions are reasonable. Replacing `sigma` with `s` adds uncertainty, so t has wider small-sample tails; it approaches z as `n` grows.

### Confidence Interval for Estimating a Population Mean (with `sigma` Not Known)

Use a simple random sample from a normal population, or `n >= 30` from a population without strong skew or problematic outliers:

```text
xbar - E < mu < xbar + E
E = t_(alpha/2, df=n-1) * s/sqrt(n)
```

For a small, strongly skewed or outlier-contaminated population, use bootstrap or nonparametric methods instead.

### Choosing Between `z` and `t`

For a CI for `mu`, use `z` when `sigma` is known and `t`, `df = n - 1`, when `sigma` is unknown, even for large `n`. Require simple random sampling and a normal population or adequate large-sample behavior. A small, strongly nonnormal sample calls for neither method.

### Chi-Square Distribution

Use chi-square for `sigma^2` or `sigma` when a simple random sample comes from a normal population:

```text
chi-square = (n - 1)*s^2 / sigma^2,       df = n - 1
```

Chi-square is nonnegative and skewed, with shape depending on `df`. Non-normality can cause serious errors even for large `n`; inspect a histogram and normal quantile plot.

### Confidence Interval for Estimating a Population Standard Deviation or Variance

Let `chi^2_R` have area `alpha/2` to its right and `chi^2_L` have area `alpha/2` to its left. With a right-tail table, look up `alpha/2` for `chi^2_R` and `1 - alpha/2` for `chi^2_L`:

```text
Variance: (n-1)*s^2/chi^2_R < sigma^2 < (n-1)*s^2/chi^2_L

SD: sqrt((n-1)*s^2/chi^2_R) < sigma
    < sqrt((n-1)*s^2/chi^2_L)
```

Use `df = n - 1`, calculate both limits separately, and take square roots only for `sigma`. It is asymmetric, so do not write it as `s +/- E`. Simple random sampling and normality are essential.

### Determining Sample Size for `sigma` or `sigma^2`

Use Table 7-2. Select confidence, target (`sigma` or `sigma^2`), and relative accuracy:

| Confidence | Target within 20% | Minimum `n` |
|---|---:|---:|
| 95% | `sigma^2` | 211 |
| 95% | `sigma` | 48 |
| 99% | `sigma^2` | 369 |
| 99% | `sigma` | 85 |

Higher confidence or smaller error requires a larger sample.

### Finite Population Correction (Beyond the Basic Formulas)

For sampling without replacement when `n > 0.05N`, multiply the standard error by `sqrt((N-n)/(N-1))`. The planning formulas are:

```text
Proportion: n = N*phat*qhat*z^2 / (phat*qhat*z^2 + (N-1)*E^2)
Mean:       n = N*sigma^2*z^2 / ((N-1)*E^2 + sigma^2*z^2)
```

## Key Concepts (5-10)

1. **Parameter versus statistic:** `p`, `mu`, `sigma`, and `sigma^2` describe populations; `phat`, `xbar`, `s`, and `s^2` come from samples.
2. **Point versus interval:** a point is concise; a CI adds precision and confidence.
3. **Confidence is procedural:** the parameter is fixed; intervals vary across samples.
4. **Margin of error has levers:** confidence raises the critical value, `n` lowers standard error, and variability raises `E`.
5. **Match the distribution:** proportion -> z; known-`sigma` mean -> z; unknown-`sigma` mean -> t; variance/SD -> chi-square.
6. **Assumptions and rounding matter:** require credible design and shape conditions; round limits at the end and `n` upward.

## Mental Models

- **Point versus fence:** `phat` or `xbar` is the center; `E` shows sampling movement. A 95% procedure captures the fixed parameter in about 95% of repetitions.

## Anti-patterns

- Say “95% confident that the interval contains the parameter,” not “a 95% probability that the fixed parameter is in this interval”; a CI is not the spread of observations.
- Do not use `0.95` or `0.05` as a critical value; a two-sided 95% z interval uses `1.96`, and do not skip tail splitting or use `3` instead of `0.03`.
- Do not use a Wald proportion interval with fewer than 5 successes or failures, z for an unknown-`sigma` mean, z/t for a small strongly nonnormal sample, chi-square without normality, or a sample size rounded down.

## Worked Example (study depth, reconstruct one confidence interval/sample-size calculation)

### A 95% proportion CI and its sample-size plan

A simple random poll has `n = 1501` adults and `phat = 0.70`; the binomial conditions are treated as satisfied, with about 1051 successes and 450 failures.

For 95% confidence, `alpha = 0.05`, `z_(alpha/2) = 1.96`, and `qhat = 0.30`:

```text
E = 1.96*sqrt((0.70)(0.30)/1501) = 0.023183
CI = 0.70 +/- 0.023183 = (0.676817, 0.723183)
   = (0.677, 0.723) after final rounding
```

We are 95% confident that the interval contains the population proportion. It supports a majority response because it is entirely above 0.50, subject to the assumptions.

To plan a new 95% poll with `E = 0.03`, use a prior estimate `phat = 0.73`, `qhat = 0.27`:

```text
n = (1.96^2)(0.73)(0.27)/(0.03^2)
  = 841.3104 -> 842
```

Without a planning estimate, use `0.25`: `1067.1111 -> 1068`. Upward rounding preserves the requested error.

## Key Takeaways (3-7 actionable)

1. Check design and assumptions before choosing a formula.
2. Use `phat`, `xbar`, `s^2`, and `s` as point estimates.
3. Match z, t, or chi-square to the parameter and `sigma` status.
4. Interpret confidence as a repeated-procedure success rate.
5. Convert percentage points to decimals and round required `n` upward.

## Connects To

- **Related methods:** sampling design determines representativeness; descriptive statistics supply `phat`, `xbar`, `s`, and `s^2`; binomial/normal models, tests, bootstrap, finite-population, and two-sample methods extend this framework.

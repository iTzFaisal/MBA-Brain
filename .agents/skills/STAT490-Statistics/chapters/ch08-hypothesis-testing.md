# Chapter 8: Hypothesis Testing

## Core Idea

Hypothesis testing evaluates a population claim with sample data. Begin with the **null hypothesis** (`H0`), usually equality, and reject it only when the observed or more extreme result is sufficiently unlikely under that model, as stated by the **Rare Event Rule for Inferential Statistics**. A test proves neither hypothesis. Statistical significance concerns detectability; practical significance concerns whether the effect matters.

## Frameworks Introduced (exact named concepts, when to use, how)

### Rare Event Rule for Inferential Statistics

Assume `H0`; reject when the observed or more extreme result has a small probability under it and the preselected `alpha`.

### Null and Alternative Hypotheses

Write a claim about `p`, `mu`, `sigma`, or variance and its opposite first. Put equality in `H0` (`p = p0`, `mu = mu0`, or `sigma = sigma0`) and `>`, `<`, or `!=` in `H1` (also `Ha`). Thus `mu <= 195` gives `H0: mu = 195`, `H1: mu > 195`. A claim with equality is `H0`; no test proves it true.

### Test Statistic

Standardize distance from the null value. For a proportion, `q0 = 1 - p0`:

```text
z = (p-hat - p0) / sqrt(p0*q0/n)
```

For a mean with known `sigma`:

```text
z = (x-bar - mu0) / (sigma/sqrt(n))
```

For a mean with unknown `sigma`:

```text
t = (x-bar - mu0) / (s/sqrt(n)),       df = n - 1
```

For a population standard deviation or variance:

```text
chi-square = (n - 1)*s^2 / sigma0^2,   df = n - 1
```

Use `p0`, not `p-hat`, in the proportion standard error and the claimed variance in the chi-square denominator.

### Critical Region (Rejection Region)

The critical region rejects `H0`: `>` is right-tailed, `<` left-tailed, and `!=` two-tailed. Let `H1`, not the observed direction, select the tail.

### Significance Level

Choose `alpha` before results. It is the probability of rejecting a true `H0` (Type I error). Common values are `0.10`, `0.05`, and `0.01`.

### Critical Value

Choose the distribution, `df`, tails, and alpha allocation. At `alpha = 0.05`, normal cutoffs are `z = 1.645` right-tailed and `z = +/-1.96` two-tailed. t and chi-square cutoffs depend on `df`.

### P-value

The P-value is the probability, assuming `H0`, of a statistic at least as extreme in the direction of `H1`: left area, right area, or both tails for a symmetric two-tailed z/t test. For chi-square, double the smaller tail probability.

```text
P-value <= alpha  -> reject H0
P-value > alpha   -> fail to reject H0
```

It is not the probability that `H0` is true or that results were caused by chance.

### Two-Tailed Test, Left-Tailed Test, and Right-Tailed Test

Classify from `H1`: alpha goes upper for an increase, lower for a decrease, and into both tails for a difference. Never choose after seeing the sample.

### P-value Method

1. Translate the claim and opposite into `H0` and `H1`.
2. Choose `alpha`; check design, independence, distribution, and sample-size conditions.
3. Calculate and compare the statistic and P-value, decide, and state the result in context.

### Traditional Method

Repeat the setup and checks, calculate the statistic, identify the region, and reject only inside it. A valid continuous test agrees with the P-value method.

### Confidence Interval Method

For two tails at `alpha`, use a `(1 - alpha)` interval; for one tail, use `(1 - 2*alpha)`, such as 90% at `alpha = 0.05`. Reject a value outside it. Proportion intervals use a sample-based standard error, unlike the null-based formal test; use P-values or critical values to test proportions.

### Type I Error and Type II Error

A **Type I error** rejects a true `H0` (probability `alpha`). A **Type II error** fails to reject a false `H0` (probability `beta` for a specified alternative).

| Reality | Reject `H0` | Fail to reject `H0` |
|---|---|---|
| `H0` true | Type I error | Correct decision |
| `H0` false | Correct decision | Type II error |

### Power of a Hypothesis Test

```text
power = 1 - beta
```

Power is the probability of rejecting a false null for a specified alternative. It increases with sample size, effect size, lower variability, and larger alpha. A common target is `0.80`; plan `n` around a meaningful effect.

### One-Proportion z Test: Normal Approximation to the Binomial

Use for one binary proportion claim. Require an appropriate random/design-based sample; fixed independent binary trials with constant probability; and under `H0`, `n*p0 >= 5` and `n*q0 >= 5`. Compute `p-hat = x/n` and the null-based z. With small counts, use the exact binomial test: `P(X >= x)` right or `P(X <= x)` left under `p0`.

### One-Mean z Test: sigma Known

Use when population `sigma` is known. Require a simple random sample and a normal population or `n >= 30`; with moderate samples, avoid serious nonnormality and outliers. Use z. Large `n` cannot repair bias.

### One-Mean t Test: sigma Not Known

Use when `sigma` is unknown and estimated by `s`. Require a simple random sample and a normal population or `n >= 30`; for small samples, inspect outliers and normality. Use t with `df = n - 1`; use a nonparametric or bootstrap method when severe skew or outliers invalidate it.

### Chi-Square Test for a Standard Deviation or Variance

Use for one claim about `sigma` or `sigma^2` from a normal population. Require a simple random sample and strict normality. Large chi-square values support a right tail, small values a left tail, and split alpha for two tails. Use the claimed variance, or `sigma0^2`, in the denominator.

### Conclusion Wording

Return to the claim. If it is `H1`, write "There is sufficient evidence to support the claim that ... ." after rejection and "There is not sufficient evidence to support the claim that ... ." otherwise. For a claim in `H0`, write "There is sufficient evidence to warrant rejection of the claim that ... ." or "There is not sufficient evidence to warrant rejection of the claim that ... ." Never write "accept `H0`" or "the null is true."

### Statistical Significance and Practical Significance

Statistical significance is a small P-value relative to alpha. Practical significance asks whether effect size, direction, units, precision, cost, and consequences matter. Report an estimate and, when useful, an interval; compare it with a domain threshold. A tiny effect can be significant, while an important effect can miss when power is low.

## Key Concepts (5-10)

1. **The null is a working model, not a conclusion.** Equality defines its distribution.
2. **The alternative controls the tail.** `>`, `<`, and `!=` mean right, left, and two-tailed.
3. **Use the null standard error.** Proportions use `sqrt(p0*q0/n)`.
4. **Assumptions determine defensibility.** Check design, counts, normality, sample size, and `sigma`.
5. **A P-value measures incompatibility, not truth.** Failing to reject is not accepting.

## Mental Models

### The Courtroom Model

Treat `H0` as a default account: rejection overturns it; non-rejection means insufficient evidence.

### The Surprise Meter

The statistic measures null distance; the P-value converts it to a tail probability.

### The Tail Compass

Read `H1`: `>` right, `<` left, and `!=` both ways.

### Two Gates: Design, Then Mathematics

Check design and distribution before arithmetic; arithmetic cannot repair bias.

### Signal Versus Scale

Testing detects signal above noise; practical significance asks whether it matters.

### Decision Matrix, Not a Binary Truth Machine

Every test has two correct outcomes and two errors; alpha controls Type I risk, beta Type II risk, and power.

## Anti-patterns

- Put equality in `H0`, not `H1`; do not choose a tail, alpha, or method after seeing data.
- Do not turn "different" into "greater" or "less," use `p-hat` in the null standard error, or misread the P-value as truth, chance, or `p`.
- Do not say "accept," "prove," or "the null is true," or report only reject/fail to reject.
- Do not use z when `sigma` is unknown, t without small-sample checks, or chi-square on a substantially nonnormal population.
- Do not assume a large or voluntary-response sample removes bias.
- Do not call every statistically significant result practically important.

## Worked Example (study depth, reconstruct a full claim test)

### XSORT Gender-Selection Claim: One Proportion

**Question.** In a trial, 668 of 726 babies were girls. At `alpha = 0.05`, test whether XSORT raises the proportion above `0.50`.

### 1. Define the parameter and claim

Let `p` be the proportion of girls among XSORT births. Claim: `p > 0.50`.

### 2. Form the hypotheses

```text
H0: p = 0.50
H1: p > 0.50
```

The claim is `H1`; reject `H0`.

### 3. Check the requirements

The outcome is binary and `n*p0 = n*q0 = 726(0.50) = 363 >= 5`; with appropriate independent trials, the normal approximation is adequate. Self-selection limits generalization.

### 4. Compute the statistic

```text
p-hat = 668/726 = 0.920
z = (0.920 - 0.500) / sqrt((0.50)(0.50)/726)
  = 22.63  (approximately)
```

`H1` says "greater than," so this is right-tailed.

### 5. Find the P-value and decide

The area right of `z = 22.63` is below `0.0001`; reject because `P-value <= 0.05`. The critical method agrees: `22.63 > 1.645`.

### 6. State the conclusion in context

There is sufficient evidence to support the claim that, for the population represented by the study, the proportion of girls among XSORT births exceeds `0.50`. The result is statistically significant, but it does not prove broader safety, causal, or value claims.

### 7. Assess practical significance

The estimate is 92.0%, 42 percentage points above 50%, a large difference. Assess precision, risks, ethics, and generalizability. If P-value exceeded 0.05, report insufficient evidence, not proof of no effect.

## Key Takeaways (3-7 actionable)

1. Translate the claim: equality in `H0`, direction or difference in `H1`.
2. Check design, independence, normality, counts, and `sigma`.
3. Match parameter to distribution: proportion -> z/binomial; mean -> z/t; spread -> chi-square.
4. Choose alpha in advance; apply P-value or critical-region rules consistently.
5. State context, effect size, uncertainty, consequence, and power.

## Connects To

- **Descriptive statistics:** `p-hat`, `x-bar`, and `s` summarize samples; tests infer about `p`, `mu`, and `sigma`.
- **Sampling distributions and binomial probability:** They justify normal/t references and proportion tests.
- **Intervals, t, chi-square, design, and power:** They add magnitude, handle spread, protect validity, and guide planning.

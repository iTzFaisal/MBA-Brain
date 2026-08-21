# Chapter 13: Nonparametric Statistics

## Core Idea

Use nonparametric methods when normality is doubtful, data are ordinal/nominal, or ranks are natural. They are **distribution-free**, not assumption-free: design, independence, pairing, symmetry, sample size, and order matter.

Trade-off: the sign test keeps direction; rank tests keep order but not distances. Parametric tests are more efficient when assumptions hold; nonparametric tests buy robustness.

### Design-to-test router

- One sample or matched pairs with a median claim: use sign when only direction is trustworthy or symmetry is doubtful; use signed-ranks when magnitudes help and differences are approximately symmetric.
- Two independent samples: use the Wilcoxon rank-sum test, also called Mann-Whitney U.
- Three or more independent samples: use Kruskal-Wallis.
- Paired measurements used to test association: use Spearman's rank correlation test.
- An ordered binary sequence whose randomness is questioned: use the runs test.

State directional hypotheses, verify design, choose the tail/cutoff, and treat failure to reject as insufficient evidence, not proof of `H0`.

## Frameworks Introduced (exact named concepts, when to use, how)

### Ranks and handling ties

**When to use:** Ranks support signed-ranks, rank-sum, Kruskal-Wallis, and Spearman. Sort and rank from 1 upward; tied observations receive the mean of their positions. Rank absolute differences for signed-ranks, both samples for rank-sum, all groups for Kruskal-Wallis, and variables separately for Spearman.

### Sign Test

**When to use:** Use the **Sign Test** for a one-population median, matched-pair differences, or two-category nominal data. Typical nulls are median difference `= 0` and `p = 0.5`.

Compute first minus second, or observation minus claimed median; label nominal categories `+` and `-`. Discard zeros. Let `n` be the remaining count and `x = min(number of +, number of -)`. For `n <= 25`, use exact Table A-7 and reject when `x` is at or below its cutoff. For `n > 25`, use:

`z = [(x + 0.5) - n/2] / sqrt(n/4)`

`+0.5` is the continuity correction; `x` is less frequent, so use the left tail. Under `H0`, `P(+) = P(-) = 0.5`; double the probability of `x` or fewer less-frequent signs for an exact two-tailed P-value. Confirm the dominant sign supports one-tailed `H1`. Primary handling discards zeros; some conventions split an even number and discard one of an odd number. State alternatives.

### Wilcoxon Signed-Ranks Test for Matched Pairs

**When to use:** Use the **Wilcoxon Signed-Ranks Test for Matched Pairs** for a paired median claim, or a one-sample claim after subtracting the claimed median. It requires a simple random paired sample and approximately symmetric differences, not normality.

Compute `d = first - second`; discard `d = 0`, rank `|d|`, average ties, and restore signs. Let `W+` be the positive-rank sum, `|W-|` the absolute negative-rank sum, and `T = min(W+, |W-|)`. For `n` nonzero differences, use exact Table A-8 if `n <= 30`; reject when `T` is at or below its cutoff. If `n > 30`, use

`z = [T - n(n + 1)/4] / sqrt[n(n + 1)(2n + 1)/24]`

and the appropriate normal cutoff. Original signs give direction.

### Wilcoxon Rank-Sum Test for Two Independent Samples

**When to use:** Use the **Wilcoxon Rank-Sum Test for Two Independent Samples** (Mann-Whitney U) for two independent simple random samples. It handles ordinal data; equal-median language requires similarly shaped populations.

Pool and rank both samples, averaging ties. For Sample 1, let `n1` be its size, `R` its rank sum, and `n2` the other size. Under equal location,

`mu_R = n1(n1 + n2 + 1)/2`

`sigma_R = sqrt[n1 n2(n1 + n2 + 1)/12]`

`z = (R - mu_R) / sigma_R`

If either sample has 10 or fewer observations, use exact tables; otherwise use the normal approximation and alternative tail. Positive `z` means Sample 1 has higher ranks. Equivalently,

`U = n1 n2 + n1(n1 + 1)/2 - R`, with `z = [U - n1 n2/2] / sqrt[n1 n2(n1 + n2 + 1)/12]`.

Switching labels reverses `z`, not the conclusion.

### Kruskal-Wallis Test

**When to use:** Use the **Kruskal-Wallis Test**, or **H test**, for at least three independent simple random samples comparing locations/equal medians under comparable shapes. Each group needs at least five observations for chi-square approximation.

Pool observations, average tied ranks, and let `n_i`, `R_i`, `N`, and `k` denote group size, rank sum, total size, and group count:

`H = [12 / (N(N + 1))] * sum(R_i^2 / n_i) - 3(N + 1)`

Compare `H` right-tailed with chi-square `df = k - 1`. With many ties:

`H_corrected = H / [1 - sum(t_j^3 - t_j)/(N^3 - N)]`,

Here `t_j` is each tied group's size. Rejection means medians are not all equal, not which groups differ.

### Rank Correlation

**When to use:** Use **Rank Correlation**, or **Spearman's rank correlation test**, for paired data testing monotone association. It suits ordinal/rank or nonnormal data; pairs should be a simple random sample.

Rank each variable separately and average ties. With no ties,

`r_s = 1 - [6 sum(d^2) / (n(n^2 - 1))]`.

With ties, calculate ordinary correlation on the ranks:

`r_s = [n sum(xy) - sum(x)sum(y)] / sqrt{[n sum(x^2) - (sum(x))^2][n sum(y^2) - (sum(y))^2]}`

Test `H0: r_s = 0` against the stated alternative. For `n <= 30`, use Table A-9; for `n > 30`, use `r_s = +/- z / sqrt(n - 1)`. The sign gives direction, not causation; inspect a scatterplot.

### Runs Test for Randomness

**When to use:** Use the **Runs Test for Randomness** when order matters and observations fall into two categories. For numerical data, classify above/below a chosen mean or median and delete equals.

Count category sizes `n1`, `n2`, and runs `G`. Test `H0: the sequence is random` against `H1: it is not random`. If `n1 <= 20`, `n2 <= 20`, and `alpha = 0.05`, use Table A-10; reject at or beyond either critical value. Otherwise use

`mu_G = 2n1 n2/(n1 + n2) + 1`

`sigma_G = sqrt[(2n1 n2)(2n1 n2 - n1 - n2) / ((n1 + n2)^2(n1 + n2 - 1))]`

`z = (G - mu_G) / sigma_G`, with two-tailed normal cutoffs. Few runs suggest clustering/trend; many suggest alternation. It tests order, not frequency.

## Key Concepts (5-10)

1. **Distribution-free is not assumption-free:** design and method-specific conditions remain essential.
2. **Structure selects the test:** pairing, independence, group count, association, and order come first.
3. **Ties receive average ranks:** arbitrary ranks change the statistic.
4. **Sign sacrifices power for simplicity; signed-ranks adds magnitude** but requires approximately symmetric differences.
5. **Independent samples are not pairs:** rank-sum pools; signed-ranks uses within-pair differences.
6. **Thresholds select inference:** sign `n <= 25`, signed-ranks `n <= 30`, rank-sum exact if either sample `<= 10`, and Kruskal-Wallis chi-square when each group has at least five.
7. **Runs tests order; Spearman tests association:** neither tests frequency or causation.

## Mental Models

- **Robustness ladder:** sign uses direction; signed-ranks adds paired magnitude; rank-sum compares two pooled distributions; Kruskal-Wallis extends this to several groups.
- **Pool, rank, compare:** independent-group tests create a common relative-position scale.
- **Sequence texture:** few runs look like clumps and many like alternation, even with identical totals.

## Anti-patterns

- Ignore sampling, independence, pairing, symmetry, or sample-size conditions because a test is "nonparametric."
- Use signed-ranks for independent samples or rank-sum for matched pairs.
- Keep zeros in sign/signed-ranks counts; the primary rule discards them.
- Rank signed differences directly; rank absolute differences, average ties, then restore signs.
- Assign arbitrary tie ranks, omit the Kruskal-Wallis correction, or treat its rejection as every pair differing.
- Run a one-tailed sign test without checking direction, or treat Spearman association as causation.

## Worked Example

### Wilcoxon Signed-Ranks Test for Freshman Weights

Ten students have September and April weights. At `alpha = 0.05`, test whether median `d = September - April` is zero. Differences: `+1, +1, -4, -3, 0, -1, -5, -8, -3, -1`.

1. Set `H0: median(d) = 0`, `H1: median(d) != 0`; discard zero, leaving `n = 9`.
2. The four `|d| = 1` values receive rank `2.5`; the two `|d| = 3` values receive `5.5`; `4`, `5`, and `8` receive `7`, `8`, and `9`.
3. `W+ = 5`, `|W-| = 40`, so `T = min(5, 40) = 5`.
4. Since `n <= 30`, Table A-8 gives a two-tailed `alpha = 0.05` cutoff of `6`; reject because `5 <= 6`.

There is sufficient evidence the median difference is not zero. Seven of nine nonzero differences are negative, so April weights tend to exceed September weights. Volunteers limit generalization.

## Key Takeaways (3-7 actionable)

1. Identify the design before selecting a formula.
2. Verify sampling, independence/pairing, symmetry where required, and thresholds.
3. Discard required zeros, average ties, and correct Kruskal-Wallis ties when needed.
4. Use the correct exact/approximate branch and alternative tail.
5. Report reject/fail-to-reject, direction, and sampling limitations.

## Connects To

- **Matched-pairs t test:** sign and signed-ranks analyze paired differences without normality.
- **One-sample/proportion tests:** sign handles median or two-category claims when scale assumptions fail.
- **Two-sample t test/one-way ANOVA:** rank-sum and Kruskal-Wallis compare independent groups through ranks.
- **Pearson correlation and exploration:** Spearman targets monotone association; plots and sequence inspection guide choice; runs tests order randomness.

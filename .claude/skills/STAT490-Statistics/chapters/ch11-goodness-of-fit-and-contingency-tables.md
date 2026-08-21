# Chapter 11: Goodness-of-Fit and Contingency Tables

## Core Idea

Chi-square procedures analyze categorical data as frequency counts. Their common engine compares observed counts with counts predicted by `H_0`:

\[
\chi^2=\sum\frac{(O-E)^2}{E}.
\]

`O` is observed and `E` is expected. Squaring prevents cancellation; dividing by `E` scales each discrepancy by its expected size. A large statistic means the data are far from the null model, so tests are right-tailed.

Choose the test from the study design, not from the table's appearance:

- One categorical variable versus claimed proportions: goodness-of-fit.
- Two categorical variables measured on one population or sample: independence.
- A common categorical outcome compared across separately sampled groups: homogeneity.
- Binary outcomes recorded on matched pairs: McNemar's test.

Similar arithmetic does not make the hypotheses or units interchangeable. Dependence or unequal proportions are not automatically causal.

## Frameworks Introduced (exact named concepts, when to use, how)

### Chi-square distribution

**When to use:** Use it as the reference distribution for disagreement between observed and expected categorical counts.

**How:** Compute nonnegative `chi^2`, determine `df`, and use a right-tail critical value or P-value. Because counts are discrete but the reference distribution is continuous, adequate expected counts matter.

### Goodness-of-fit test

**When to use:** Use it for a random one-way sample when a claim specifies probabilities across `k` categories. Set `H_0` to the claimed distribution; `H_1` says at least one probability differs.

**How:** With sample size `n`, claimed probabilities `p_i`, and observed counts `O_i`, calculate

\[
E_i=np_i,\qquad
\chi^2=\sum_{i=1}^{k}\frac{(O_i-E_i)^2}{E_i},\qquad df=k-1.
\]

For equal probabilities, `E_i=n/k`. Reject only for a large right-tail value. Every expected frequency must be at least 5; observed frequencies need not. Combine sensible categories or use another method if necessary.

### Contingency table (or two-way frequency table)

**When to use:** Use it when every observation is classified by two categorical variables. Rows represent one variable, columns the other, and cells contain frequencies.

**How:** Record row totals, column totals, and the grand total. Under independence or homogeneity, calculate expected cells from the margins and apply the common engine.

### Test of independence

**When to use:** Use it when one population or sample is classified by two categorical variables and the claim concerns a relationship.

**How:** Test

\[
H_0:\text{the variables are independent},\qquad
H_1:\text{the variables are dependent}.
\]

For cell `(i,j)`,

\[
E_{ij}=\frac{(\text{row total}_i)(\text{column total}_j)}{\text{grand total}},
\]

then calculate

\[
\chi^2=\sum\frac{(O_{ij}-E_{ij})^2}{E_{ij}},\qquad df=(r-1)(c-1).
\]

It is right-tailed; every expected cell should be at least 5.

### Test of homogeneity

**When to use:** Use it when separate populations or predetermined groups are sampled and the claim is equal outcome proportions.

**How:** Arrange group-by-outcome counts in a contingency table and use the same formula, `chi^2`, `df`, right-tail rule, and expected-count condition as independence. Independence asks whether classifications within one population are related; homogeneity asks whether proportions are equal across groups.

### Fisher exact test

**When to use:** For a `2 x 2` table with one or more expected frequencies below 5, use Fisher's exact test because the chi-square approximation may be unreliable.

**How:** Obtain the exact P-value, usually with software. It avoids the ordinary approximation and does not require every expected count to be at least 5. Keep the table's original independence or homogeneity interpretation.

### Yates' correction for continuity

**When to use:** Some analysts apply it in a `2 x 2` table or when expected frequencies are below 10 to account for the discrete-to-continuous approximation.

**How:** Replace each contribution with

\[
\frac{(|O-E|-0.5)^2}{E}
\]

instead of `(O-E)^2/E`. It generally lowers `chi^2`; it does not replace design checks or Fisher's exact test when appropriate.

### McNemar's test for matched pairs

**When to use:** Use it for nominal, binary outcomes measured twice on the same subjects or matched pairs, such as before/after classifications or two treatments applied to each subject. Results within a pair are not independent.

**How:** Arrange outcomes in a `2 x 2` table and call the discordant cell counts `b` and `c`. Test whether the two discordant directions occur in equal proportions:

\[
H_0:\text{discordant frequencies }b\text{ and }c\text{ have the same proportion}.
\]

When `b+c >= 10`, use the continuity-corrected statistic

\[
\chi^2=\frac{(|b-c|-1)^2}{b+c},\qquad df=1,
\]

Use a right-tail rule. When `b+c<10`, use the exact binomial distribution. Concordant pairs are excluded because they show no directional difference.

## Key Concepts (5-10)

1. **Observed versus expected:** `O` is actual; `E` is predicted by `H_0` and may be fractional.
2. **Right-tail logic:** Chi-square values cannot be negative. Large disagreement, not a signed direction, supplies evidence against `H_0`.
3. **Degrees of freedom:** Use `k-1` for goodness-of-fit and `(r-1)(c-1)` for an `r x c` independence or homogeneity table.
4. **Null model determines expectations:** Goodness-of-fit uses `np_i`; independence and homogeneity use row total times column total divided by the grand total.
5. **Expected-count conditions:** Check expected, not observed, frequencies. The ordinary approximation requires every expected frequency to be at least 5.
6. **Design determines meaning:** Independence uses two classifications in one population; homogeneity compares groups or populations; McNemar uses paired binary outcomes.
7. **Matched pairs change the unit:** The total is the number of pairs, and only discordant counts `b` and `c` measure change.
8. **Association is not causation:** A rejection supports dependence or unequal proportions; causal language needs an appropriate experiment and justification.

## Mental Models

### The null-world table

Imagine the table that `H_0` would generate while preserving relevant totals. Expected counts describe that null world; `chi^2` measures the distance from it.

### A weighted mismatch meter

Each cell contributes `(O-E)^2/E`; the same raw difference matters more when its expected count is small.

### Margins constrain freedom

Once margins are fixed, many cells are forced by the others. Degrees of freedom count the independent choices left.

### Discordant pairs carry direction

Both conditions succeeding or failing does not distinguish treatments. Only discordant pairs can show which condition has more successes.

## Anti-patterns

- Choose a test from the sampling design, not the table's appearance; matched pairs require McNemar's test.
- Use expected, not observed, counts for the approximation check, and derive expectations from the null model rather than observed proportions.
- Use goodness-of-fit only for one variable, the correct `df` for the design, and a right-tail rule for chi-square.
- Do not ignore expected counts below 5; combine categories or use an alternative such as Fisher's exact test for a small `2 x 2` table.
- Failure to reject is not proof of fit or independence, and a small P-value alone is not causation.
- In McNemar's test, identify discordant `b` and `c`; exclude concordant pairs.

## Worked Example (study depth, reconstruct a chi-square goodness-of-fit or independence test)

### Echinacea and infection: chi-square test of independence

Among 207 rhinovirus-exposed subjects assigned to placebo, 20% extract, or 60% extract, record infection:

| Infection outcome | Placebo | 20% extract | 60% extract | Row total |
|---|---:|---:|---:|---:|
| Infected | 88 | 48 | 42 | 178 |
| Not infected | 15 | 4 | 10 | 29 |
| Column total | 103 | 52 | 52 | 207 |

At `alpha=0.05`, test `H_0`: infection and treatment group are independent, against dependence:

\[
E_{ij}=\frac{(\text{row total})(\text{column total})}{207}.
\]

Expected cells:

| Outcome | Placebo | 20% extract | 60% extract |
|---|---:|---:|---:|
| Infected | 88.570 | 44.715 | 44.715 |
| Not infected | 14.430 | 7.285 | 7.285 |

All expected counts exceed 5 (`min=7.285`), so the ordinary approximation is acceptable. Summing all six contributions gives

\[
\chi^2=\sum\frac{(O-E)^2}{E}=2.925.
\]

Here `r=2` and `c=3`, so

\[
df=(r-1)(c-1)=2.
\]

The `alpha=0.05` critical value is `5.991`. Since `2.925<5.991`, fail to reject `H_0`: this sample does not show that infection depends on treatment group. It does not prove the treatments identical.

## Key Takeaways (3-7 actionable)

1. Identify the design and null model before calculating expected counts.
2. Use `E=np_i` for a claimed one-way distribution and `E=(row total)(column total)/(grand total)` for a contingency table.
3. Verify every expected count is at least 5; for a small `2 x 2` table, consider Fisher's exact test.
4. Use `k-1` degrees of freedom for goodness-of-fit and `(r-1)(c-1)` for an `r x c` table.
5. Read chi-square tests in the right tail and inspect which cells create the disagreement.
6. Distinguish independence, homogeneity, and matched-pairs McNemar analysis by how observations were collected.
7. Report dependence or unequal proportions, not automatic causation.

## Connects To

- **Probability models:** Uniform, Poisson, Benford, genetic, and other claimed probabilities supply `p_i` for goodness-of-fit.
- **Two-proportion inference:** For a `2 x 2` independence table, the chi-square and two-proportion tests are related by `z^2=chi^2`.
- **Matched-pairs inference:** McNemar's test handles nominal binary before/after or paired-treatment outcomes; it is not a paired quantitative `t` procedure.
- **Study design and causal inference:** Random assignment can support treatment conclusions, but the chi-square calculation itself tests a categorical association pattern.
- **Data quality:** A goodness-of-fit result assesses a claimed pattern; an unusually perfect fit may warrant questions about how the data were generated.

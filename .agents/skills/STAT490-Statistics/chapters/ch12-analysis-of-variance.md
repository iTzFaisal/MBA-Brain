# Chapter 12: Analysis of Variance

## Core Idea

Analysis of variance (ANOVA) tests whether several population means can plausibly be equal by comparing:

- **Between-group variation**: how far sample means are from the grand mean.
- **Within-group variation**: how much observations scatter around their own group means.

The central ratio is `F = MS(treatment) / MS(error)`. Under the null, mean separation should be comparable to within-group scatter. If at least one mean differs, the treatment component tends to dominate. The right-tailed F test gives smaller P-values for larger F values.

For one-way ANOVA, `H_0: mu_1 = mu_2 = ... = mu_k` and `H_1: the means are not all equal`. A significant result is omnibus: at least one mean differs, but the test does not identify which one. Two-way ANOVA adds a factor and tests interaction before separate main effects.

## Frameworks Introduced (exact named concepts, when to use, how)

- **F distribution**: Use it for ANOVA variance ratios. It is nonnegative and right-skewed; its shape and critical values depend on both numerator and denominator df.

- **One-way analysis of variance (ANOVA)**: Use it for three or more independent groups defined by one factor. State hypotheses, check requirements, obtain F and its P-value, and reject equal means when `P <= alpha`.

- **ANOVA sum-of-squares decomposition**: Partition variation as `SS(total) = SS(treatment) + SS(error)`, with `SS(total) = sum_all (x_ij - x_bar)^2`, `SS(treatment) = sum_{i=1}^k n_i (x_bar_i - x_bar)^2`, and `SS(error) = sum_{i=1}^k (n_i - 1)s_i^2`. Here `x_bar` is the grand mean, `x_bar_i` the group mean, `n_i` its size, and `s_i^2` its variance.

- **Mean squares and the one-way F test**: Divide by df: `MS(treatment) = SS(treatment)/(k - 1)`, `MS(error) = SS(error)/(N - k)`, and `MS(total) = SS(total)/(N - 1)`, where `N = sum n_i`. Use `F = MS(treatment)/MS(error)` with df `k - 1` and `N - k`.

- **Bonferroni multiple comparison test**: After a significant one-way test, compare pairs using ANOVA `MS(error)` and `df = N - k`. For means i and j, `t = (x_bar_i - x_bar_j)/sqrt(MS(error)(1/n_i + 1/n_j))`. With `m = k(k - 1)/2` pairs, use `alpha/m` per test or multiply each two-tailed P-value by m.

- **Two-way analysis of variance (ANOVA)**: Use it when quantitative observations are classified by two factors in rows and columns. Test interaction first with `F = MS(interaction)/MS(error)`. Interpret row `F = MS(row)/MS(error)` and column `F = MS(column)/MS(error)` separately only when interaction is not significant.

- **Interaction graph**: Plot cell means against one factor with lines for levels of the other. Parallel lines suggest no interaction; nonparallel lines suggest changing effects. Use the formal interaction F test for the decision.

- **Completely randomized design** and **rigorously controlled design**: Random assignment gives each element the same chance of each treatment. Control other factors to reduce confounding and make differences more credible.

- **Balanced design** and **one observation per cell**: A balanced two-way design has equal cell sizes. Replication supplies within-cell variation and permits an interaction estimate. With one observation per cell, an independent interaction/error estimate is unavailable; justify no interaction before testing main effects.

## Key Concepts (5-10)

1. **Treatment or factor**: The characteristic separating one-way populations; its categories are levels or treatments.

2. **Omnibus inference**: Rejecting `H_0` says not all means are equal. Failing to reject says the evidence is insufficient, not that equality has been proved.

3. **Between versus within variation**: Treatment SS increases as group means move from the grand mean. Error SS measures scatter inside groups and is unchanged when every value in a group is shifted by one constant.

4. **Degrees of freedom**: With `k` groups and `N` observations, treatment, error, and total df are `k - 1`, `N - k`, and `N - 1`. Report the F statistic with `(k - 1, N - k)` df.

5. **Sample-size weighting**: Equal groups give `F = n s_x_bar^2/s_p^2`. Unequal groups use `n_i`-weighted treatment SS and pooled error variance; larger groups receive more weight.

6. **Requirements**: Use quantitative data from approximately normal populations with common or nearly common variances, simple random samples, independent observations, and one factor. Equal or nearly equal sizes improve robustness; consider Kruskal-Wallis for a far-from-normal population.

7. **Familywise error**: Repeated unadjusted pairwise tests inflate the chance of a false positive somewhere. The omnibus test provides one initial test; Bonferroni lowers each follow-up test's effective alpha.

8. **Interaction versus main effect**: An interaction means the effect of one factor changes at levels of the other. A main effect averages across the other factor and can mislead when interaction exists.

9. **Replication and design**: Independent observations provide an error estimate. Balanced cells simplify two-way analysis; randomization or control is needed before a mean difference can support causal language.

## Mental Models

- **Signal-to-noise gauge**: `MS(treatment)` is separation signal; `MS(error)` is background noise. F asks whether signal exceeds ordinary scatter.

- **Grand-mean accounting**: Each departure from the grand mean splits into a group-mean departure and a residual. The two SS accounts must reconcile.

- **Interaction as a gatekeeper**: If factors work differently in combination, do not summarize either as independent; otherwise examine row and column averages.

- **Replication buys a denominator**: Repeated observations reveal within-cell error. Without replication, the two-way interaction/error structure cannot be estimated.

## Anti-patterns

- Running unadjusted pairwise tests, or treating a significant omnibus F test as proof that every group differs. Use an adjusted follow-up to name differing pairs.

- Treating a large P-value as proof that all means are equal.

- Ignoring independence or applying the independent-samples procedure to matched or paired observations.

- Assuming normality and equal variances without inspecting groups, or ignoring a severe departure from those requirements.

- Running separate row and column ANOVAs, or interpreting main effects after a significant interaction.

- Inferring causation from an observational category difference when an unmeasured factor may explain it.

## Worked Example (study depth, reconstruct a one-way ANOVA table/decision)

Use crash-test chest-deceleration data for small, medium, and large cars. Each group has `n_i = 10`, so `k = 3` and `N = 30`:

| Group | `x_bar_i` | `s_i^2` |
|---|---:|---:|
| Small | 44.7 | 19.3444 |
| Medium | 42.1 | 18.9889 |
| Large | 39.0 | 21.3333 |

The grand mean is `x_bar = (447 + 421 + 390)/30 = 41.9333`. The groups are treated as approximately normal with similar variances, and the samples as random and independent.

Within-group variation is
`SS(error) = 9(19.3444) + 9(18.9889) + 9(21.3333) = 537.000`.

Between-group variation is
`SS(treatment) = 10(44.7 - 41.9333)^2 + 10(42.1 - 41.9333)^2 + 10(39.0 - 41.9333)^2 = 162.867`.

Thus `SS(total) = 699.867`, and the compact ANOVA table is:

| Source | SS | df | MS | F |
|---|---:|---:|---:|---:|
| Treatment/between | 162.867 | 2 | 81.433 | 4.094 |
| Error/within | 537.000 | 27 | 19.889 | |
| Total | 699.867 | 29 | 24.133 | |

The F distribution uses `(2, 27)` df. Technology gives `P approximately 0.028`. At `alpha = 0.05`, reject equal population means: the three means are not all equal. Do not claim that every pair differs. There are `m = 3(2)/2 = 3` pairs; a Bonferroni follow-up uses `MS(error) = 19.8889`, `df = 27`, and `alpha/3` per pair. For small versus medium, `t = 2.6/sqrt(19.8889(0.2)) = 1.304`, with unadjusted two-tailed `P approximately 0.203` and adjusted `P approximately 0.610`, so it is not significant. The corrected results identify small versus large as significant, while medium versus large is not. Report this pairwise conclusion separately from the omnibus result.

For a balanced two-way design with `r` row levels, `c` column levels, and `n` observations per cell, df are row `r - 1`, column `c - 1`, interaction `(r - 1)(c - 1)`, error `rc(n - 1)`, and total `rcn - 1`. Test interaction first; if it is significant, discuss combinations or simple effects rather than separate main effects.

## Key Takeaways (3-7 actionable)

- Use one-way ANOVA for three or more independent groups and two-way ANOVA for two factors.
- Check normality, variance, sampling, independence, outcome type, and balance before trusting F.
- Read or build the table using SS, df, MS, and F; report F df and P-value.
- Interpret a small one-way P-value only as evidence that at least one mean differs; use Bonferroni to locate differences.
- In two-way ANOVA, test interaction first and stop separate main-effect interpretation when it is significant.
- Prefer randomization, control, replication, and balanced sizes when designing the study.

## Connects To

- **Two independent means**: One-way ANOVA extends mean comparison to three or more groups without an uncorrected sequence of pairwise tests.
- **F distribution**: It supplies the right-tailed reference distribution for ANOVA ratios.
- **Kruskal-Wallis**: Consider it when a population is far from normal.
- **Confidence intervals and boxplots**: Use them to explore possible differences, not as substitutes for omnibus and corrected inference.
- **Experimental design**: Random assignment and nuisance-factor control determine whether ANOVA supports causal language; sampling determines generalizability.

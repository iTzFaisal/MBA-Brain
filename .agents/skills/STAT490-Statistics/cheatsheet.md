# Statistics Cheatsheet

## Start Here

| Question | Decision |
|---|---|
| Can the result generalize? | Check source, random/probability sampling, nonresponse, measurement, and target population. |
| Can it support causation? | Require a suitable randomized/controlled experiment; observational correlation is not causation. |
| What should I inspect first? | CVDOT: center, variation, distribution, outliers, time. |

## Display Router

| Data/question | Display |
|---|---|
| Quantitative distribution | histogram, dotplot, stemplot, boxplot |
| Categories | bar, Pareto, pie |
| Paired quantitative values | scatterplot |
| Ordered observations | time-series/run chart |

## Probability and Distribution Rules

- `P(not A) = 1 - P(A)`; `P(A or B) = P(A)+P(B)-P(A and B)`.
- `P(A and B) = P(A)P(B|A)`; independent means `P(B|A)=P(B)`.
- "At least one" -> `1 - P(none)`.
- Binomial: fixed `n`, independent binary trials, constant `p`; `P(x)=C(n,x)p^x(1-p)^(n-x)`, `mu=np`, `sigma=sqrt(npq)`.
- Poisson: independent events at stable mean rate `m` per interval; `P(x)=m^x e^(-m)/x!`, `sigma=sqrt(m)`.
- Normal: `z=(x-mu)/sigma`; sample mean uses `z=(xbar-mu)/(sigma/sqrt(n))`.
- Normal approximation to binomial: verify `np >= 5`, `nq >= 5`; use half-unit continuity correction.

## Estimation and Testing

| Target | Standard method |
|---|---|
| Proportion `p` | z interval/test; check at least 5 successes and failures |
| Mean `mu`, sigma known | z |
| Mean `mu`, sigma unknown | t, `df=n-1` |
| Variance or SD | chi-square; population normality is important |

- CI pattern: `estimate +/- critical value*SE`.
- `P <= alpha` -> reject `H0`; otherwise fail to reject. Never say accept/prove.
- `H0` has equality; `H1` chooses the tail. Statistical significance is not practical importance.
- For planning: percentage points become decimals; round sample size up; no prior proportion -> use `p=q=0.5`.

## Comparing Groups

- Two proportions: pool only for the equality-null test; do not pool the CI.
- Two means: independent -> unpooled t by default; matched -> analyze signed within-pair differences.
- Three or more means: one-way ANOVA, `F=MS(treatment)/MS(error)`; significant F means at least one differs, then use adjusted pairwise tests.
- Two-way ANOVA: test interaction before separate main effects.
- Nonparametric: sign (direction), signed-ranks (paired), rank-sum (two independent), Kruskal-Wallis (3+), Spearman (monotone association), runs (order randomness).

## Categorical Counts and Regression

- Goodness-of-fit: `E=np_i`, `df=k-1`.
- Independence/homogeneity: `E=(row total)(column total)/(grand total)`, `df=(r-1)(c-1)`; all expected counts should be at least 5.
- Regression: plot first; `yhat=b0+b1x`; residual `e=y-yhat`; `r` is linear association, `r^2` is explained sample variation; avoid extrapolation and causal claims.

## SPC Tells

- R chart = subgroup spread; x-bar chart = subgroup center; p chart = binary defect proportion.
- Instability: obvious nonrandom pattern, point beyond UCL/LCL, or 8 consecutive points on one side of centerline.
- Control limits describe process behavior, not specifications. Investigate signals; do not tamper with routine noise.

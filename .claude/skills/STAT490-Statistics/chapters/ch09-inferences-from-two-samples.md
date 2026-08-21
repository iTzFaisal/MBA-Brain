# Chapter 9: Inferences from Two Samples

## Core Idea

Two-sample inference compares proportions, means, paired measurements, or variances. Start with the design: unrelated observations are independent; repeated measurements or defensible matches are paired. Then choose the z, t, or F procedure whose standard error and assumptions fit the contrast.

## Frameworks Introduced

- **Two Proportions (Independent Samples)**
  - **Use when:** The response is binary and two independent simple random samples estimate `p_1` and `p_2`.
  - **Check:** Samples are independent, and each has at least 5 successes and 5 failures: `x_i >= 5` and `n_i - x_i >= 5`.
  - **Test `H_0: p_1 = p_2`:** Let `\hat p_i=x_i/n_i`, then pool because the equality null asserts one common proportion:
    
    `\hat p=(x_1+x_2)/(n_1+n_2)`, `\hat q=1-\hat p`.
    
    Use `z=[(\hat p_1-\hat p_2)-(p_1-p_2)]/sqrt[\hat p\hat q(1/n_1+1/n_2)]`, with `p_1-p_2=0` under the null.
  - **Estimate with a confidence interval:** Do not pool. Use
    
    `(\hat p_1-\hat p_2) +/- z_(alpha/2) sqrt[\hat p_1\hat q_1/n_1+\hat p_2\hat q_2/n_2]`.
    
    This estimates `p_1-p_2` using separate sample proportions. The test and interval therefore use different standard errors; do not decide equality by checking overlap of two separate proportion intervals.

- **Two Independent Means, Unknown and Not Assumed Equal**
  - **Use when:** Two unrelated groups provide quantitative observations and the target is `mu_1-mu_2`. This unpooled method is the default.
  - **Check:** Samples are independent simple random samples; `sigma_1` and `sigma_2` are unknown; and either both `n_i >= 30` or both populations are approximately normal. For small samples, inspect outliers and severe nonnormality.
  - **Calculate:**
    
    `t=[(xbar_1-xbar_2)-(mu_1-mu_2)]/sqrt(s_1^2/n_1+s_2^2/n_2)`.
    
    For the conservative hand calculation use `df=min(n_1-1,n_2-1)`. Software often uses Welch's value, `df=(A+B)^2/[A^2/(n_1-1)+B^2/(n_2-1)]`, where `A=s_1^2/n_1` and `B=s_2^2/n_2`. The interval is `(xbar_1-xbar_2) +/- t_(alpha/2,df) sqrt(s_1^2/n_1+s_2^2/n_2)`.

- **Two Independent Means with Known `sigma_1` and `sigma_2`**
  - **Use rarely:** Both population standard deviations must genuinely be known, samples must be independent simple random samples, and both sample sizes must be large or both populations normal.
  - **Calculate:** Replace the t standard error with the known-parameter z procedure:
    
    `z=[(xbar_1-xbar_2)-(mu_1-mu_2)]/sqrt(sigma_1^2/n_1+sigma_2^2/n_2)`;
    the interval is `(xbar_1-xbar_2) +/- z_(alpha/2) sqrt(sigma_1^2/n_1+sigma_2^2/n_2)`.

- **Two Independent Means Assuming `sigma_1=sigma_2` (Pooled t)**
  - **Use when:** Independent simple random samples have unknown standard deviations and a common population variance is substantively justified or explicitly required. Apply the same size/normality checks as above.
  - **Calculate:**
    
    `s_p^2=[(n_1-1)s_1^2+(n_2-1)s_2^2]/(n_1+n_2-2)`;
    
    `t=[(xbar_1-xbar_2)-(mu_1-mu_2)]/[s_p sqrt(1/n_1+1/n_2)]`, with `df=n_1+n_2-2`.
    
    The interval is `(xbar_1-xbar_2) +/- t_(alpha/2,df)s_p sqrt(1/n_1+1/n_2)`. Pooling can improve power when equality is credible. Do not use a preliminary F test to choose; unless instructed otherwise, use the unpooled method.

- **Dependent Samples (Matched-Pairs t)**
  - **Use when:** Every observation has a meaningful counterpart: the same subject measured twice or a genuinely matched subject/pair. Equal sample sizes or adjacent spreadsheet columns do not establish pairing.
  - **Calculate:** Choose an order and define `d_i` (for example, `d_i=April_i-September_i`). Treat the `n` differences as one sample:
    
    `t=(dbar-mu_d)/(s_d/sqrt(n))`, with `df=n-1`, and interval `dbar +/- t_(alpha/2,n-1)s_d/sqrt(n)`.
    
    The pairs should be randomly sampled or assigned, and the differences should be approximately normal or have `n >= 30`; with small `n`, inspect differences for outliers and strong nonnormality. Pairs may be dependent within pair, but pairs should be independent. The sign depends on the chosen order.

- **F Test for Two Variances (or Standard Deviations)**
  - **Use when:** The target is variation, not means. Require independent simple random samples from two normally distributed populations. The F test is highly sensitive to nonnormality and outliers, so it is not robust.
  - **Calculate:** Put the larger sample variance in the numerator: `F=s_1^2/s_2^2`, with degrees of freedom `n_1-1` and `n_2-1`. Test `H_0:sigma_1^2=sigma_2^2`; large values oppose equality and an `F` near 1 is only compatible with equality, not proof. With the larger variance on top, a one-tailed alternative is right-tailed; for a two-tailed `alpha=.05` test, use upper-tail area `.025`.
  - **Interval:** If `F_R` and `F_L` are the upper and lower critical values, use `(s_1^2/s_2^2)/F_R <= sigma_1^2/sigma_2^2 <= (s_1^2/s_2^2)/F_L`; take square roots for `sigma_1/sigma_2`. Equality corresponds to inclusion of 1. When normality is doubtful, consider Count Five or the more robust Levene-Brown-Forsythe procedure, which applies a two-sample t test to deviations from each sample median.

## Key Concepts

- **Contrast:** Infer one target, such as `p_1-p_2`, `mu_1-mu_2`, `mu_d`, or `sigma_1^2/sigma_2^2`, rather than comparing two isolated estimates.
- **Design:** Independent groups require a two-sample standard error; paired data require the standard deviation of within-pair differences.
- **Pooling:** Pool proportions only for the equality-null test. Use separate proportions for its confidence interval. Pool mean variances only under a common-variance model.
- **Degrees of freedom:** They select the t or F reference distribution. Unpooled hand calculations use `min(n_1-1,n_2-1)`; pooled means use `n_1+n_2-2`.
- **Robustness:** Independent-mean and matched-pairs t procedures tolerate moderate nonnormality under their checks; the F procedure does not tolerate it well.
- **Evidence:** Rejecting a null supports a claim at the chosen error rate. Non-rejection is insufficient evidence, not proof of equality; report effect size and practical meaning.

## Mental Models

- **Design determines the denominator.** Ask what relationship generated the observations before doing arithmetic. Pairing can remove subject-to-subject variation; treating paired data as independent loses that control.
- **Reduce to one ordered contrast.** Write the group order or difference order explicitly. Reversing it reverses the sign but not the underlying evidence.
- **Pool only when the model says to pool.** The two-proportion equality null supplies one common proportion; estimation of the difference does not. Matching sample sizes alone never justifies pooling mean variances.
- **Treat assumptions as a gate.** Check sampling, independence, counts, size/normality, and outliers first. Large samples help means but do not make an F test safe against severe nonnormality.

## Anti-patterns

- **Pairing by convenience:** Same sample size, adjacent columns, or a shared label is not a defensible match.
- **Using separate-interval overlap to test two proportions:** Directly test `p_1-p_2` or construct its interval instead.
- **Pooling independent means automatically:** Use unpooled t unless a common variance is justified or required; do not use a preliminary F test as the decision rule.
- **Applying F to nonnormal or outlier-prone data:** Inspect graphs and use a robust alternative when needed.
- **Confusing statistical and practical significance:** A small P-value says little about usefulness; give the contrast and interval in context.
- **Ignoring sampling limits:** No formula repairs volunteer bias, convenience sampling, weak matching, or a sampled population that does not support the stated claim.

## Worked Example

### Airbag Fatality Rates: Two-Proportion Inference

Among front-seat occupants in crashes, 41 of `n_1=11,541` occupants with airbags died, compared with 52 of `n_2=9,853` without airbags. Let group 1 be airbags and test whether `p_1<p_2` at `alpha=.05`.

1. **Check and state:** Treat the groups as independent simple random samples. Each group has at least 5 fatalities and 5 survivors, so the normal approximation condition holds. Use `H_0:p_1=p_2` versus `H_1:p_1<p_2`.
2. **Pool for the test:** `\hat p_1=41/11,541=.003553`, `\hat p_2=52/9,853=.005278`, and `\hat p=(41+52)/(11,541+9,853)=.004347`, so `\hat q=.995653`. Substitution in the pooled statistic gives `z=-1.91`, with left-tail `P=.0281`.
3. **Interpret:** Reject `H_0`; the data provide evidence of a lower fatality proportion for the airbag group. This is not automatically a universal causal claim.
4. **Estimate:** A 90% interval uses separate, unpooled proportions: `-0.00323 <= p_1-p_2 <= -0.000218`. It estimates a lower airbag fatality rate by about `0.0218` to `0.323` percentage points. The contrast between pooled testing and unpooled estimation is intentional.

## Key Takeaways

1. Identify the estimand and design before selecting z, t, or F.
2. Check random sampling/independence, success-failure counts, size or normality, and outliers.
3. Pool two proportions only for the equality-null test; keep the interval unpooled.
4. Use unpooled t by default for independent means with unknown unequal variances; pool only with a defensible common-variance assumption.
5. Convert matched observations to signed differences and use a one-sample t procedure.
6. Use F for variances only with plausible normal populations; otherwise consider robust alternatives.
7. Report direction, uncertainty, P-value or decision, sampling limitations, and practical meaning.

## Connects To

- **Chapters 7 and 8:** The same interval and test logic now targets a difference or ratio of two population parameters.
- **Sampling distributions:** Normal, t, and F distributions describe reference behavior; the standard error describes contrast variability across samples.
- **Experimental design:** Random assignment supports fair comparisons, while matching can remove subject or plot variation. Design precedes calculation.
- **Decision-making:** Confidence intervals connect evidence to effect size, uncertainty, and practical importance.

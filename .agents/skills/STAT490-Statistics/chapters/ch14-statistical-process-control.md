# Chapter 14: Statistical Process Control

## Core Idea

Statistical process control (SPC) monitors a characteristic repeatedly over time so process changes can be detected before quality deteriorates. It applies to manufacturing, services, environmental measures, and other repeated operations.

Keep a **process** distinct from a static **population**:

- **Process data** are observations in time order; their mean, spread, or distribution may change.
- Only a **statistically stable** (or **within statistical control**) process can be treated as if its observations came from a population with constant characteristics.
- SPC evaluates the process trajectory, not just whether individual products meet a target.

A stable process has natural variation: random fluctuation without detectable trends, cycles, shifts, or unusual points. A signal suggests assignable variation, a cause that may be found and corrected. Separate routine noise from evidence of change; do not react to every fluctuation.

Every control chart has a **centerline (CL)**, **upper control limit (UCL)**, and **lower control limit (LCL)**. These estimate process behavior and are roughly equivalent to 99.7% confidence limits under the chapter's assumptions. They are not specifications, tolerances, or targets: a stable process can miss specifications, and an unstable one can temporarily satisfy them.

## Frameworks Introduced (exact named concepts, when to use, how)

### Statistical Process Control

**When to use:** Use SPC when a characteristic is measured repeatedly in a meaningful time sequence and the aim is to maintain or improve the process.

**How:** Define the characteristic and sampling interval, preserve order, form comparable subgroups when appropriate, plot the suitable chart, and investigate signals. Never replace a control limit with a specification.

### Process Data

**When to use:** Treat observations as process data when each value comes from an ongoing operation and collection order matters.

**How:** Record time and context; check for changes before applying methods that assume one fixed population.

### Run Chart

**When to use:** Use a **Run Chart** for individual observations when you need a quick time-ordered check, especially before choosing or interpreting subgroup charts.

**How:** Plot each value against time or sample number. Look for trends, shifts, outliers, cycles, or widening or narrowing variation. It is a visual scan; formal limits here apply to R, x, and p charts.

### Control Chart for R (R Chart, or Range Chart)

**When to use:** Use an **R Chart** for within-subgroup variation when observations arrive in equal-sized subgroups and `n <= 10`. For `n > 10`, use an s chart based on subgroup standard deviations.

**Requirements:** Use equal-sized subgroups, an essentially normal process-data distribution, and independent individual values.

For subgroup `i`, calculate

\[
R_i=\max(x_{i1},\ldots,x_{in})-\min(x_{i1},\ldots,x_{in}),
\qquad
\bar R=\frac{R_1+\cdots+R_k}{k}.
\]

Using the table constants for `n`, plot the ranges in time order:

\[
\text{CL}_R=\bar R,\qquad
\text{UCL}_R=D_4\bar R,\qquad
\text{LCL}_R=D_3\bar R.
\]

The R chart tests spread, not the process mean.

### Control Chart for x (x Chart, commonly called an x-bar Chart)

**When to use:** Use an **x Chart** to monitor the process center with equal-sized, approximately normal, independent subgroups. Read it with an R chart because either spread or mean can become unstable.

For subgroup means \(\bar x_i\), calculate

\[
\bar{\bar x}=\frac{\bar x_1+\cdots+\bar x_k}{k}.
\]

For equal subgroup sizes, this is also the mean of all individual observations. With the table constant `A2`, use

\[
\text{CL}_x=\bar{\bar x},\qquad
\text{UCL}_x=\bar{\bar x}+A_2\bar R,\qquad
\text{LCL}_x=\bar{\bar x}-A_2\bar R.
\]

### Control Chart for p (p Chart)

**When to use:** Use a **p Chart** for a binary attribute, such as defective/nondefective or conforming/nonconforming, with equal-sized samples in this treatment.

**Requirements:** Samples are time ordered and have common size `n`; items are binary and independent.

For sample `i`, plot \(\hat p_i=d_i/n\), where `d_i` is the number with the attribute. Pool all samples:

\[
p=\frac{\text{total attribute items}}{\text{total items sampled}},
\qquad q=1-p.
\]

Then calculate

\[
\text{CL}_p=p,\qquad
\text{UCL}_p=p+3\sqrt{\frac{pq}{n}},\qquad
\text{LCL}_p=p-3\sqrt{\frac{pq}{n}}.
\]

Set UCL to 1 if it exceeds 1 and LCL to 0 if it is negative. The p chart detects a change in defect proportion; it does not show that the rate meets a customer or engineering specification.

### Criteria for Determining When a Process Is Not Statistically Stable (Out of Statistical Control)

Apply these criteria to the run or control-chart sequence:

1. **Obvious nonrandom pattern, trend, or cycle:** The sequence behaves systematically rather than like chance fluctuation.
2. **Point outside the control limits:** A point is above UCL or below LCL.
3. **Run of 8 Rule:** Eight consecutive points all lie above the centerline or all lie below it.

## Key Concepts (5-10)

1. **Stability is temporal.** A snapshot can look acceptable while the process drifts, shifts, cycles, or becomes more variable.
2. **Natural variation is not no variation.** Stability means differences show no detectable nonrandom cause.
3. **R and x answer different questions.** R asks whether subgroup spread is stable; x asks whether the center is stable.
4. **Limits are process estimates.** CL, UCL, and LCL summarize current behavior; they are not targets or specifications.
5. **A p chart is for binary attributes.** It pools observations for `p` and, here, requires equal sample sizes.
6. **A signal is evidence, not a diagnosis.** Investigate timing and conditions before naming a cause; stable behavior still requires a separate capability comparison.

## Mental Models

- **Process versus population:** A population snapshot is a distribution; a process is a movie. Preserve time order because the movie can change.
- **R asks “how wide?” and x asks “where centered?”** Interpret spread and location together.
- **Control limits are a process fingerprint:** They describe what the current process normally produces, not what management wishes it produced.
- **Signal means investigate, not tamper:** Adjust only when evidence supports an assignable cause; otherwise an adjustment can create a shift or extra variation.

## Anti-patterns

- Treating UCL/LCL as product specifications, or assuming every point inside them is acceptable to a customer.
- Ignoring chronological order and analyzing changing process data as one fixed population.
- Declaring stability because no point crosses a limit while overlooking a trend, cycle, shift, widening spread, or run of eight.
- Reading only the x chart or only the R chart; stable spread does not prove a stable mean, and vice versa.
- Using an R chart for subgroups larger than 10, or using a p chart for a continuous measure or a nonbinary attribute.
- **Tampering:** adjusting equipment after every unusual-looking observation. Wait for a signal, investigate the assignable cause, and change deliberately. Preserve a verified beneficial downward defect trend rather than automatically undoing it.
- Concluding that a stable chart proves products meet specifications.

## Worked Example

### Earth temperatures: R and x-bar charts

Thirteen chronological decades each contain `n = 10` annual Earth mean temperatures. Their subgroup means, in order, are `13.819, 13.692, 13.741, 13.788, 13.906, 14.016, 14.052, 13.983, 13.938, 14.014, 14.264, 14.396, 14.636`; the corresponding ranges are `0.49, 0.41, 0.37, 0.52, 0.26, 0.26, 0.23, 0.30, 0.45, 0.39, 0.32, 0.55, 0.36`.

The mean range is \(\bar R=0.3777\). For `n = 10`, `D3 = 0.223` and `D4 = 1.777`, so

\[
\text{CL}_R=0.3777,\qquad
\text{UCL}_R=(1.777)(0.3777)=0.6712,\qquad
\text{LCL}_R=(0.223)(0.3777)=0.0842.
\]

All ranges fall within these limits, with no obvious range pattern or run of eight on one side of the centerline. Within-decade variation is stable.

The mean of the subgroup means is \(\bar{\bar x}=14.019\). With `A2 = 0.308`,

\[
\text{CL}_x=14.019,\qquad
\text{UCL}_x=14.019+(0.308)(0.3777)=14.135,\qquad
\text{LCL}_x=14.019-(0.308)(0.3777)=13.903.
\]

Early means are below LCL, and the 1980s, 1990s, and 2000s means are above UCL. The sequence also trends upward. Thus the R chart shows stable spread, but the x-bar chart shows an unstable process center under criteria 1 and 2. Investigate what changed and when; do not tamper with individual temperatures. Whether the temperatures meet a scientific or policy specification is a separate question.

## Key Takeaways (3-7 actionable)

1. Define the characteristic, sampling interval, subgroup size, and time order before calculating.
2. Start with a run chart to see trends, shifts, cycles, outliers, and changing spread.
3. For equal normal subgroups, use R for variation and x-bar for the mean; interpret them together.
4. For equal-size binary samples, use pooled `p`, `q = 1 - p`, and limits \(p\pm3\sqrt{pq/n}\), truncated to [0, 1].
5. Declare instability for a nonrandom pattern, a point beyond a limit, or a Run of 8; investigate rather than reflexively adjust.
6. After stability, compare the predictable process with specifications; do not confuse the two analyses.

## Connects To

- **Descriptive statistics and visualization:** Run charts make time order central to ordinary plots.
- **Sampling and probability:** R and x limits use subgroup behavior and chart constants; p limits use proportion sampling variation and a 3-standard-error approximation.
- **Normal models and independence:** R/x procedures assume an essentially normal process and independent individual values; p procedures assume independent binary outcomes.
- **Capability and improvement:** Once stability is established, compare level and spread with specifications, then investigate assignable causes and standardize verified improvements.

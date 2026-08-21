# Chapter 10: Quality Control

## Core Idea
Quality control measures process output against a standard and corrects unacceptable performance. Every process has **random (chance/common) variation** from many small influences; **assignable (special/nonrandom) variation** has an identifiable cause such as tool wear, equipment adjustment, bad material, operator conditions, or measurement problems. The manager's sequence is: stabilize the process by detecting nonrandom variation, then test whether its remaining natural variation can meet specifications. A process can be statistically in control and still be incapable of satisfying customer requirements.

Quality assurance is most progressive when quality is designed into the product and process, reducing dependence on inspection. Inspection remains an appraisal activity; statistical process control (SPC) monitors production while it is occurring; continuous improvement seeks to reduce variation at its source.

## Frameworks Introduced

- **Inspection decision framework:** Inspect before production (inputs), during production (conversion), and after production (final conformance). Decide how much and how often by weighing inspection cost, delay, destructive testing, process reliability, human involvement, and the cost of passing defects. Candidate points include raw materials, before costly or irreversible steps, before covering/assembly operations, and finished output. On-site inspection gives speed and avoids transport effects; a laboratory gives specialized equipment and a controlled environment. Acceptance sampling checks lots before or after production; process control monitors the process during production.
- **SPC control cycle:** Define the characteristic; measure it; compare it with a standard; evaluate whether departures are random; correct assignable causes; and monitor long enough to verify the correction. Preserve time order because a control chart is a time-ordered plot of sample statistics.
- **Control-chart logic:** Choose limits from the sampling distribution. A point on or beyond a limit signals possible nonrandom variation, but it is evidence to investigate, not a diagnosis. A point inside both limits does not prove randomness; supplement charts with run tests and a visual plot.
- **Chart-selection rule:** Use variable charts for measured continuous data: an x-bar chart for center and an R chart for dispersion. Use attribute charts for counted data: a p-chart for the fraction defective when both good and bad units can be counted, and a c-chart for defects/occurrences per unit when non-occurrences cannot be counted.
- **Stability-to-capability sequence:** Establish statistical control first; then compare natural process width with specifications using Cp or Cpk. Improve the process rather than relying on inspection to screen out predictable defects.

## Key Concepts

- **Limits are not specifications.** Control limits describe expected variation in sample statistics; specifications are engineering/customer acceptance boundaries; process variability is the natural standard deviation of individual output. Use z = 2 for about 95.44% coverage (Type I risk about 4.56%) or z = 3 for about 99.74% (about 0.26%). Narrower limits reduce Type I error (false out-of-control signal) but increase Type II error (missing a real shift).
- For x-bar charts, with known process standard deviation sigma and subgroup size n:
  `UCL = x-double-bar + z(sigma/sqrt(n))`, `LCL = x-double-bar - z(sigma/sqrt(n))`.
  When sigma is unknown, estimate spread with the average subgroup range:
  `UCL = x-double-bar + A2(R-bar)`, `LCL = x-double-bar - A2(R-bar)`.
- For R charts:
  `CL = R-bar`, `UCL = D4(R-bar)`, `LCL = D3(R-bar)`.
  The table constants depend on n. Use x-bar and R together when both center and dispersion matter: a mean shift may leave R unchanged, while increasing dispersion may first appear on R.
- For a p-chart, `p_i = d_i/n`, `p-bar = total defectives / total observations`, and `sigma_p = sqrt[p-bar(1-p-bar)/n]`:
  `UCL = p-bar + z(sigma_p)`, `LCL = p-bar - z(sigma_p)`.
  Replace a negative LCL with zero. The binomial model (often normal-approximated) supports the chart.
- For a c-chart, `c-bar = total defects / number of samples` and `sigma_c = sqrt(c-bar)`:
  `UCL = c-bar + z(sqrt(c-bar))`, `LCL = c-bar - z(sqrt(c-bar))`.
  It uses a Poisson model for occurrences over a continuous unit where more than one defect at one point is negligible; set a negative LCL to zero.
- **Run tests:** Code observations above/below the median as A/B and successive increases/decreases as U/D. Expected runs and standard deviations are `E(r)_med = N/2 + 1`, `sigma_med = sqrt((N-1)/4)`, `E(r)_u/d = (2N-1)/3`, and `sigma_u/d = sqrt((16N-29)/90)`. Compute `z = (observed runs - expected runs)/sigma`; too few or too many runs (commonly beyond +/-2) indicate nonrandomness. Use both tests because they detect different patterns.
- **Capability:** For a stable, approximately normal process, process width is `6 sigma`. `Cp = (USL - LSL)/(6 sigma)` assumes the process is centered; `Cpk = min[(USL - mean)/(3 sigma), (mean - LSL)/(3 sigma)]` accounts for centering. A common capability threshold is 1.33. Cp is misleading for an off-center process; capability indexes are meaningless for an unstable or markedly nonnormal process.
- Improve capability by simplifying, standardizing, mistake-proofing, upgrading equipment, or automating. Taguchi's loss view adds that deviation from target creates increasing loss even while output remains within specifications.

## Mental Models

- **Quality is a process property:** inspection finds symptoms; prevention and variation reduction change the system.
- **Control charts are the voice of the process:** limits describe what the process normally produces, not what the customer wants.
- **R asks "how wide?" and x-bar asks "where centered?"** Read both before changing a process.
- **Stability precedes capability:** first remove special causes, then judge the predictable process against specifications.

## Anti-patterns

- Treating 100% manual inspection as perfect; fatigue, boredom, measurement error, cost, delay, and destructive tests still matter.
- Confusing control limits with specifications, or declaring a capable process merely because it is in control.
- Choosing a p-chart for continuous measurements or a c-chart when good and bad units are countable.
- Reacting to every fluctuation, ignoring time order, or overlooking trends, cycles, bias, or unusual run counts because every point is inside the limits.
- Computing Cp/Cpk before stability, using Cp for a clearly off-center process, or assuming normality without support.

## Worked Example

**Billing statements (p-chart):** Twenty samples of 100 statements contain 220 defectives. Thus `p-bar = 220/2,000 = .11` and `sigma_p = sqrt[.11(.89)/100] = .0313`. With three-sigma limits, `UCL = .11 + 3(.0313) = .2039` and `LCL = .11 - 3(.0313) = .0161`. A sample fraction above .2039 signals investigation; correct the cause, then collect new data for revised limits. A low point also merits investigation because unusually good results may reveal a resource or process change worth preserving.

**Measured times (x-bar/R):** Five subgroups of four glue-drying times have `x-double-bar = 12.11` minutes and known `sigma = .02`. With z = 3, the x-bar limits are `12.11 +/- 3(.02/sqrt(4))`, or 12.14 and 12.08. If sigma is estimated from `R-bar = .046`, `A2 = .73` gives the same limits; `D4 = 2.28` and `D3 = 0` give R limits of .105 and 0. Individual observations are not judged against x-bar limits because the chart plots subgroup means.

**Capability:** If a process has mean 9.20 grams, sigma .30 gram, LSL 7.50, and USL 10.50, the lower-side index is `(9.20-7.50)/(3*.30) = 1.89`; the upper-side index is `(10.50-9.20)/(3*.30) = 1.44`. Therefore `Cpk = 1.44`, which exceeds 1.33. The process is capable, but the smaller upper-side margin shows why centering matters. By contrast, a centered process with specification width .80 and sigma .13 has `Cp = .80/(6*.13) = 1.03`, below the usual threshold.

## Key Takeaways

1. Inspect where failure becomes costly, but build quality into design and the process whenever possible.
2. Use SPC to separate chance variation from assignable causes; define, measure, compare, correct, and verify.
3. Match the chart to the data: x-bar/R for measured center/spread, p for defective proportions, and c for defect counts.
4. Investigate limit violations, run-test signals, and patterns without reflexive tampering.
5. Assess capability only after stability; use Cp for centered processes and Cpk when centering is not assured.
6. Reduce variation through process improvement because lower variation cuts inspection, warranty, complaints, and productivity costs.

## Connects To

- **Quality management and continuous improvement:** SPC turns measurement into corrective learning and supports quality at the source.
- **Probability and sampling:** sampling distributions, the central limit theorem, binomial/Poisson models, and standard-error limits explain chart signals.
- **Operations strategy:** capability improvement moves an organization from inspection dependence toward quality designed into products and processes.
- **Process design and cost analysis:** inspection location, frequency, automation, destructive testing, and the cost of passed defects determine the economically sensible control system.

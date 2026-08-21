# Appendix B: Reference Tables

## Core Idea

Appendix B is a lookup aid for probability calculations, not a substitute for identifying the correct model. It contains four reference resources:

- **Table A:** area under the normal curve from 0 to `z`.
- **Table B.1:** standardized-normal area from negative infinity to a negative `z`.
- **Table B.2:** standardized-normal area from negative infinity to a positive `z`.
- **Table C:** cumulative Poisson probabilities, `P(X <= c)`.

The normal tables describe continuous areas. The Poisson table describes accumulated probability for a discrete count. Do not treat either table as a list of raw observations or as an exact-probability table by default.

## Reference Rules

1. **Standardize first.** For a normal variable, calculate `z = (x - mu) / sigma`. Use the row for the integer and first decimal place, then the column for the hundredths place. In B.1 the hundredths headings are printed in descending order (`.09` through `.00`), so preserve the negative sign when combining row and column.
2. **Choose by the required area.** Use Table A when the desired region is between the mean and `z`; use B.1 for a negative left-tail cutoff; use B.2 for a positive left-tail cutoff.
3. **Convert Table A values.** For positive `z`, `P(Z <= z) = 0.5 + A(0,z)` and `P(Z >= z) = 0.5 - A(0,z)`. For a negative cutoff, use `|z|`: `P(Z <= -|z|) = 0.5 - A(0,|z|)`.
4. **Use complements and differences.** `P(Z > z) = 1 - F(z)` and `P(a < Z < b) = F(b) - F(a)`. Symmetry gives `F(-z) = 1 - F(z)`.
5. **Read Poisson by parameters.** Select the row for the mean count `lambda` and the column for the cutoff `c`. The entry is `P(X <= c)`, including every count from zero through `c`.
6. **Convert cumulative Poisson values.** `P(X = c) = F(c) - F(c-1)`; `P(X >= c) = 1 - F(c-1)`; and interval probabilities are CDF differences. Match `lambda` to the same time, space, or exposure interval as the count.

## Key Concepts

- A standard normal distribution is centered at zero, has unit standard deviation, and has 0.5 area on each side of zero.
- A `z` value is a distance in standard-deviation units; its sign indicates which side of the mean contains the observation.
- A normal-table entry is an area/probability, not a `z` value.
- A Poisson variable counts events in a fixed interval. `lambda` is the expected count for that interval, and the table's `c` is a count cutoff.
- Table C implements `P(X <= c) = sum from x=0 to c of (lambda^x * e^(-lambda) / x!)`; it accumulates exact Poisson probabilities.
- Because Poisson outcomes are discrete, strict and inclusive inequalities must be translated carefully.

## Mental Models

- **Normal lookup:** start with the half-curve (`0.5`), then add or subtract the mean-to-cutoff area.
- **Standard-normal lookup:** the table is a coordinate converter: observation -> `z` -> area.
- **Poisson lookup:** read the table as a cumulative staircase. Moving one column right adds the probability of exactly one more event.
- **Operations decision:** first define the event (`at most`, `at least`, `between`, or `outside`), then select the table and perform the required complement or difference.

## Anti-patterns

- Reading Table A as though it already gives a left-tail probability.
- Dropping the sign of a negative `z` without applying symmetry.
- Using `P(X <= c)` as `P(X = c)` in Poisson work.
- Using a Poisson mean from one interval with a count measured over another interval.
- Subtracting rounded values prematurely or reporting a probability without stating the event inequality.

## Worked Example

Suppose process output is normal with `mu = 100` and `sigma = 10`. For `P(X <= 120)`, standardize: `z = 2.00`. Table A gives `A(0,2.00) = 0.4772`; add `0.5` to obtain `0.9772`, so the upper tail is `0.0228`. For a Poisson count with `lambda = 3.0`, Table C gives `F(2) = 0.423` and `F(1) = 0.199`. Therefore `P(X = 2) = 0.224`, while `P(X >= 3) = 1 - 0.423 = 0.577`.

## Key Takeaways

- Identify the distribution before opening a table.
- Separate the `z` calculation from the area conversion.
- Treat B.1 and B.2 as cumulative left-tail tables, while Table A is mean-to-cutoff.
- Treat Table C as cumulative through the selected count.
- State whether the result is a left tail, right tail, interval, exact count, or cumulative count.

## Connects To

The bounded Appendix B excerpt names the tables but does not provide chapter numbers. Use the normal tables in MGT530 chapters on demand/forecast variability, inventory safety stock and service levels, statistical quality control, and project-management probability estimates such as PERT. Use the cumulative Poisson table in chapters on waiting lines and arrival counts, acceptance sampling and defect counts, reliability/failure occurrences, and other discrete-event applications. The chapter topic determines the model; Appendix B supplies the final probability lookup.

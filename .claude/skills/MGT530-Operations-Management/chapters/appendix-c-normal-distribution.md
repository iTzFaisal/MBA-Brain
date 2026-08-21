# Appendix C: Working with the Normal Distribution

## Core Idea

The normal distribution is a theoretical model that approximates many real-life phenomena and is widely used in operations management. Its curve is symmetric and bell-shaped around the mean. Although it extends from negative to positive infinity, most observations lie near the mean; about 99.74% lie within three standard deviations.

## Frameworks/Reference Rules

- **Standardize before using a table.** Convert an observed value to a z value (z score), the number of standard deviations it is from the mean:

  `z = (x - mu) / sigma`

  Here, `x` is the specified value, `mu` is the distribution mean, and `sigma` is the distribution standard deviation. A negative z is below the mean; a positive z is above it.

- **Interpret area as probability.** The entire area under the curve is `1.0000` (100%). The area to either side of the mean is `0.5000`. For a continuous normal variable, the probability of one exact value is zero, so `P(X <= x)` and `P(X < x)` are equivalent.

- **Select the table by the question.**
  1. Use **Appendix B Table A** when the question concerns a symmetric range, such as “within +/- z” or “outside +/- z.” This table gives the area from the mean (`z = 0`) to a positive z.
  2. Use **Appendix B Tables B1/B2** for a one-sided probability, such as “no more than,” “to the left of,” or “to the right of” a z value. These tables give cumulative area from negative infinity to z. Use the negative-z portion for negative values. Read z by taking the integer and first decimal from the row and the second decimal from the column.

- **Use symmetry and complements.** The two tails at equal distances from the mean have equal area. Thus, area within `+/- z` is twice the Table A area from `0` to `+z`. Area outside `+/- z` is either twice one tail, `2(0.5000 - area from 0 to +z)`, or the complement `1.0000 - area within`. For a one-sided result from Table B, the area to the opposite side is `1.0000 -` the tabulated cumulative area.

## Key Concepts

- **Normal curve:** A symmetric, bell-shaped probability distribution centered at its mean.
- **Standard normal distribution:** The normal distribution expressed in standard-deviation units using z values.
- **z value (z score):** The signed distance of `x` from the mean measured in standard deviations.
- **Mean (`mu`):** The center of the distribution and its point of symmetry.
- **Standard deviation (`sigma`):** The scale that determines how far values typically spread from the mean.
- **Cumulative area:** Probability from negative infinity up to a specified z.
- **Tail area:** Probability beyond a specified cutoff on the left or right.

## Mental Models

- **Think in standardized coordinates.** First locate `x` relative to `mu`; then express that location in units of `sigma`. The resulting z lets one probability table serve every normal distribution.
- **Treat the curve as a probability ledger.** Start with total area `1.0000`, allocate the known central or cumulative area, and use subtraction for what remains.
- **Let wording choose the lookup.** “Within” or “outside” signals a symmetric calculation; “no more than,” “less than,” or “more than” signals a one-sided cumulative calculation.
- **Mirror before calculating twice.** Equal distances on opposite sides of the mean have equal areas, so symmetry reduces work and catches sign errors.

## Anti-patterns

- **Using Table A for a one-sided question:** It reports only mean-to-z area, not cumulative area; convert it or use Table B instead.
- **Using Table B for a within-`+/- z` question without adjustment:** Its cumulative value is not the central area; use symmetry or complements.
- **Treating z as a probability:** z is a location in standard deviations. The table supplies the probability.
- **Forgetting the complement:** A left-tail result is not the right-tail result; subtract from `1.0000`.
- **Assigning positive probability to an exact continuous value:** A single exact value has probability zero.

## Worked Example

**Standardization.** If `mu = 20`, `sigma = 2`, and `x = 17.5`, then `z = (17.5 - 20) / 2 = -1.25`. The negative sign correctly identifies a value 1.25 standard deviations below the mean.

**One-sided probability.** If `mu = 20`, `sigma = 1`, and `x = 22`, then `z = (22 - 20) / 1 = +2.00`. Table B gives the cumulative area to the left as `0.9772`, so `P(X <= 22) = 0.9772`. The probability at or above 22 is the complement: `P(X >= 22) = 1.0000 - 0.9772 = 0.0228`.

**Symmetric probability.** For a cutoff of `z = 2`, Table A gives `0.4772` between the mean and `+2`. Therefore, the area within `+/-2` is `2(0.4772) = 0.9544`, and the area outside it is `1.0000 - 0.9544 = 0.0456`, split equally between the two tails.

## Key Takeaways

1. Compute `z = (x - mu) / sigma` before looking up a probability.
2. Choose Table A for symmetric “within/outside `+/- z`” questions.
3. Choose Table B for one-sided cumulative questions, then complement when the requested side is opposite.
4. The curve’s total area is `1.0000`, each half is `0.5000`, and symmetric tails match.
5. Exact-value probabilities are zero for a continuous normal variable.

## Connects To

- **Appendix B:** Supplies Table A and Tables B1/B2 used for the area lookups.
- **Chapters 7 and 10:** Apply the symmetric `+/- z` table rule.
- **Chapters 4S, 13, and 17:** Apply the one-sided Table B rule.
- **Operations-management analysis:** Standardization and tail probabilities turn process measurements or time limits into comparable probability statements.

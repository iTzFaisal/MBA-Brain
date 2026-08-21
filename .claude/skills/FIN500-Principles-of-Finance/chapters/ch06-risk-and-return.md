# Chapter 6: The Meaning and Measurement of Risk and Return

## Core Idea
Return is the cash benefit from an investment, while risk is the potential variability of future cash flows or returns. Principle 3, **Risk Requires a Reward**, means an investor should require compensation for bearing risk, but diversification can remove company-specific risk so the relevant residual risk is market or systematic risk.

## Frameworks Introduced
- **Holding-period return**
  - **When to use:** Measure the realized return from owning a security over a defined historical period.
  - **How:** First compute the dollar gain, `DG = P_end + dividend - P_begin`. Then divide by the beginning investment: `r_HPR = (P_end + dividend - P_begin)/P_begin`. Use cash flow, not accounting profit, as the return input.
- **Probability-weighted expected return**
  - **When to use:** Forecast an investment with several possible economic states or cash-flow outcomes.
  - **How:** List each outcome, assign probabilities that sum to 1, and calculate `E(CF) = sum[p_i * CF_i]` or `E(r) = sum[p_i * r_i]`. The result is an average, not a guaranteed outcome.
- **Variance and standard deviation**
  - **When to use:** Quantify the dispersion of possible returns when risk is not obvious from inspection.
  - **How:** Compute the expected return, subtract it from every possible return, square each deviation, weight by its probability, and sum: `sigma^2 = sum[p_i(r_i - E(r))^2]`. Take the square root: `sigma = sqrt(sigma^2)`. For a historical sample with equally weighted observations, the source uses the sample form with `n - 1` in the denominator.
- **Diversification and risk decomposition**
  - **When to use:** Decide whether adding securities or asset classes reduces portfolio risk.
  - **How:** Combine assets whose returns are not perfectly correlated. Company-unique (unsystematic) risk can be diversified away; market-wide (systematic) risk cannot. The source observes that risk reduction becomes slight after approximately 20 securities.
- **Characteristic line and beta**
  - **When to use:** Estimate a security's exposure to market movements and the systematic risk relevant to a diversified investor.
  - **How:** Plot security returns against market-index returns and fit the characteristic line. Its slope is beta: a beta of `0.748`, for example, means a 1% market move is associated with an average 0.748 percentage-point move in the security.
- **CAPM and the security market line**
  - **When to use:** Set the minimum acceptable return for a security using its nondiversifiable risk.
  - **How:** Use `r_required = r_f + beta(r_m - r_f)`. The security market line plots this required return against beta. A beta of 0 has only the risk-free return; beta 1 has market risk; beta above 1 has more systematic risk than the typical market security.

## Key Concepts
- **Holding-period return:** Historical or realized return, equal to dollar gain divided by the amount invested.
- **Expected rate of return:** Probability-weighted average of all possible future returns.
- **Risk:** Potential variability in future cash flows or returns.
- **Variance:** Probability-weighted average squared deviation from expected return.
- **Standard deviation:** Square root of variance, used as the conventional measure of total return volatility.
- **Unsystematic risk:** Company-specific risk that diversification can eliminate.
- **Systematic risk:** Market or nondiversifiable risk caused by factors affecting securities broadly.
- **Beta:** Slope relating an investment's returns to market returns; a measure of systematic risk.
- **Portfolio beta:** Weighted average of the individual securities' betas, using portfolio proportions as weights.
- **Risk premium:** Return expected above the risk-free rate for assuming risk.

## Mental Models
- **Risk is dispersion, not simply a bad result.** A high standard deviation can contain upside and downside; compare it with expected return and alternatives.
- **Diversification changes the kind of risk.** More holdings reduce firm-specific noise, but they do not make the portfolio immune to recessions, interest-rate changes, or market shocks.
- **Beta is not total volatility.** A stock can have a large standard deviation but a modest beta if much of its movement is company-specific.
- **Required return is an opportunity-cost threshold.** Invest only when the expected return is sufficient for the systematic risk and the return available elsewhere.

## Anti-patterns
- **Using accounting earnings as the investment benefit:** Financial decisions depend on cash flows generated for investors.
- **Calling every high-risk investment bad:** The right choice depends on the expected return, alternatives, and the investor's attitude toward risk.
- **Assuming diversification eliminates all risk:** Only unsystematic risk is diversifiable; systematic risk remains.
- **Treating beta as a precise truth for every individual stock:** Beta depends on the measurement method and can mislead when company-specific events dominate. It is more reliable for diversified portfolios.
- **Ignoring holding period and asset allocation:** A longer horizon and a mix of stocks and bonds can materially reduce the observed range of outcomes, though they do not guarantee a profit.

## Worked Example
Investment X and Y have the same five outcome probabilities: `0.05, 0.25, 0.40, 0.25, 0.05`. X's possible returns are `-10%, 5%, 20%, 30%, 40%`; Y's are `0%, 5%, 16%, 24%, 32%`.

Applying `E(r) = sum[p_i r_i]` and the probability-weighted standard-deviation procedure gives:

| Investment | Expected return | Standard deviation |
|---|---:|---:|
| X | 18.25% | 11.97% |
| Y | 15.25% | 8.44% |

X offers the higher expected return but also more risk. There is no universal winner: a risk-averse investor may prefer Y, while an investor willing to accept more variability may choose X.

## Key Takeaways
1. Separate realized holding-period return from probability-weighted expected return.
2. Measure an individual investment's total variability with standard deviation, not intuition alone.
3. Diversify across imperfectly correlated securities to remove company-unique risk.
4. For a broadly diversified investor, beta and systematic risk determine the relevant risk premium.
5. Use CAPM to translate beta into a required return: `risk-free rate + beta * market risk premium`.
6. Higher expected return is a reward for accepting risk, not evidence that the investment is automatically superior.

## Connects To
- **Chapter 5: Time Value of Money:** Expected or required returns become the rates used to discount cash flows.
- **Chapter 7: Bond Valuation:** Bond ratings, default risk, and market rates determine the required return used in price valuation.
- **Chapter 8: Stock Valuation:** CAPM and dividend-based returns provide inputs for preferred and common-stock valuation.
- **Chapter 9: Cost of Capital:** CAPM beta and market risk premiums estimate the firm's cost of common equity and divisional WACCs.

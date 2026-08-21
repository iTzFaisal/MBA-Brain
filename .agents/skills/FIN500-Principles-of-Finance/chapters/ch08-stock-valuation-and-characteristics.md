# Chapter 8: The Valuation and Characteristics of Stock

## Core Idea
Stock value is the present value of the cash flows investors expect to receive. Preferred stock generally supplies a fixed dividend in perpetuity; common stock represents residual ownership, so its dividends and price can grow with profitable reinvestment. Apply the same three principles throughout: cash flow matters, money has a time value, and risk requires a reward.

## Frameworks Introduced
- **Preferred-stock claim and protection framework**
  - **When to use:** Evaluate the risk and cash-flow rights of a preferred issue before valuing it.
  - **How:** Preferred stock has no fixed maturity and fixed dividends, ranks after debt but before common stock in claims on assets and income, and often has cumulative dividends, protective provisions, convertibility, a call provision, or a sinking fund. A callable issue may require a higher return because the firm can redeem it when doing so benefits the firm.
- **Preferred-stock perpetuity valuation**
  - **When to use:** Value nonmaturing preferred stock with a constant dividend.
  - **How:** Estimate the dividend and required return, then use `V_ps = D/r_ps`. If buying at the market price, the expected return is `r_ps = D/P_ps`.
- **Common-stock ownership and residual-return framework**
  - **When to use:** Distinguish common equity from creditor or preferred claims.
  - **How:** Common shareholders receive residual income after debt and preferred claims, have a residual claim on assets in liquidation, limited liability, voting rights, and often preemptive rights. The upside is not capped, but dividends are not guaranteed and common claims are last.
- **Internal-growth framework**
  - **When to use:** Estimate a sustainable dividend and earnings growth rate from reinvestment.
  - **How:** `g = ROE * pr`, where `pr` is the percentage of earnings retained. Since `pr = 1 - dividend-payout ratio`, a firm grows internally only through retained profits reinvested in the business. Growth creates value only when reinvestment earns an attractive return relative to the required return.
- **Constant-growth dividend model**
  - **When to use:** Value common stock when dividends are expected to grow at a constant rate forever and `r_cs > g`.
  - **How:** Forecast next year's dividend `D1 = D0(1 + g)`, then use `V_cs = D1/(r_cs - g)`. This is the present value of the growing dividend stream, not a valuation based solely on earnings.
- **Stockholder return decomposition**
  - **When to use:** Decide whether the current market price meets an investor's hurdle rate.
  - **How:** For common stock, `r_expected = D1/P_cs + g`: dividend yield plus expected price-growth rate. For preferred stock, use dividend yield alone. Buy only when expected return is at least the investor's required return.

## Key Concepts
- **Preferred stock:** Hybrid security with fixed dividends, no fixed maturity, and priority over common stock.
- **Cumulative feature:** Unpaid preferred dividends must be paid before common dividends can be declared.
- **Protective provisions:** Rights or restrictions that protect preferred investors during nonpayment or financial difficulty.
- **Convertible preferred stock:** Preferred shares exchangeable for a predetermined number of common shares.
- **Call provision:** Issuer's right to repurchase preferred shares at stated prices over specified periods.
- **Common stock:** Security representing ownership in a corporation.
- **Limited liability:** Investor's loss is generally limited to the amount invested.
- **Internal growth:** Growth from retaining and reinvesting the firm's profits.
- **Profit-retention rate:** Percentage of earnings retained rather than paid as dividends.
- **Dividend-payout ratio:** Dividends expressed as a percentage of earnings.

## Mental Models
- **Claim hierarchy explains risk.** Debt is paid first, preferred stock next, and common stock receives the residual. Common stock has the greatest upside and the least contractual protection.
- **Retention is an investment decision, not automatically value creation.** Retained earnings increase value only when reinvested at a return that justifies their risk and exceeds the investor's opportunity cost.
- **Common-stock return has two parts.** The investor receives cash dividends and expected capital appreciation; omitting either part understates return.
- **Market price is a return claim.** At the margin, the current price is the price that makes the expected return satisfy the marginal investor's required return.

## Anti-patterns
- **Valuing common stock from earnings alone:** The valuation model discounts cash dividends; earnings matter only insofar as they support future cash flows and growth.
- **Using `D0` as the next dividend:** Forecast `D1 = D0(1 + g)` before applying the constant-growth model.
- **Applying the constant-growth formula when `r <= g`:** The model requires `r > g`; otherwise the perpetuity does not converge.
- **Calling external financing internal growth:** Issuing new shares or acquiring another firm increases size but is not the retained-profit growth relevant to this model.
- **Ignoring redeemability of preferred stock:** The issuer may call the stock when rates fall and refinance cheaply, so the investor should account for that unfavorable option.
- **Treating common dividends as contractual:** The board declares dividends, and common shareholders are paid only after senior claims are met.

## Worked Example
Nike's most recent dividend is `$0.80` per share, EPS is `$2.31`, ROE is `22%`, and the investor requires `16%`. The payout ratio is `0.80/2.31 = 34.6%`, so the retention rate is `65.4%`. Estimate internal growth:

`g = 0.22 * 0.654 = 0.144 = 14.4%`

Using the expected `$0.80` dividend as `D1` in the source example:

`V_cs = 0.80/(0.16 - 0.144) = $50.00`

The investor should not pay more than `$50` if the assumptions are reasonable, because a higher price would reduce the expected return below the required `16%`.

## Key Takeaways
1. Value preferred stock as a constant perpetuity and common stock as the PV of future dividends.
2. Use the claim hierarchy to understand why common stock is riskier than preferred stock and debt.
3. Estimate internal growth with `ROE * retention rate`, then test whether reinvestment actually creates value.
4. In the constant-growth model, forecast `D1` and require `r > g`.
5. Compare a stock's dividend yield plus growth with the investor's required return before investing.
6. Separate internal equity from new stock: flotation costs make external common equity more expensive to the firm.

## Connects To
- **Chapter 5: Time Value of Money:** Preferred stock uses the perpetuity formula, while common stock uses discounted future cash flows.
- **Chapter 6: Risk and Return:** Required returns reflect risk; CAPM can supply the common-stock hurdle rate.
- **Chapter 7: Bond Valuation:** Preferred and common-stock valuation reuse the general asset-value equation developed for bonds.
- **Chapter 9: Cost of Capital:** Stockholder required returns become the cost of retained earnings, preferred stock, or new common equity after flotation costs.

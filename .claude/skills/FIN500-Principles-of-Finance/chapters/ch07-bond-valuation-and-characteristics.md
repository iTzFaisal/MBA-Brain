# Chapter 7: The Valuation and Characteristics of Bonds

## Core Idea
A bond is a long-term debt promise: periodic interest plus repayment of par value at maturity. Its intrinsic value is the present value of those promised cash flows discounted at the investor's required rate of return. Coupon terms determine the cash flows; market-required returns and perceived risk determine the price.

## Frameworks Introduced
- **Bond type and priority framework**
  - **When to use:** Assess the security and default protection before comparing a bond's yield with alternatives.
  - **How:** A debenture is unsecured corporate debt; a subordinated debenture is paid after secured and unsubordinated debt in insolvency; a mortgage bond is secured by real property. A Eurobond is issued in a country different from the currency denomination. A convertible bond adds the option to exchange debt for stock at a prespecified price.
- **Bond terms and cash-flow map**
  - **When to use:** Translate an issue's contract into the cash flows needed for valuation.
  - **How:** Identify par value `M`, coupon rate, coupon payment `I = coupon rate * M`, maturity `n`, payment frequency, call protection, indenture restrictions, and credit rating. The quoted price is normally a percentage of par, so a quote of `103.83` means `$1,038.30` for a `$1,000` bond.
- **Three-step intrinsic valuation process**
  - **When to use:** Estimate what a bond is worth to an investor with a stated required return.
  - **How:** (1) Estimate the amount and timing of coupons and maturity value. (2) Determine the investor's required return from risk-free return plus a risk premium. (3) Discount and add the cash flows:
    - `V_b = sum[I_t/(1 + r_b)^t] + M/(1 + r_b)^n`
- **Semiannual-payment adjustment**
  - **When to use:** Value the typical bond that pays interest twice a year.
  - **How:** Replace `n` years with `2n` periods, replace annual coupon `I` with `I/2`, and replace annual required return `r_b` with `r_b/2` per period. Discount par value over the resulting `2n` periods.
- **Yield and current-income framework**
  - **When to use:** Infer the return embedded in a market price or report the bond's annual cash income.
  - **How:** Yield to maturity is the discount rate that equates the bond's current market price to the PV of coupons and maturity value, assuming the bond is held to maturity. Current yield is only `annual interest payment/current market price`; it excludes the capital gain or loss at maturity.
- **Three bond-valuation relationships**
  - **When to use:** Make a quick price or risk judgment without recomputing every cash flow.
  - **How:** Required return and price move inversely. If required return equals coupon rate, price equals par; if it is higher, the bond sells at a discount; if lower, it sells at a premium. Long-term bonds have greater interest-rate risk than short-term bonds.

## Key Concepts
- **Bond:** Long-term promissory note promising fixed interest and face-value repayment.
- **Debenture:** Unsecured corporate debt backed by the issuer's promise to pay.
- **Mortgage bond:** Bond secured by a lien on real property.
- **Convertible bond:** Debt exchangeable for a prespecified number of common shares or at a prespecified conversion price.
- **Par value:** Face amount repaid at maturity, commonly `$1,000` for corporate bonds.
- **Coupon interest rate:** Contractual annual interest as a percentage of par value.
- **Zero coupon bond:** Bond issued below face value with little or no periodic interest.
- **Maturity:** Time until the issuer returns par value and terminates the bond.
- **Indenture:** Legal agreement specifying bondholder, issuer, and trustee rights and restrictions.
- **Yield to maturity (YTM):** Return implied by the current price if the bond is held to maturity.

## Mental Models
- **A bond is an annuity plus a lump sum.** Coupons are the annuity; par value is the terminal cash flow. This makes Chapter 5's PV tools directly usable.
- **Coupon is contractual, yield is market-based.** A 5% coupon keeps paying on par even when investors now require 8%; the price must fall so the buyer's total yield can reach 8%.
- **Long maturity magnifies rate exposure.** A long-term holder is locked into an old return for more years before principal can be reinvested at the new market rate.
- **High yield can be a warning, not a gift.** A large yield and deep discount may compensate for substantial default risk; the promised yield assumes the issuer pays.

## Anti-patterns
- **Confusing coupon rate, current yield, and YTM:** Coupon is based on par, current yield ignores price appreciation or loss, and YTM incorporates all promised cash flows.
- **Discounting annual coupons when payments are semiannual:** Use half the coupon, half the rate, and twice the number of periods.
- **Assuming par value is market value:** Par is the maturity repayment; market value changes with required returns and risk.
- **Reading a high YTM as a guaranteed return:** Default can prevent receipt of coupons or principal, especially for low-rated or junk bonds.
- **Ignoring contract features:** Calls, call-protection periods, indenture restrictions, collateral, and ratings affect the investor's risk and required return.

## Worked Example
Toyota's `$1,000` bond has a `3.4%` annual coupon, five years remaining, and investors require `2.7%`. The annual coupon is `$34`. Discounting five `$34` payments plus `$1,000` at maturity gives:

`V_b = PV($34 annuity for 5 years at 2.7%) + PV($1,000 in year 5 at 2.7%) = $1,032.33`

Toyota actually pays semiannually. The accurate setup is `10` periods, `$17` per period, and `1.35%` per period:

`V_b = PV($17 annuity for 10 periods at 1.35%) + PV($1,000 in period 10) = $1,032.54`

The small difference illustrates why payment frequency must match the valuation inputs.

## Key Takeaways
1. Start with the bond contract: coupon, par, maturity, payment frequency, security, and rating.
2. Value a bond as the PV of coupons plus the PV of par value at the investor's required return.
3. Use current market-required returns, not the historical coupon rate, as the discount rate.
4. Required return above the coupon rate implies a discount bond; below the coupon rate implies a premium bond.
5. YTM is the complete hold-to-maturity return measure; current yield is only annual coupon income relative to price.
6. Long maturities expose investors to larger price changes when market interest rates move.

## Connects To
- **Chapter 5: Time Value of Money:** Bond valuation is a direct application of annuity and single-sum PV formulas.
- **Chapter 6: Risk and Return:** Credit risk and systematic risk determine the required return and risk premium.
- **Chapter 8: Stock Valuation:** The same intrinsic-value equation applies to preferred and common stock, with different cash-flow patterns.
- **Chapter 9: Cost of Capital:** A bond's market-implied return becomes the firm's before-tax cost of debt, adjusted for flotation costs and taxes.

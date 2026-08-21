# Chapter 10: Reporting and Analyzing Long-Term Liabilities

## Core Idea
Long-term debt supplies large amounts of financing but creates fixed interest and principal obligations. Accounting must separate the contract rate that determines cash interest from the market rate that determines issue price and interest expense, then carry discounts and premiums toward par as the debt matures.

## Frameworks Introduced
- **Debt-versus-equity financing test**: Use before raising capital. Debt preserves owner control, makes interest tax deductible, and can increase return on equity when the assets earn more than the debt costs; it also requires fixed interest and principal payments and magnifies poor performance.
- **Bond-feature risk assessment**: Read the bond indenture for collateral, maturity pattern, registration, conversion, call rights, and sinking-fund requirements. Secured debt pledges assets; debentures are unsecured; term bonds mature on one date, serial bonds in installments; registered and bearer bonds identify holders differently; callable debt can be retired by the issuer and convertible debt can become equity.
- **Rate-to-price rule**: Compare contract and market rates at issuance. Equal rates produce par; contract below market produces a discount and proceeds below par; contract above market produces a premium and proceeds above par. Cash interest is `par value x contract rate x period fraction`.
- **Bond issue-price procedure**: Discount each future principal payment and each periodic interest payment at the market rate per period, then add the present values. For semiannual bonds, divide annual rates by two and double the number of annual periods.
- **Straight-line amortization**: Use when its result is not materially different from effective interest. Total interest expense is total cash interest plus a discount or less a premium; divide the total by the number of interest periods. Discount amortization increases interest expense and carrying value; premium amortization decreases both.
- **Effective-interest amortization**: Use the market rate at issuance and the beginning carrying value. `Interest expense = beginning carrying value x market rate per period`; `cash interest = par x contract rate per period`; discount amortization is expense less cash, while premium amortization is cash less expense. Update carrying value toward par each period.
- **Bond-retirement procedure**: At maturity, carrying value equals par, so debit Bonds Payable and credit Cash for par after the final interest entry. Before maturity, update amortization, remove par and any unamortized discount/premium, record the retirement price, and recognize the difference as gain or loss. Conversion to common stock transfers carrying value to equity with no gain or loss in the source procedure.
- **Long-term note procedure**: Record a note initially at its selling price, equal to face less discount or plus premium. For equal installment payments, use a present-value annuity factor to find the payment; each payment includes interest on beginning carrying value plus principal reduction, so interest declines and principal repayment increases.
- **Debt-feature and debt-to-equity analysis**: Compute `debt-to-equity = total liabilities / total equity`. A lower ratio generally means less financing risk, but compare industry, trend, collateral, maturity, covenants, and income stability before judging.
- **Lease and pension treatment**: In the source's 8e treatment, an operating lease records rent expense and cash for the lessee; a capital lease records an asset and liability at the present value of payments, then depreciation and interest. A defined-benefit pension is underfunded when the accumulated benefit obligation exceeds plan assets and overfunded when assets exceed the obligation.

## Key Concepts
- **Bond**: Written promise to pay par value at maturity plus contract-rate interest.
- **Bond indenture**: Legal contract specifying issuer and bondholder rights and obligations.
- **Par/face value**: Principal repaid at maturity.
- **Contract rate**: Stated or coupon rate used to calculate cash interest.
- **Market rate**: Rate investors demand for the risk and term of the debt.
- **Carrying value**: Par less unamortized discount or plus unamortized premium.
- **Discount on Bonds Payable**: Contra-liability reducing carrying value below par.
- **Premium on Bonds Payable**: Adjunct liability increasing carrying value above par.
- **Effective-interest method**: Allocates interest using market rate times beginning carrying value.
- **Installment note**: Note repaid through a series of payments containing interest and principal.

## Mental Models
- **Think contract rate for cash, market rate for economics**: Never use the stated rate to compute expense on a discount or premium bond; it only determines the cash paid.
- **See amortization as a bridge to par**: A discount raises carrying value each period; a premium lowers it. Both reach par exactly at maturity.
- **Build the debt timeline first**: Identify issue date, payment dates, market rate per period, maturity, carrying value, and current portion before journalizing.
- **Treat leverage as a trade-off, not a score**: Debt can raise equity returns when operating returns exceed interest, but fixed obligations make downturns more dangerous.

## Anti-patterns
- **Issuing every bond at face value**: If contract and market rates differ, present value determines a discount or premium.
- **Using annual rates with semiannual periods**: Divide the rate by two and use twice as many periods.
- **Treating a bond discount as an asset**: It is a contra liability and is amortized into interest expense.
- **Keeping interest expense equal under effective interest**: Expense changes with the carrying value; straight-line is the constant-allocation method.
- **Retiring debt without updating amortization**: The resulting gain or loss will be wrong.
- **Calling bondholders owners**: Bonds create creditor claims; stock creates equity and voting rights.
- **Hiding lease debt or collateral details**: Off-balance-sheet financing and pledged assets affect creditor risk and require appropriate disclosure.

## Worked Example
Fila issues two-year, $100,000 bonds with an 8% annual contract rate and semiannual interest. The 10% annual market rate is 5% per half-year. The issue price is `($100,000 x 0.8227) + ($4,000 x 3.5460) = $96,454`, so the discount is $3,546:

```text
Dec. 31  Dr Cash                              $96,454
Dr Discount on Bonds Payable                    3,546
    Cr Bonds Payable                                    $100,000
```

At the first six-month payment, cash interest is `$100,000 x 8% x 1/2 = $4,000`. Effective interest is `$96,454 x 5% = $4,823`; discount amortization is `$823`. The entry is `Dr Bond Interest Expense $4,823 / Cr Discount on Bonds Payable $823 / Cr Cash $4,000`, and the new carrying value is `$97,277`. The same procedure produces expense of $4,864, $4,907, and $4,952 in later periods; the carrying value reaches $100,000 at maturity.

## Key Takeaways
1. Compare contract and market rates before recording a bond; the difference determines discount, par, or premium.
2. Price bonds as the present value of principal plus periodic interest discounted at the market rate per period.
3. Under effective interest, compute expense from beginning carrying value and the issuance-date market rate.
4. Reconcile cash interest, interest expense, and discount/premium amortization every payment period.
5. Update the carrying value before early retirement; maturity retirement is at par, while conversion transfers carrying value to equity.
6. For installment notes, split each equal cash payment into declining interest and increasing principal.
7. Evaluate debt-to-equity with debt features, collateral, maturity, earnings volatility, and industry benchmarks.

## Connects To
- **Chapter 8**: Long-term assets may be purchased or financed through debt; capital leases create both asset and liability balances.
- **Chapter 9**: Current portions of long-term debt, accrued interest, and short-term notes use the same time and classification logic.
- **Chapter 11**: Bond conversion removes debt and records common stock and paid-in capital.
- **Chapter 12**: Bond proceeds, principal repayments, and noncash conversions affect financing cash-flow analysis.

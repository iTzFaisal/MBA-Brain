# Appendix B: Applying Present and Future Values

## Core Idea
Present and future value translate money across time at a stated interest rate. A present value is today's equivalent of a future amount; a future value is the amount today's money accumulates to. The procedure is exact only when the rate and number of periods use the same compounding interval.

## Frameworks Introduced
- **Time-line identification**: Use a timeline before computing. Mark today's amount, each payment date, the target date, the periodic interest rate `i`, the number of periods `n`, and whether the cash flow is a single amount or an ordinary annuity.
- **Present value of a single amount**: Use when one known future payment is discounted to today: `PV = FV / (1 + i)^n`. Table B.1 gives the factor `1/(1+i)^n`; multiply the factor by `FV`. To solve for an unknown `n` or `i`, divide `PV/FV`, then locate the nearest factor in the table.
- **Future value of a single amount**: Use when one current amount grows to a future date: `FV = PV x (1+i)^n`. Table B.2 gives the factor `(1+i)^n`; multiply it by `PV`. The future-value and present-value factors are reciprocals, apart from rounding.
- **Ordinary-annuity procedure**: Use for equal payments at equal end-of-period intervals. For present value, multiply the payment by the Table B.3 present-value-of-an-annuity factor. For future value at the final payment date, multiply the payment by the Table B.4 future-value-of-an-annuity factor. Excel equivalents shown in the appendix are `=-PV(rate, periods, payment)` and `=-FV(rate, periods, payment)`.
- **Compounding alignment rule**: Convert an annual rate to the rate per payment period and convert years to the matching number of periods. For 12% compounded monthly, use `i = 1%` and `n = 12` for one year; for 8% compounded quarterly over five years, use `i = 2%` and `n = 20`.

## Key Concepts
- **Present value (PV)**: Amount that can be invested today at the required rate to equal a future amount.
- **Future value (FV)**: Amount accumulated at a future date from a present investment.
- **Interest/discount rate**: Compensation per compounding period for using money.
- **Compounding**: Earning interest on the original amount and prior interest.
- **Period (`n`)**: Number of matched interest/payment intervals.
- **Present-value factor**: Table multiplier that discounts one future dollar.
- **Future-value factor**: Table multiplier that compounds one present dollar.
- **Ordinary annuity**: Equal payments made at the end of equal periods.
- **Annuity factor**: Sum of single-amount factors for a series of equal payments.

## Mental Models
- **Use a timeline, not a memorized table**: The payment date determines whether it is a single amount or an annuity and which table applies.
- **Match the units rule**: Monthly cash flows require monthly rate and monthly periods; never combine an annual rate with monthly `n`.
- **Think of PV and FV as equivalent dates**: At the required return, the investor is indifferent between the discounted future amount and the present amount.
- **Treat ordinary annuities as end-of-period by default**: A beginning-of-period annuity needs a timing adjustment; do not silently use the ordinary-annuity factor.

## Anti-patterns
- **Using the annual rate with a periodic count**: This compounds the wrong number of times and materially misstates value.
- **Discounting a stream as one single amount**: Each annuity payment occurs at a different date; use an annuity factor or discount each payment separately.
- **Forgetting that tables assume an amount of 1**: Multiply the table factor by the actual PV, FV, or payment.
- **Comparing a lump sum and installments without a common date**: Convert both alternatives to present or future value before choosing.
- **Treating table rounding as exact**: Factors are estimates; use a calculator or spreadsheet when precision affects the decision.

## Worked Example
A company expects an investment to pay $70,000 after six years and requires an 8% return. Table B.1 gives the present-value-of-1 factor `0.6302` for `i = 8%` and `n = 6`:

```text
PV = $70,000 x 0.6302 = $44,114
```

Thus $44,114 today is the maximum price under the stated return, subject to the table's rounding. The same logic values a six-period stream: a $10,000 payment every six months for three years at an 8% annual return uses `i = 4%`, `n = 6`, and Table B.3 factor `5.2421`, giving `PV = $52,421`.

## Key Takeaways
1. Draw the timeline and identify the target date before selecting a formula or table.
2. Use PV for a current price or borrowing amount and FV for an accumulated investment balance.
3. Convert both the interest rate and number of periods to the same compounding interval.
4. Use annuity tables for equal end-of-period payments and single-amount tables for one payment.
5. Compare alternatives only after expressing them at the same date and required return.

## Connects To
- **Chapter 10**: Bond and note prices are present values of principal and interest cash flows.
- **Chapter 12**: Cash-flow forecasts and investment decisions use equivalent-date cash amounts.
- **Chapter 13**: Financial analysis can compare investment growth and return assumptions.
- **Appendix B tables**: Tables B.1-B.4 provide the single-amount and annuity factors used in the procedures.

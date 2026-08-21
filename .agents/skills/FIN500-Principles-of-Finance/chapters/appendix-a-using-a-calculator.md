# Appendix A: Using a Calculator

## Core Idea
The BA II Plus and HP 10BII do not replace financial reasoning; they solve time-value-of-money and cash-flow equations once the periods, timing, signs, and rate conventions are entered correctly. A reliable workflow is to clear prior registers, set payments per year and BEGIN/END timing, enter cash flows with consistent signs, compute, and sanity-check the result.

## Frameworks Introduced
- **TVM-variable workflow**
  - When to use: For a single payment, annuity, loan, savings goal, or project with equal periodic cash flows.
  - How: Set `P/Y` (payments per year) and `END` or `BEGIN`; clear TVM variables; enter any four of `N`, `I/Y`, `PV`, `PMT`, and `FV`; press `CPT` for the fifth. Use negative values for cash paid out and positive values for cash received. The calculator reports annual `I/Y` while `P/Y` converts the periodic rate.
- **Table-value framework**
  - When to use: When finding a single discount or accumulation factor or the value of a level annuity.
  - How: The underlying relationships are `FV of $1 = (1 + i)^n`, `PV of $1 = 1/(1 + i)^n`, `FV annuity = PMT * ((1+i)^n - 1)/i`, and `PV annuity = PMT * (1 - (1+i)^(-n))/i`. Enter the payment as a negative amount when it represents an investment.
- **Bond valuation workflow**
  - When to use: When valuing a coupon bond or solving its yield to maturity.
  - How: Set `P/Y = 2` for semiannual payments, use `N = years * 2`, enter semiannual coupon in `PMT`, par value in `FV`, and annual required return in `I/Y`. Alternatively use the calculator's bond feature: enter settlement date, coupon rate, maturity date, redemption value, 360-day convention, and semiannual frequency; solve `PRI` for price or `YLD` for yield.
- **NPV/IRR workflow**
  - When to use: For capital projects with equal or unequal annual cash flows.
  - How: For equal cash flows, use TVM to find PV, subtract the initial investment for NPV, then solve `I/Y` with the initial outlay as `PV` for IRR. For unequal cash flows, clear the cash-flow worksheet, enter `CF0`, each `CFj`, and repetition count (`Fj` on BA II Plus or `Nj` on HP 10BII), enter the discount rate, and compute NPV or IRR. Include salvage value in the final cash flow.
- **Cross-check workflow**
  - When to use: Whenever a result affects an investment decision or a date/rate convention is easy to misenter.
  - How: Verify the sign of the result, ensure the number of periods matches the payment frequency, and compare the dedicated bond/CF function with a TVM or hand-calculated reasonableness check.

## Key Concepts
- **TVM variables**: `N` periods, `I/Y` annual interest rate, `PV` present value, `PMT` periodic payment, and `FV` future value.
- **P/Y**: Number of payments or compounding periods per year.
- **END mode**: Cash flows occur at the end of each period.
- **BEGIN mode**: Cash flows occur at the beginning of each period.
- **Cash-flow sign convention**: Outflows are negative and inflows are positive.
- **Annuity**: Equal cash flows repeated for a fixed number of periods.
- **Bond price**: Present value of coupon payments plus redemption value.
- **Yield to maturity (YTM)**: Rate that equates a bond's price with its promised cash flows.
- **Net present value (NPV)**: Present value of future project cash flows less the initial investment.
- **Internal rate of return (IRR)**: Rate that makes NPV equal to zero.

## Mental Models
- **The calculator is a cash-flow equation solver**: If the economic cash flows are wrong, a precise display is still a wrong answer.
- **Timing is part of the finance**: BEGIN versus END and annual versus monthly payments change the value, not merely the keystrokes.
- **Signs describe perspective**: A negative PV is usually the investor's payment; the same transaction can appear positive from the counterparty's perspective.
- **Use two paths for high-stakes answers**: A TVM setup and a dedicated bond or cash-flow worksheet should agree after rate and date conventions are aligned.

## Anti-patterns
- **Reuse uncleared registers**: Old TVM or cash-flow values silently contaminate the new calculation; clear `CLR TVM`, `CLR WORK`, or the HP registers first.
- **Leave the wrong P/Y or timing mode active**: A monthly annuity entered with annual periods, or an end-of-period deposit entered in BEGIN mode, produces a systematically wrong result.
- **Enter every amount as positive**: Without opposing cash-flow signs, the calculator may reject the solution or return the wrong perspective.
- **Omit final salvage value**: Add salvage to the final year's operating cash flow before computing NPV and IRR.
- **Treat annual rates as periodic rates**: Set `P/Y` and enter the annual rate in `I/Y`; do not manually mix annual and monthly periods.

## Worked Example
A project costs `$80,000`, pays `$15,000` at each year-end for 10 years, and uses a 12% cost of capital.

1. Set `P/Y = 1`, `END`, `N = 10`, `I/Y = 12`, `PMT = +15,000`, and compute `PV`: `-$84,753.3454` (a `$84,753.3454` inflow value from the investor's perspective).
2. NPV is `$84,753.3454 - $80,000 = $4,753.3454`.
3. Enter the initial outlay as `PV = -80,000` while retaining the 10-year, `$15,000` cash-flow stream and solve `I/Y`: `IRR = 13.4344%`.
4. Since NPV is positive at 12% and IRR exceeds 12%, the project passes those decision tests.

## Key Takeaways
1. Clear the calculator and set payment frequency and timing before entering financial values.
2. Use consistent cash-flow signs and let the required unknown be the only value computed.
3. Match periods, rates, coupon payments, and dates; semiannual bonds require semiannual periods and coupon amounts.
4. For unequal project cash flows, use the CF worksheet and include repetition counts and terminal salvage.
5. Treat calculator output as a check on a correctly specified cash-flow model, not as a substitute for one.

## Connects To
- **Chapter 14**: Forecasted cash budgets and pro forma cash flows supply the timing inputs for valuation.
- **Chapter 16**: Foreign investment cash flows must be converted to a consistent currency before NPV analysis.
- **Chapter 17**: Security yields, marketable-securities prices, and opportunity costs use present-value and rate calculations.
- **Time value of money**: Every TVM, bond, NPV, and IRR function is an application of discounting cash flows at the appropriate rate and date.

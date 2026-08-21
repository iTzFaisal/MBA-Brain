# Chapter 5: The Time Value of Money

## Core Idea
A dollar available today is worth more than a dollar received later because today's dollar can earn a return. Financial decisions become comparable only after every cash flow is moved to a common date by compounding forward or discounting back at an appropriate rate.

## Frameworks Introduced
- **Timeline method**
  - **When to use:** Begin every time-value-of-money problem with cash flows at different dates, especially when the stream is uneven or includes an annuity.
  - **How:** Put time 0 (today) first, mark each period, place positive inflows and negative outflows at the date they occur, and write the rate per period above the line. Then decide whether each flow must be compounded forward or discounted back.
- **Single-sum compounding and discounting**
  - **When to use:** Move one amount between the present and a future date.
  - **How:** Use `FV_n = PV(1 + r)^n` to compound forward and `PV = FV_n/(1 + r)^n` to discount back. The rate and `n` must refer to the same period. `r` and `n` move value in opposite directions for present value: a higher rate or longer wait lowers PV.
- **Annuity framework**
  - **When to use:** Handle equal payments for a fixed number of periods, such as savings deposits, loan payments, bond coupons, or pension withdrawals.
  - **How:** For an ordinary annuity, payments occur at period-end:
    - `FV_annuity = PMT[((1 + r)^n - 1)/r]`
    - `PV_annuity = PMT[1 - (1 + r)^(-n)]/r`
    An annuity due pays at period-beginning, so multiply the corresponding ordinary-annuity value by `(1 + r)`.
- **Comparable-rate framework**
  - **When to use:** Compare loans or investments quoted with different compounding frequencies.
  - **How:** Convert the quoted APR to a periodic rate `APR/m`, use `mn` periods, and compare effective annual rates: `EAR = (1 + APR/m)^m - 1`. APR is a nominal annual rate without intra-year compounding; EAR reflects the true annual compound return.
- **Uneven-stream and perpetuity framework**
  - **When to use:** Value project cash flows that are not a single sum or equal annuity.
  - **How:** Discount each flow individually and add inflows while subtracting outflows. A constant perpetuity has the shortcut `PV_perpetuity = PP/r`; a delayed annuity is first valued at the date its payments begin and then discounted to today.

## Key Concepts
- **Time value of money:** The opportunity cost of receiving a dollar later rather than investing it today.
- **Compound interest:** Interest is added to principal, so later interest is earned on prior interest as well.
- **Future value (FV):** The amount an investment grows to at a specified future date.
- **Present value (PV):** The value today of a future payment discounted at the required rate of return.
- **Future value factor:** `(1 + r)^n`, the multiplier that compounds a present amount.
- **Annuity:** Equal dollar payments for a specified number of periods.
- **Ordinary annuity:** An annuity whose payments occur at the end of each period.
- **Annuity due:** An annuity whose payments occur at the beginning of each period.
- **Amortized loan:** A loan repaid with equal periodic payments, with the interest portion declining and principal portion increasing over time.
- **Perpetuity:** An annuity with an infinite life and a constant payment.

## Mental Models
- **Cash flows have dates, not just amounts.** Treat a promised $1,000 as incomplete information until its timing and risk-adjusted rate are known.
- **Discounting is inverse compounding.** Use the same relationship in either direction; only the unknown and the investor's viewpoint change.
- **Rate-period matching is non-negotiable.** Monthly cash flows require a monthly rate and number of months; annual inputs mixed with monthly inputs produce a false answer.
- **EAR is the comparison lens.** A lower quoted APR can still be more expensive when it compounds more frequently.

## Anti-patterns
- **Comparing APRs with different compounding frequencies:** Convert to EAR first; otherwise the displayed annual rates are not economically comparable.
- **Treating a beginning-of-period payment as an ordinary annuity:** Shift the value by `(1 + r)` for an annuity due.
- **Reusing calculator variables:** Clear the time-value registers or enter zero for unused variables; stale `PV`, `FV`, or `PMT` values contaminate the next answer.
- **Using inconsistent signs or units:** Enter at least one positive and one negative cash flow, and use a per-period rate. For a calculator, a rate may be entered as a percent; for a spreadsheet, use a decimal or percent notation.
- **Rounding a periodic rate too early:** Use `APR/m` at full precision, particularly for monthly loans.

## Worked Example
You can handle monthly mortgage payments of `$1,250` for 30 years at an APR of `6.5%`, compounded monthly. Treat the mortgage as the present value of an ordinary annuity:

`r = 0.065/12`, `n = 30*12 = 360`

`PV = 1,250[1 - (1 + 0.065/12)^(-360)]/(0.065/12)`

`PV = $197,763.52`

Thus, under these assumptions, the largest principal supported by the stated payment stream is about `$197,764`. The calculation works because the cash-flow frequency, rate, and number of periods all use months.

## Key Takeaways
1. Draw the timeline before calculating; it exposes timing, signs, and the correct number of periods.
2. Use `FV_n = PV(1 + r)^n` and its inverse to put single cash flows in comparable dollars.
3. Use annuity formulas only when payments are equal and their timing is correctly classified.
4. Convert nonannual rates and periods consistently, and use EAR when comparing quoted rates.
5. Add discounted cash flows only after they have been brought to the same date.
6. The discount rate should represent the return available on an investment with comparable risk.

## Connects To
- **Chapter 6: Risk and Return:** The required or discount rate compensates investors for risk and opportunity cost.
- **Chapter 7: Bond Valuation:** A bond is an annuity of coupon payments plus a discounted maturity value.
- **Chapter 8: Stock Valuation:** Preferred stock uses the perpetuity shortcut; common stock discounts a growing dividend stream.
- **Chapter 9: Cost of Capital:** WACC supplies a risk-appropriate discount-rate benchmark for firm investment decisions.

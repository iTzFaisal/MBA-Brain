# Finance Patterns

Use these as compact workflows. Keep the decision perspective, timing, signs, and assumptions visible.

## Common-Size and Ratio Diagnosis

**When to use** - A firm, peer, or trend needs an operating and financial diagnosis.

**How** - Convert statement lines to common-size percentages. Ask the five questions: liquidity, operating profit on assets, financing, return to owners, and shareholder value. Compare across time and with suitable peers; decompose `OROA = operating margin * asset turnover`, then inspect receivable, inventory, fixed-asset turnover, debt ratio, and interest coverage.

**Trade-offs** - Ratios reveal questions, not verdicts. Seasonality, accounting policy, business model, and excess liquidity can make a high or low ratio misleading.

## TVM Timeline

**When to use** - Cash flows occur at different dates, frequencies, or amounts.

**How** - Mark time 0 and each period, place signed flows at their dates, and write the per-period rate above the timeline. Discount or compound every flow to one date. Match months with monthly rates and distinguish ordinary annuities from annuities due; compare quoted rates with EAR.

**Trade-offs** - A calculator is faster, but a wrong period, sign, or `BEGIN/END` setting gives a precise wrong answer. Clear registers and sanity-check direction and magnitude.

## Asset Valuation

**When to use** - Pricing a bond, preferred stock, or common stock from expected investor cash flows.

**How** - Identify the claim's contractual or expected cash flows, select a risk-matched required return, and discount to the valuation date. Treat a bond as coupons plus par; preferred stock as `D/r`; common stock as dividends plus expected growth, using `D1/(r-g)` only if `r > g`.

**Trade-offs** - A higher required return lowers price. Coupon, current yield, and YTM are different; dividend growth creates value only when retained funds earn an attractive return.

## CAPM and WACC

**When to use** - Setting a hurdle rate for a security or project.

**How** - For diversified investors, estimate equity cost with `rf + beta(rm-rf)`. Estimate debt from current promised cash flows and net proceeds, apply the interest tax shield, add preferred cost, and weight components to form WACC. Use market or target weights and a divisional or pure-play WACC when risk differs.

**Trade-offs** - Debt tax savings reduce cost, while flotation costs, distress, agency costs, and lost flexibility increase it. One company-wide WACC can misprice heterogeneous projects.

## Capital-Budgeting Tests

**When to use** - Accepting, rejecting, or ranking fixed-asset projects.

**How** - Discount incremental after-tax FCF at the risk-appropriate `k`. Accept an independent project when `NPV >= 0`; use IRR or MIRR as supporting return measures and `PI >= 1` as an independent-project screen. Use payback only for liquidity. Under rationing, choose the feasible set with the largest total NPV; equalize lives with replacement chains or EAA.

**Trade-offs** - IRR and PI can rank unequal-size or mutually exclusive projects incorrectly; multiple sign changes can create multiple IRRs. NPV measures dollars of wealth and is the tie-breaker.

## Free-Cash-Flow Construction

**When to use** - Building a project or firm cash-flow forecast.

**How** - Apply the with-versus-without test. Build initial outlay, annual operating FCF, and terminal FCF. Use `OCF = Delta EBIT - Delta taxes + Delta depreciation`; subtract increases in NOWC and capital spending, include opportunity costs and synergies, exclude sunk costs and interest, recover NOWC at the end, and add after-tax salvage.

**Trade-offs** - Accelerated depreciation changes tax timing, not total depreciation. More working capital can protect operations but ties up cash; a static NPV can omit valuable delay, expansion, or abandonment options.

## Break-Even and Leverage

**When to use** - Testing sales sensitivity and financing plans.

**How** - Compute `break-even units = fixed costs/(price-variable cost)`. Trace `sales -> EBIT -> EPS` with DOL, DFL, and `DTL = DOL * DFL`; use EBIT-EPS indifference points to compare plans across outcomes. Check coverage and debt capacity under adverse EBIT, not just the base case.

**Trade-offs** - Fixed costs magnify upside and downside. The interest tax shield may lower WACC, but leverage raises distress, agency, refinancing, and earnings-volatility risk. EPS is not the shareholder-wealth objective.

## Dividend and Financing Choices

**When to use** - Deciding how much cash to retain, distribute, or raise externally.

**How** - Fund all acceptable positive-NPV projects and the target financing mix first. Use retained earnings for the equity portion while available, issue new equity only afterward, and distribute the residual subject to liquidity, law, covenants, taxes, control, clientele, information, and expectations. Compare a dividend with a fair-price repurchase.

**Trade-offs** - Retention is valuable only when reinvestment creates value; a payout can force costly external equity. Stable policy can support credibility, but repurchases can be flexible and may change leverage or signal valuation.

## Percent-of-Sales and Cash Budget

**When to use** - Forecasting financing needs over a planning period, especially with growth or seasonality.

**How** - Forecast sales and expenses, apply sales ratios only to genuinely proportional accounts, project assets, identify spontaneous liabilities and retained earnings, then calculate `DFN = change in assets - change in spontaneous liabilities - change in retained earnings`. Use monthly receipts, disbursements, minimum cash, borrowing, and repayment in the cash budget.

**Trade-offs** - Percent-of-sales is cheap but misses fixed minimums, capacity steps, and economies of scale. EFN includes spontaneous financing; DFN isolates financing management must actively obtain. Profit can rise while cash timing creates a deficit.

## Cash Conversion Cycle and Short-Term Credit

**When to use** - Cash is tied up in receivables or inventory, or alternative credit sources have different terms.

**How** - Measure `CCC = DSO + DSI - DPO`. Accelerate collections, improve inventory turns, and use supplier terms responsibly. Compare credit on usable proceeds, interest, discounts, fees, compensating balances, APR/APY, security, availability, and maturity; match temporary assets with temporary debt and permanent assets with permanent financing.

**Trade-offs** - Lower CCC can sacrifice sales, stock availability, or supplier support. Short debt may be cheap but exposes the firm to rollover and rate risk; commercial paper needs a liquidity backstop.

## FX Conversion, Parity, and Arbitrage

**When to use** - Pricing a foreign payment, hedging a known settlement, or evaluating a DFI.

**How** - Label currency units, convert direct and indirect quotes with the correct reciprocal, and account for bid-ask spreads. Use spot for immediate delivery, forward for a locked future rate, cross-rates for triangular comparisons, and IRP/PPP/Fisher relationships as no-arbitrage benchmarks. Value DFI cash after taxes, restrictions, repatriation, conversion, and parent-currency discounting.

**Trade-offs** - A high foreign nominal rate can reflect inflation and depreciation. Parity is a benchmark weakened by transaction costs and barriers; a profitable local subsidiary is not necessarily a valuable parent-currency investment.

## MACRS and Calculator Control

**When to use** - Tax depreciation or a calculator setup affects project value.

**How** - Determine MACRS class, depreciable basis, recovery-year percentages, and half-year or midmonth convention; value the earlier tax shield. On a calculator clear registers, set `P/Y` and timing, enter opposing signs, include terminal salvage, and cross-check NPV or IRR.

**Trade-offs** - Book depreciation is not the tax schedule. Bonus depreciation and MACRS change tax timing, while calculator speed cannot correct an incorrectly specified cash-flow model.

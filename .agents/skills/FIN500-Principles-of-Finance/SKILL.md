---
name: FIN500-Principles-of-Finance
description: "Knowledge base from Foundations of Finance: The Logic and Practice of Financial Management by Arthur J. Keown, John D. Martin, and J. William Petty. Use when applying shareholder wealth, valuation, risk and return, capital budgeting, WACC, working capital, or international finance frameworks."
argument-hint: "[finance decision, calculation, concept, or chapter/topic]"
---

# Foundations of Finance: The Logic and Practice of Financial Management

- **Skill name:** `FIN500-Principles-of-Finance`
- **Book:** *Foundations of Finance: The Logic and Practice of Financial Management*, Tenth Edition
- **Authors:** Arthur J. Keown, John D. Martin, J. William Petty
- **Coverage:** 17 chapters plus Appendix 3A, Appendix 11A, and Appendix A
- **Source length:** about 619 pages
- **Book type:** `text`
- **Depth:** `study`
- **Generated:** 2026-08-21

## How to Use This Skill

1. Classify the question as capital budgeting, capital structure, working capital management, valuation, financial analysis, or international finance.
2. State the decision objective, perspective, currency, timing, risk level, tax assumption, and cash-flow sign convention before calculating.
3. Start with the Core Frameworks below, then open the cited chapter for the full treatment and examples.
4. Prefer incremental, after-tax cash flow and market-based opportunity costs over accounting totals or historical financing rates.
5. Use `glossary.md` for terminology, `patterns.md` for repeatable workflows, and `cheatsheet.md` for a fast decision screen.

## Core Frameworks & Mental Models

### 1. Objective and the five finance principles

- **Use shareholder wealth maximization when** choosing an investment, financing plan, payout, or operating policy. Judge whether the decision increases the market value of existing common stock after considering timing and risk; do not substitute EPS or accounting profit for value.
- **Use the Five Principles That Form the Foundations of Finance when** a problem's logic is unclear. Apply them as a pre-calculation check: **Cash Flow Is What Matters**; **Money Has a Time Value**; **Risk Requires a Reward**; **Market Prices Are Generally Right**; and **Conflicts of Interest Cause Agency Problems**.
- **Use Cash Flow Is What Matters when** comparing an action with the status quo. Count cash that changes because of the decision, not accrual earnings, depreciation, or cash that would occur anyway.
- **Use Money Has a Time Value when** benefits and costs occur at different dates. Put every flow on a timeline and compound or discount it to one common date at a rate for comparable risk and the same period units.
- **Use Risk Requires a Reward when** two alternatives have different uncertainty. Require a higher expected return for greater relevant risk, and distinguish total volatility from the systematic risk that a diversified investor cannot remove.
- **Use Market Prices Are Generally Right when** estimating opportunity costs or interpreting a security price. Treat current market-required returns as the benchmark, while checking for behavioral distortion, liquidity, and information limits.
- **Use Conflicts of Interest Cause Agency Problems when** ownership and control are separated. Align managers and capital providers with disclosure, oversight, covenants, and long-term value incentives.

### 2. Classify the decision before measuring it

- **Use capital budgeting when** deciding whether to acquire, replace, expand, delay, or abandon long-lived assets. **Use capital structure decisions when** selecting debt, preferred stock, and common equity. **Use working capital management when** setting current assets, operating liabilities, and short-term financing.

### 3. Read statements as operating and funding evidence

- **Use the income-statement waterfall when** tracing sales to EBIT, taxes, net income, EPS, or DPS. **Use the balance sheet as a funding map when** each asset must be explained by liabilities or equity; book value is historical-cost evidence, not market value.
- **Use the statement of cash flows when** profit and cash diverge. Separate operating, investing, and financing buckets, add back depreciation, and reverse changes in operating assets and liabilities.
- **Use common-size statements and the five-question approach when** diagnosing liquidity, operating return, financing, owner return, and shareholder value. Decompose `OROA = operating margin * asset turnover`, then investigate turnover, leverage, coverage, seasonality, and accounting choices.

### 4. Build free cash flow before valuing a project or firm

- **Use incremental, after-tax free cash flow when** a project changes operations. Build initial outlay, annual operating FCF, and terminal FCF; `OCF = Delta EBIT - Delta taxes + Delta depreciation`.
- **Use the Appendix 3A cash waterfall when** measuring cash available to all capital providers: `FCF = after-tax operating cash - increase in NOWC - increase in long-term assets`. NOWC excludes interest-bearing short-term debt.
- **Use the terminal-value check when** a project ends. Recover working capital, include after-tax salvage, subtract cleanup, and retain depreciation's tax shield; never subtract interest from project FCF.

### 5. Move value through time and value assets from claims

- **Use the timeline method when** any flow is uneven, delayed, periodic, or easy to mis-time. Match rate and periods to cash-flow frequency; classify ordinary annuity payments as end-period and annuity-due payments as beginning-period.
- **Use `PV = FV/(1+r)^n` and `FV = PV(1+r)^n` when** moving a single amount. Convert APRs with different compounding frequencies to comparable periodic rates or EAR before comparing them.
- **Use the asset-value equation when** valuing a bond or stock: price is the PV of expected cash flows at the required return. A bond is coupons plus par; preferred stock is `D/r`; common stock uses dividends, including `D1/(r-g)` only when `r > g`.
- **Use the claim hierarchy when** interpreting risk: debt has priority, preferred stock is next, and common stock receives the residual. Common-stock return is dividend yield plus expected price growth.

### 6. Measure risk, then set the return hurdle

- **Use expected return, variance, and standard deviation when** comparing outcomes or total volatility. **Use diversification when** reducing unsystematic risk; systematic risk remains.
- **Use beta and CAPM when** the investor is diversified: `required return = risk-free rate + beta * market risk premium`. Beta is not total standard deviation, and required return is an opportunity-cost threshold, not a forecast guarantee.

### 7. Estimate a risk-matched cost of capital

- **Use component costs when** the firm raises debt, preferred stock, retained earnings, or new equity. Estimate current returns from net proceeds and promised cash flows; apply the tax shield to debt, not preferred dividends.
- **Use WACC when** project risk resembles the firm's business: `WACC = wd*after-tax kd + wps*kps + wcs*kcs`. Prefer market or target weights; switch to new-equity cost when internal funds run out.
- **Use a divisional WACC or pure-play comparison when** project risk differs materially. One company-wide rate can misprice projects.

### 8. Select investments with NPV first

- **Use NPV when** accepting independent projects or ranking mutually exclusive alternatives: `NPV = PV of future FCF - initial outlay`. Accept an independent project when `NPV >= 0`; it adds today's wealth.
- **Use IRR or MIRR when** a percentage return is useful, but check signs and let NPV resolve conflicts. Use PI for benefit per dollar, payback as a liquidity screen, and discounted payback when the screen must recognize time value.
- **Use constrained-portfolio selection when** capital is rationed: choose the feasible combination with the largest total NPV, not automatically the highest PI or IRR. Equalize unequal lives with replacement chains or equivalent annual annuity.
- **Use risk-adjusted NPV, sensitivity, scenarios, simulation, or real-options analysis when** one forecast hides uncertainty or management can delay, expand, scale back, or abandon. Flexibility can add value beyond static NPV.

### 9. Balance leverage, risk, and flexibility

- **Use break-even and leverage analysis when** tracing `sales -> EBIT -> EPS`. Fixed operating costs create operating leverage; fixed financial charges create financial leverage. Use `DOL`, `DFL`, and `DTL = DOL * DFL` to expose sensitivity, not to declare the best capital structure.
- **Use the moderate trade-off view when** choosing debt. Weigh the interest tax shield against expected distress, agency, covenant, refinancing, earnings-volatility, and lost-flexibility costs. Seek an optimal range and respect debt capacity and adverse-case interest coverage.
- **Use EBIT-EPS indifference analysis when** comparing financing plans across possible EBIT outcomes. EPS is a sensitivity lens; shareholder wealth, risk, WACC, and the probability of distress remain the decision criteria.

### 10. Treat dividends as residual financing plus communication

- **Use residual dividend theory when** positive-NPV investment and target financing decisions are known. Fund the equity portion with retained earnings first, issue new equity only after internal funds are exhausted, and distribute the remaining safe cash.
- **Use dividend irrelevance, bird-in-the-hand, low-dividend/tax-preference, clientele, information, agency, and expectations views when** explaining why payout changes may affect price. Preserve liquidity and a credible pattern; an unexpected cut can signal weaker prospects.
- **Use a repurchase when** a fair-price, flexible distribution or share-count change fits the objective. Compare taxes, control, valuation, future investment, and remaining-holder effects; a stock split changes pieces, not aggregate value by itself.

### 11. Forecast the funding gap and manage the cash clock

- **Use the three-step forecast when** estimating financing needs: forecast sales and expenses, estimate assets needed, then identify financing. Apply percent-of-sales only to accounts that truly scale with sales.
- **Use DFN when** isolating active financing: `DFN = change in total assets - change in spontaneous liabilities - change in retained earnings`. Use a cash budget when seasonal receipt and payment timing matters; annual profitability does not eliminate a monthly cash shortage.
- **Use the cash conversion cycle when** diagnosing operating cash tied up: `CCC = DSO + DSI - DPO`. Improve it by collecting sooner, turning inventory faster, or extending supplier terms without sacrificing sales, reliability, price, or supplier support.
- **Use effective-cost analysis when** choosing short-term credit. Compare usable proceeds, fees, discounts, compensating balances, APR/APY, availability, security, and maturity risk rather than quoted interest alone. Apply EOQ with its assumptions and add safety stock for uncertainty.

### 12. Keep currencies, taxes, and tools internally consistent

- **Use unit analysis when** converting FX quotes: label currencies, invert only when units require it, and distinguish bid from ask. Use spot for immediate settlement and forward for a known future rate; forward is locked, not a certain future spot forecast.
- **Use IRP, PPP, the law of one price, and the International Fisher effect as parity benchmarks when** checking consistency. **Use the DFI cash-flow screen when** valuing parent-currency cash repatriated after taxes, blocked funds, political constraints, and conversion.
- **Use MACRS when** tax depreciation timing affects FCF. Determine property class and basis, apply the relevant convention and tax percentages, and value earlier tax shields; use tax depreciation rather than book depreciation.
- **Use the calculator as an equation solver when** the timeline, signs, `P/Y`, `BEGIN/END`, rate, periods, and final salvage are already correct. Clear registers and cross-check material results.

## Chapter Index

| ID | Chapter or appendix | Source file |
|---|---|---|
| Ch 1 | An Introduction to the Foundations of Financial Management | [ch01-an-introduction-to-the-foundations-of-financial-management.md](chapters/ch01-an-introduction-to-the-foundations-of-financial-management.md) |
| Ch 2 | The Financial Markets and Interest Rates | [ch02-financial-markets-and-interest-rates.md](chapters/ch02-financial-markets-and-interest-rates.md) |
| Ch 3 | Understanding Financial Statements and Cash Flows | [ch03-understanding-financial-statements-and-cash-flows.md](chapters/ch03-understanding-financial-statements-and-cash-flows.md) |
| Ch 4 | Evaluating a Firm's Financial Performance | [ch04-evaluating-a-firms-financial-performance.md](chapters/ch04-evaluating-a-firms-financial-performance.md) |
| Ch 5 | The Time Value of Money | [ch05-the-time-value-of-money.md](chapters/ch05-the-time-value-of-money.md) |
| Ch 6 | The Meaning and Measurement of Risk and Return | [ch06-risk-and-return.md](chapters/ch06-risk-and-return.md) |
| Ch 7 | The Valuation and Characteristics of Bonds | [ch07-bond-valuation-and-characteristics.md](chapters/ch07-bond-valuation-and-characteristics.md) |
| Ch 8 | The Valuation and Characteristics of Stock | [ch08-stock-valuation-and-characteristics.md](chapters/ch08-stock-valuation-and-characteristics.md) |
| Ch 9 | The Cost of Capital | [ch09-cost-of-capital.md](chapters/ch09-cost-of-capital.md) |
| Ch 10 | Capital-Budgeting Techniques and Practice | [ch10-capital-budgeting-techniques-and-practice.md](chapters/ch10-capital-budgeting-techniques-and-practice.md) |
| Ch 11 | Cash Flows and Other Topics in Capital Budgeting | [ch11-cash-flows-and-other-topics-in-capital-budgeting.md](chapters/ch11-cash-flows-and-other-topics-in-capital-budgeting.md) |
| Ch 12 | Determining the Financing Mix | [ch12-determining-the-financing-mix.md](chapters/ch12-determining-the-financing-mix.md) |
| Ch 13 | Dividend Policy and Internal Financing | [ch13-dividend-policy-and-internal-financing.md](chapters/ch13-dividend-policy-and-internal-financing.md) |
| Ch 14 | Short-Term Financial Planning | [ch14-short-term-financial-planning.md](chapters/ch14-short-term-financial-planning.md) |
| Ch 15 | Working-Capital Management | [ch15-working-capital-management.md](chapters/ch15-working-capital-management.md) |
| Ch 16 | International Business Finance | [ch16-international-business-finance.md](chapters/ch16-international-business-finance.md) |
| Ch 17 | Cash, Receivables, and Inventory Management | [ch17-cash-receivables-and-inventory-management.md](chapters/ch17-cash-receivables-and-inventory-management.md) |
| Appendix 3A | Free Cash Flows | [appendix-3a-free-cash-flows.md](chapters/appendix-3a-free-cash-flows.md) |
| Appendix 11A | The Modified Accelerated Cost Recovery System | [appendix-11a-modified-accelerated-cost-recovery-system.md](chapters/appendix-11a-modified-accelerated-cost-recovery-system.md) |
| Appendix A | Using a Calculator | [appendix-a-using-a-calculator.md](chapters/appendix-a-using-a-calculator.md) |

## Topic Index

| Topic or framework | Chapter identifiers |
|---|---|
| Agency problems and incentives | Ch 1, Ch 12, Ch 13 |
| Asset valuation | Ch 5, Ch 7, Ch 8 |
| Break-even and leverage | Ch 12 |
| Capital budgeting and project ranking | Ch 10, Ch 11, Appendix 3A, Appendix 11A |
| Capital structure and financing mix | Ch 9, Ch 12, Ch 13 |
| Cash conversion cycle | Ch 15, Ch 17 |
| Cash-flow statement and free cash flow | Ch 3, Ch 11, Appendix 3A |
| CAPM and beta | Ch 6, Ch 9, Ch 11 |
| Cost of capital and WACC | Ch 2, Ch 6, Ch 7, Ch 9, Ch 12 |
| Dividend policy and repurchases | Ch 8, Ch 13 |
| Financial forecasting and DFN | Ch 14 |
| Financial markets and interest rates | Ch 2 |
| Financial statements and ratio analysis | Ch 3, Ch 4 |
| Foreign exchange, parity, arbitrage, and DFI | Ch 16 |
| Incremental cash flow and project risk | Ch 1, Ch 10, Ch 11 |
| MACRS and depreciation tax shields | Ch 10, Ch 11, Appendix 11A |
| NPV, IRR, PI, payback, and EAA | Ch 10, Appendix A |
| Operating working capital and short-term credit | Ch 14, Ch 15, Ch 17 |
| Risk, return, and diversification | Ch 1, Ch 6, Ch 9 |
| Shareholder wealth maximization | Ch 1, Ch 10, Ch 13 |
| Stock and bond characteristics | Ch 7, Ch 8 |
| Time value of money and calculator setup | Ch 5, Appendix A |

## Supporting Files

- [glossary.md](glossary.md) - Alphabetical terms and concise chapter references.
- [patterns.md](patterns.md) - Actionable finance workflows with uses and trade-offs.
- [cheatsheet.md](cheatsheet.md) - Compact decision rules and formulas.

## Scope & Limits

This skill synthesizes the assigned chapter and appendix Markdown files for study, framework application, and chapter navigation. It does not provide current market data, tax or legal advice, a substitute for the textbook's assumptions and worked problems, or a guarantee that a model fits a real firm. Validate rates, tax rules, accounting conventions, currency restrictions, data quality, project risk, and contract terms for the actual decision. Formulas are presented in readable study notation; align signs, dates, units, and definitions before using a calculator or spreadsheet.

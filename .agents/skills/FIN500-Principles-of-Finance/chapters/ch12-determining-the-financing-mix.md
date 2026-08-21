# Chapter 12: Determining the Financing Mix

## Core Idea
Financing choices determine how strongly changes in sales and EBIT are amplified into earnings per share and how the firm's cost of capital behaves. The manager's objective is not to maximize debt: it is to choose a prudent capital structure that balances the interest tax shield against financial distress, agency costs, loss of flexibility, and earnings volatility.

## Frameworks Introduced
- **Business, operating, and financial risk decomposition**
  - **When to use:** Use when diagnosing why earnings are volatile before choosing financing.
  - **How:** Separate risk from the chosen business line, from the mix of fixed and variable operating costs, and from fixed financial obligations such as interest and principal. High business or operating risk generally calls for caution with additional financial leverage.
- **Break-even analysis**
  - **When to use:** Use for short-run planning to find the sales volume at which `EBIT = 0` and to see how fixed costs expose the firm to operating risk.
  - **How:** Classify costs over the relevant output range, then calculate:
    `Break-even units = Fixed costs / (Selling price per unit - Variable cost per unit)`
    `Break-even revenue = Fixed costs / [1 - (Variable costs / Revenue)]`
    Treat semivariable costs carefully and do not extrapolate the linear model beyond the relevant range.
- **Operating, financial, and combined leverage**
  - **When to use:** Use to quantify how a percentage change in sales flows through EBIT to EPS.
  - **How:**
    `DOL = % change in EBIT / % change in Sales`
    `DFL = % change in EPS / % change in EBIT`
    `DTL = % change in EPS / % change in Sales = DOL * DFL`
    Fixed operating costs create operating leverage; fixed-rate debt or preferred financing creates financial leverage.
- **MM independence hypothesis and the moderate trade-off view**
  - **When to use:** Use as a theory check: first ask what would happen in perfect markets, then add the frictions that matter in practice.
  - **How:** With no taxes, homogeneous forecasts, perfect markets, and no distress costs, MM says firm value and WACC are independent of debt-equity mix. In reality, interest is tax deductible but excessive debt raises default, distress, and agency costs. The benefit-cost trade-off produces a saucer-shaped or U-shaped WACC curve.
- **Optimal range and debt capacity**
  - **When to use:** Use when setting a target financing mix rather than making a one-period EPS choice.
  - **How:** Seek the debt range that minimizes composite cost of capital and maximizes common stock value. Stop before debt pushes the firm beyond its debt capacity, defined as the maximum debt consistent with its current credit rating and ability to service obligations.
- **EBIT-EPS analysis and comparative ratios**
  - **When to use:** Use to compare debt and equity financing plans over a range of possible operating outcomes, then validate the result against peers and coverage capacity.
  - **How:** Solve the EBIT level at which the two plans produce equal EPS:
    `(EBIT - I_s)(1 - T_c) / S_s - P/S_s = (EBIT - I_b)(1 - T_c) / S_b - P/S_b`
    Above the indifference EBIT, the more leveraged plan produces higher EPS; below it, the less leveraged plan does. Also inspect balance-sheet leverage, coverage ratios at multiple EBIT levels, net debt, and industry norms.
- **Free-cash-flow control hypothesis**
  - **When to use:** Use when profitable investment opportunities are scarce and managers control substantial cash in excess of positive-NPV funding needs.
  - **How:** Debt service can force excess cash to be disgorged and can discipline managers, but the benefit ends when creditor monitoring, distress, and bondholder-stockholder conflicts become more costly.

## Key Concepts
- **Business risk:** Earnings risk arising from the particular industry or business line.
- **Operating risk:** Earnings risk from the firm's fixed-versus-variable operating cost mix.
- **Financial risk:** Earnings risk from fixed finance costs such as interest and principal payments.
- **Break-even quantity:** Units that cover all operating costs and produce `EBIT = 0`.
- **Operating, financial, and combined leverage:** Operating leverage amplifies sales changes into EBIT; financial leverage amplifies EBIT changes into EPS; combined leverage maps sales changes into EPS through both effects.
- **Financial structure versus capital structure:** Financial structure includes all right-hand-side funding; capital structure includes interest-bearing short- and long-term debt plus preferred and common equity, excluding non-interest-bearing payables and accrued expenses.
- **Tax shield:** Tax reduction from deductible interest, `Tax shield = r_b * D * T_c`.
- **Optimal capital structure:** Mix that minimizes composite cost of capital and maximizes common stock price for a given funding need.
- **EBIT-EPS indifference point:** EBIT at which two financing plans produce the same EPS.

## Mental Models
- **Fixed costs are operating leverage.** They do not move with sales, so each sales change hits the residual EBIT disproportionately once fixed costs are covered.
- **Leverage multiplies in layers.** Operating leverage magnifies sales into EBIT; financial leverage magnifies EBIT into EPS. High business risk plus high financial leverage can create unacceptable combined volatility.
- **Debt is a tax shield with a finite budget.** Borrowing initially lowers effective funding cost, but distress and agency costs eventually reverse the benefit.
- **EPS is a sensitivity lens, not the objective.** EBIT-EPS analysis shows volatility and crossover points; it does not by itself maximize firm value or account for all risk.

## Anti-patterns
- **Borrowing as much as possible for the tax deduction:** The tax shield is only one side of the trade-off; default, distress, agency costs, and lost flexibility can destroy value.
- **Choosing the plan with the highest EPS at one forecast EBIT:** EBIT is uncertain, and the more leveraged plan has a steeper, more volatile EPS response.
- **Applying break-even formulas outside their relevant range:** Costs can be semivariable, step-fixed, nonlinear, or altered by learning and capacity constraints.
- **Confusing financial structure with capital structure:** Include payables and accrued expenses in the former, but not in the latter.
- **Treating peer leverage as an automatic target:** Industry norms are a reference point; adjust for business risk, cash holdings, coverage, credit rating, and strategy.
- **Ignoring excess cash when assessing debt risk:** Use net debt when cash is genuinely available to repay interest-bearing debt.

## Worked Example
Pierce Grain has price `$10`, variable cost `$6`, and fixed operating costs `$100,000`, so:

`Break-even units = $100,000 / ($10 - $6) = 25,000 units`

At base sales of `$300,000`, variable costs are `$180,000`, fixed costs `$100,000`, and EBIT `$20,000`. A 20% sales increase to `$360,000` raises variable costs to `$216,000`; EBIT becomes `$44,000`, a 120% increase. The operating leverage therefore magnifies the sales change sixfold at this base point.

Under Pierce's 25%-debt plan, interest is `$4,000` and 1,500 shares are outstanding. EPS rises from `$8.53` at the base case to `$21.33` at the higher-sales case, a 150% increase. The example shows why operating and financial leverage interact multiplicatively and why a high-operating-risk firm should be cautious about adding fixed financial obligations.

In the related financing choice, issuing `$50,000` of new 8.5% debt versus 500 common shares produced an EBIT-EPS indifference point of `$21,000`: above it, debt gave higher EPS; below it, equity gave higher EPS. Management still had to weigh the debt plan's greater EPS volatility and distress exposure.

## Key Takeaways
1. Diagnose business and operating risk before deciding how much financial risk to add.
2. Use break-even analysis as a relevant-range planning tool, not as a complete valuation model.
3. Remember the chain `sales -> EBIT -> EPS`; leverage amplifies each link.
4. Evaluate debt for both its interest tax shield and its distress, agency, covenant, and flexibility costs.
5. Target an optimal range of leverage and respect debt capacity and coverage under adverse EBIT outcomes.
6. Use EBIT-EPS indifference analysis and peer ratios as decision aids, not as substitutes for judgment or shareholder-value analysis.

## Connects To
- **Chapter 9:** The cost of capital and WACC are the rates affected by financing mix and used in investment evaluation.
- **Chapters 10-11:** Capital structure supplies the hurdle rate, while project risk and FCF determine whether the financed assets create value.
- **Chapter 13:** Dividend retention is an internal financing source and a residual choice after investment and capital-structure decisions.

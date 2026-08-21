# Chapter 9: The Cost of Capital

## Core Idea
The firm's cost of capital is the opportunity cost demanded by the investors who supply its debt and equity, adjusted for taxes and issuance costs and blended according to the capital structure. A project creates shareholder value only when its risk-appropriate return exceeds the relevant cost of capital. A single company-wide WACC can misallocate funds when divisions have materially different risk.

## Frameworks Introduced
- **Capital-structure and opportunity-cost framework**
  - **When to use:** Define which financing sources belong in the cost-of-capital calculation and why their costs matter.
  - **How:** Identify interest-bearing debt, preferred stock, and common equity and their relative importance. The cost is the return investors forgo by leaving money invested in the firm, not an historical accounting rate. Accounts payable are excluded from the capital structure in this chapter because their financing cost is embedded in operating prices.
- **Component cost of debt**
  - **When to use:** Estimate the firm's current cost of borrowing.
  - **How:** Solve for the before-tax rate `k_b` that equates net proceeds after flotation costs to the PV of promised interest and principal: `NP_b = sum[I_t/(1 + k_b)^t] + M/(1 + k_b)^n`. Then apply the interest tax shield: `after-tax k_d = k_b(1 - T_c)`, assuming the interest is deductible.
- **Component cost of preferred stock**
  - **When to use:** Estimate the cost of a new preferred issue with a constant dividend.
  - **How:** Divide the annual preferred dividend by net proceeds per share: `k_ps = D/NP_ps`. Preferred dividends are not tax deductible, so there is no tax adjustment.
- **Common-equity cost methods**
  - **When to use:** Estimate the return required by common shareholders when no contractual coupon exists.
  - **How:** For retained earnings, use the implied dividend-growth cost `k_cs = D1/P_cs + g`; there are no flotation costs. For new common shares, replace price with net proceeds: `k_ncs = D1/NP_cs + g`. Alternatively use CAPM: `k_cs = r_f + beta(r_m - r_f)`. CAPM does not include flotation costs, so it estimates internal common equity unless adjusted separately.
- **Weighted average cost of capital (WACC)**
  - **When to use:** Set a firm-level hurdle rate when a project has risk comparable to the firm's existing activities.
  - **How:** Multiply each component cost by its financing weight and sum:
    - `WACC = w_b[k_b(1 - T_c)] + w_ps k_ps + w_cs k_cs`
    Weights must sum to 100%. Use market-value weights in theory; target proportions are practical when the firm maintains a stable financing policy. Replace retained-earnings cost with new-equity cost once internal funds are exhausted.
- **Divisional WACC and pure-play comparison**
  - **When to use:** Evaluate projects in divisions whose systematic risk differs from the company as a whole.
  - **How:** Identify single-segment comparison firms with similar operating risk, estimate the division's after-tax debt cost and CAPM equity cost, apply the division's target debt ratio, and compute a divisional WACC. Use it consistently for projects within that division while recognizing that projects inside one division can still differ in risk.

## Key Concepts
- **Cost of capital:** Return the firm must earn to satisfy the opportunity costs of its capital suppliers.
- **Capital structure:** Mix of long-term debt, preferred stock, and common equity financing.
- **Opportunity cost:** Value of the next-best alternative forgone by making a choice.
- **Flotation costs:** Fees and transaction costs incurred when issuing securities.
- **Cost of debt:** Before-tax return required by creditors, based on current net proceeds and promised cash flows.
- **After-tax cost of debt:** Debt cost after the tax deduction for interest, `k_b(1 - T_c)`.
- **Cost of preferred equity:** Return required on preferred capital, based on dividend and net proceeds.
- **Cost of common equity:** Return required by residual owners, estimated with dividend growth or CAPM.
- **WACC:** Weighted average of the firm's component capital costs.
- **Divisional WACC:** Cost of capital for a specific business unit, adjusted for its risk and target financing mix.

## Mental Models
- **The WACC is a market opportunity cost, not a bookkeeping expense.** A firm can report positive earnings and still destroy value if its return on invested capital is below the return investors require.
- **Taxes and flotation costs create a wedge.** Investors' required returns are not automatically the firm's financing costs; debt tax savings lower the cost, while issuance costs raise it.
- **Use the hurdle rate that matches risk.** One WACC applied to every division accepts too many high-risk projects and rejects too many low-risk projects.
- **Internal equity is not free.** Retained earnings have no flotation fee, but shareholders still forgo the return they could earn elsewhere.

## Anti-patterns
- **Using coupon rate or historical book interest as current debt cost:** Solve from the current market price or net proceeds and promised cash flows.
- **Omitting flotation costs for a new issue:** Use net proceeds, not the public offer price, when estimating debt, preferred, or new common equity cost.
- **Applying the debt tax shield to preferred dividends:** Preferred dividends are not tax deductible in the chapter's framework.
- **Using the retained-earnings cost after internal funds run out:** Switch to the higher new-common-stock cost that includes flotation costs.
- **Using one company-wide WACC for heterogeneous divisions:** This overinvests in high-risk work and underinvests in low-risk work.
- **Treating market and book weights as interchangeable:** Market values theoretically reflect the current financing mix; book values are a fallback when market values are unavailable.
- **Choosing projects by raw return alone:** Compare each return with the cost of capital appropriate to that project's risk.

## Worked Example
Ash Inc. funds its capital with `35%` bonds costing `7%` after tax, `5%` preferred stock costing `13%`, and `60%` retained earnings costing `16%`. For up to `$5 million`, the WACC is:

`WACC = 0.35(0.07) + 0.05(0.13) + 0.60(0.16)`

`WACC = 2.45% + 0.65% + 9.60% = 12.70%`

If Ash must raise more than `$5 million`, it issues new common stock costing `18%` rather than using retained earnings:

`WACC = 0.35(0.07) + 0.05(0.13) + 0.60(0.18) = 13.90%`

The financing threshold matters: the marginal cost of new capital rises once flotation costs are incurred.

## Key Takeaways
1. Estimate component costs from current market-required returns, then adjust for taxes and flotation costs.
2. Debt receives an interest tax adjustment; preferred dividends do not.
3. Retained earnings still have an opportunity cost even though they have no flotation cost.
4. WACC is a weighted average, with weights representing each source's share of total financing.
5. Prefer market-value weights; use target weights when they represent the firm's ongoing financing policy.
6. Match a project's discount rate to its risk, using divisional or pure-play WACCs when company-wide risk is not representative.

## Connects To
- **Chapter 5: Time Value of Money:** Component costs and WACC are discount rates applied to future project cash flows.
- **Chapter 6: Risk and Return:** CAPM supplies the systematic-risk-based cost of common equity and divisional equity costs.
- **Chapter 7: Bond Valuation:** Current bond price and YTM provide the starting point for before-tax debt cost.
- **Chapter 8: Stock Valuation:** Dividend-growth valuation supplies the implied cost of retained earnings and new common equity.

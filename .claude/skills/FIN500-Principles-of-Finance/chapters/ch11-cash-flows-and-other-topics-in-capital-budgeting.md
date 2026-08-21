# Chapter 11: Cash Flows and Other Topics in Capital Budgeting

## Core Idea
Capital-budgeting analysis must use the project's **incremental, after-tax free cash flows**: the difference between the firm's cash flows with and without the project. Build those flows as initial outlay, annual FCFs, and terminal FCF; then recognize flexibility and risk that ordinary NPV may miss.

## Frameworks Introduced
- **The relevant-cash-flow screen**
  - **When to use:** Apply before calculating any NPV, PI, or IRR to decide which cash flows actually change if the project is accepted.
  - **How:** Compare the firm with and without the project. Include incremental after-tax sales, expenses, working capital, capital spending, opportunity costs, and synergies. Subtract cannibalized sales and other incremental costs. Exclude sunk costs and interest or other financing flows; the required return already prices the financing opportunity cost.
- **Three-part free-cash-flow build**
  - **When to use:** Use for every new-project or replacement analysis.
  - **How:**
    `Initial outlay = new asset cost + shipping/installation/training + initial NWC - after-tax sale proceeds of old asset`
    `Annual OCF = Delta EBIT - Delta taxes + Delta depreciation`
    `Project FCF = Delta EBIT - Delta taxes + Delta depreciation - Delta NWC - Delta capital spending`
    In the terminal year add after-tax salvage value, recover NWC, and subtract termination or cleanup costs. A positive increase in NWC is a cash outflow; liquidation creates a cash inflow.
- **Depreciation and tax-shield timing**
  - **When to use:** Use when translating pro forma income into cash flow.
  - **How:** Depreciation is noncash, so add it back, but retain its tax effect because it lowers taxable income. Bonus depreciation puts the tax benefit early; MACRS spreads it over the recovery period. Do not subtract interest from FCF because discounting at the required return would double-count financing cost.
- **Real-options analysis**
  - **When to use:** Use when management can wait, expand, scale back, sell, or abandon after uncertainty is resolved.
  - **How:** Add the value of the option to delay until market or technology improves, expand if demand is strong, or abandon if cash flows disappoint. A negative static NPV can still be worthwhile if the embedded flexibility has positive value.
- **Risk measurement and adjustment**
  - **When to use:** Use when forecast FCFs are uncertain or the project is unlike the firm's normal operations.
  - **How:** Distinguish project-standing-alone risk, contribution-to-firm risk, and systematic risk. CAPM emphasizes systematic risk, but undiversified owners and bankruptcy costs make contribution-to-firm risk relevant too. A risk-adjusted discount rate `k*` produces:
    `Risk-adjusted NPV = Sum[t=1..n] FCF_t / (1 + k*)^t - IO`
    Increase `k*` for above-normal risk and accept only if the adjusted NPV is nonnegative.
- **Simulation, scenario analysis, and sensitivity analysis**
  - **When to use:** Use when one expected NPV hides a wide range of possible outcomes.
  - **How:** Assign distributions to inputs such as market size, price, growth, market share, investment, salvage, costs, fixed costs, and useful life. Randomly draw a complete set, calculate NPV or IRR, repeat until a distribution of outcomes emerges. Scenario analysis emphasizes worst, most likely, and best cases; sensitivity analysis changes one input while holding the others constant.

## Key Concepts
- **Incremental cash flow:** A cash flow that occurs with the project but not without it.
- **Cannibalization:** New-project sales diverted from the firm's existing products; only the firm's net incremental sales count.
- **Synergistic effect:** Additional cash flow generated elsewhere in the firm because the project attracts customers or enables complementary sales.
- **Sunk cost:** A past cash flow unaffected by the current accept/reject decision; it is excluded.
- **Opportunity cost:** The cash flow forgone when project resources cannot be used for their next-best alternative.
- **Initial outlay:** Immediate after-tax cash required to put the asset into operation, including working capital and replacement effects.
- **Operating cash flow:** `Delta EBIT - Delta taxes + Delta depreciation`.
- **Terminal cash flow:** Final-year operating FCF plus after-tax salvage and recovered working capital, less termination costs.
- **Real option:** Value created by the ability to change a project after uncertainty is resolved.
- **Pure play method:** Estimates project beta from a publicly traded firm engaged solely in the same business, with capital-structure adjustments when needed.

## Mental Models
- **Principle 1: Cash Flow Is What Matters.** Ask "What cash changes because of this decision?" rather than "What accounting profit is reported?"
- **With-versus-without is the control experiment.** Every candidate inflow or outflow must survive the counterfactual: would it happen if the project were rejected?
- **Cash-flow timing is a tax strategy.** Accelerated depreciation does not increase total depreciation; it moves tax savings toward earlier, more valuable dates.
- **Options create asymmetric flexibility.** The firm can keep an upside opportunity when conditions improve and limit downside by abandoning or delaying; static NPV treats the project as if no such choices exist.

## Anti-patterns
- **Counting total project sales as incremental:** Include only sales captured from competitors or preserved for the firm; subtract cannibalized sales.
- **Including sunk research or test-marketing costs:** A cost already paid cannot change with today's decision.
- **Ignoring opportunity costs or assigning all overhead automatically:** Use the cash flow sacrificed or newly caused by the project, not arbitrary allocations.
- **Subtracting interest from project FCF:** Financing costs are already reflected in the discount rate and would be counted twice.
- **Treating depreciation as a cash expense or ignoring its tax effect:** Add back the noncash charge while retaining the tax shield.
- **Using a single expected NPV as certainty:** Inspect distributions, downside cases, and input sensitivity before accepting a risky project.

## Worked Example
Press-on Abs is expected to sell `100,000` units per year for four years at `$6` each, with variable cost `$3` per unit and fixed costs `$90,000`. Equipment costs `$200,000`, receives bonus depreciation in year 1, requires `$30,000` initial NWC, and the tax rate is `21%`.

- Initial outlay: `-$200,000 - $30,000 = -$230,000`.
- Year 1: sales `$600,000` less costs `$390,000` and depreciation `$200,000` gives EBIT `$10,000`; taxes are `$2,100`. Thus `OCF = $10,000 - $2,100 + $200,000 = $207,900`.
- Years 2-3: EBIT is `$210,000`, taxes `$44,100`, and there is no remaining depreciation, so each year's FCF is `$165,900`.
- Year 4: operating FCF is `$165,900`, and liquidation of `$30,000` NWC adds back cash, giving terminal FCF `$195,900`.

The project cash-flow stream is therefore `t0 -$230,000; t1 $207,900; t2 $165,900; t3 $165,900; t4 $195,900`. The example shows why initial working capital, depreciation timing, and recovery of working capital belong in FCF even though they are not ordinary income-statement expenses.

## Key Takeaways
1. Use incremental after-tax FCF, not total sales, net income, or allocated accounting costs.
2. Build the analysis in three parts: initial outlay, annual FCFs, and terminal FCF.
3. Include working-capital investment as an outflow and recover it when the project ends.
4. Add depreciation back but keep the tax savings; never subtract interest from project FCF.
5. Consider delay, expansion, and abandonment options before rejecting a project on static NPV alone.
6. Match risk treatment to the project's contribution to the firm and to diversified shareholders; use simulation or sensitivity analysis to expose forecast fragility.

## Connects To
- **Chapter 10:** These FCFs are the inputs to NPV, PI, IRR, MIRR, payback, and mutually exclusive project comparisons.
- **Appendix 11A:** MACRS supplies tax depreciation percentages when bonus depreciation is unavailable or not used.
- **Chapter 12:** The cost of capital supplies the discount rate and reflects the financing mix and project risk.
- **Chapter 13:** Retained earnings and distributions affect the funds available for future positive-NPV projects.

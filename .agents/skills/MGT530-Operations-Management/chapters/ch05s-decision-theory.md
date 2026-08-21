# Supplement to Chapter 5: Decision Theory

## Core Idea
Decision theory gives an operations manager a structured way to choose among alternatives when future conditions affect results. A decision problem has three building blocks: possible future conditions (states of nature), alternatives under the manager's control, and a payoff for each alternative-state combination. The method is not a promise of certainty; it makes assumptions, tradeoffs, and the value of information visible.

## Frameworks Introduced
- **Seven-step decision process**: (1) identify the problem, (2) specify objectives and solution criteria, (3) develop suitable alternatives, (4) analyze and compare them, (5) select the best alternative, (6) implement it, and (7) monitor results. A payoff analysis supports the middle steps; monitoring tests whether the decision worked.
- **Payoff-table analysis**: List alternatives as rows and states of nature as columns. Populate each cell with the expected payoff, often a present value so income and costs are comparable. Include "do nothing" when it is a real alternative.
- **Environment-matched criteria**: Under certainty, choose the highest payoff for the known state (or lowest cost). Under risk, use probabilities and expected monetary value (EMV). Under uncertainty, when probabilities cannot be assessed reliably, use maximin, maximax, Laplace, or minimax regret.
- **Expected monetary value**: For alternative `i`, `EMV_i = sum[p_j V_ij]`, where `p_j` is the probability of state `j`, `V_ij` is its payoff, and `sum p_j = 1`. Maximize EMV for profits; minimize expected value for costs. EMV is most defensible for a risk-neutral decision maker or a portfolio of many similar decisions.
- **Decision trees**: Draw square nodes for decisions and circular nodes for chance events. Read the tree left to right to show sequence, then evaluate right to left: retain the best later decision at each square and the highest EMV (or lowest expected cost) at each chance node.
- **Expected value of perfect information (EVPI)**: Measure the maximum rational price for knowing the state of nature before choosing. For profits, `EVPI = expected payoff under certainty - best EMV under risk`; equivalently, EVPI is the minimum expected regret.
- **Sensitivity analysis**: Vary an estimated probability or payoff to find when the preferred alternative changes. With two states and `p = P(state 2)`, plot or calculate `EV_i(p) = V_i1 + (V_i2 - V_i1)p`; intersections mark indifference points and optimal ranges.

## Key Concepts
- **Certainty** means relevant parameters such as demand, capacity, and cost are known. **Risk** means states have probabilistic outcomes. **Uncertainty** means the likelihood of states cannot be assessed.
- **Bounded rationality** limits optimization through time, cost, human abilities, technology, and available information; a satisfactory solution may be the practical goal.
- **Suboptimization** occurs when departments optimize their own outcomes at the expense of the organization.
- **Maximin** selects the alternative with the best worst payoff: a conservative guarantee. **Maximax** selects the alternative with the best possible payoff: an optimistic strategy. **Laplace** assigns equal likelihood to states and selects the highest average payoff.
- **Regret**, or opportunity loss, is the gap between an alternative's payoff and the best payoff available in the state that actually occurs. For profits, `R_ij = max(V_j) - V_ij`; for costs, subtract the lowest column cost from each cost. **Minimax regret** chooses the alternative with the smallest worst regret.
- Perfect information is valuable only up to EVPI. A research study, test, or option to delay is worthwhile when its cost is below the expected gain from resolving uncertainty.

## Mental Models
- **Separate control from circumstance**: choose the alternative; treat the state of nature as the uncontrollable condition that follows.
- **Worst, best, average, regret**: maximin protects the downside, maximax pursues upside, Laplace spreads attention across states, and minimax regret limits future "I should have" losses. The criteria encode different attitudes toward uncertainty rather than one universally correct answer.
- **Backward induction**: In a sequential problem, solve the last decision first. A later choice can change the value of an initial alternative, so do not evaluate the first branch before resolving its downstream options.
- **Sensitivity before precision**: Since payoffs and probabilities are estimates, identify the breakpoints and ask whether the recommendation survives plausible changes.

## Anti-patterns
- Treating uncertainty as risk by inventing precise probabilities that have no credible basis.
- Applying maximin, maximax, or Laplace while claiming the criterion is an objective optimum rather than a chosen decision rule.
- Using EMV for a single high-stakes decision without considering risk attitude, downside exposure, or whether repeated decisions will average out.
- Building a regret table from row comparisons; regret is calculated down each state column against that column's best result.
- Reading a decision tree only from left to right and ignoring later choices or chance-node probabilities.
- Reporting a preferred alternative without testing probability and payoff estimates for sensitivity.
- Allowing ego, quick-decision habits, failure to admit error, or departmental goals to replace analysis; bounded rationality should lead to explicit judgment, not hidden assumptions.

## Worked Example
Consider the capacity payoff table below, with amounts in millions of dollars:

| Alternative | Low demand | Moderate demand | High demand |
|---|---:|---:|---:|
| Small facility | 10 | 10 | 10 |
| Medium facility | 7 | 12 | 12 |
| Large facility | -4 | 2 | 16 |

If the state is certain, choose small for low demand, medium for moderate demand, and large for high demand. With no reliable probabilities, the criteria produce different defensible choices: maximin compares worst payoffs `(10, 7, -4)` and chooses small; maximax compares best payoffs `(10, 12, 16)` and chooses large; Laplace averages `(10.00, 10.33, 4.67)` and chooses medium. The regret table is `(0,2,6)`, `(3,0,4)`, and `(14,10,0)` by row. Its worst regrets are `6, 4, 14`, so minimax regret also chooses medium.

Suppose probabilities are low `.30`, moderate `.50`, and high `.20`. Then `EMV_small = .30(10)+.50(10)+.20(10) = 10`; `EMV_medium = .30(7)+.50(12)+.20(12) = 10.5`; and `EMV_large = .30(-4)+.50(2)+.20(16) = 3`. Risk-neutral selection is therefore the medium facility. The expected payoff with perfect information is `.30(10)+.50(12)+.20(16) = 12.2`, so `EVPI = 12.2 - 10.5 = 1.7` million. That is the upper limit for buying perfect information.

For a sequential tree, imagine choosing a small or large arcade. A small facility yields 40 under low demand (`p=.4`); under high demand (`p=.6`), the later choice is expansion at 55 rather than doing nothing at 40 or overtime at 50. Its value is `.4(40)+.6(55)=49`. A large facility leads to reducing prices at 50 under low demand rather than doing nothing at -10, and yields 70 under high demand: `.4(50)+.6(70)=62`. Backward evaluation therefore selects the large initial facility.

## Key Takeaways
1. Define the problem, objectives, alternatives, states, payoffs, and probabilities before calculating.
2. Match the criterion to the decision environment and the manager's risk posture.
3. Use EMV for probabilistic decisions, but interpret it as an average rather than a guaranteed payoff.
4. Use trees for sequential choices, EVPI to value information, and sensitivity analysis to expose fragile recommendations.
5. Treat implementation and monitoring as part of decision quality; a mathematically attractive choice still requires organizational follow-through.

## Connects To
- **Capacity planning**: facility size is the central payoff-table and decision-tree application.
- **Location, equipment, and product/service design**: compare alternatives against demand, competition, permits, or other states of nature.
- **Forecasting and market research**: information can convert uncertainty into risk or certainty; EVPI sets a spending ceiling.
- **Operations control and learning**: monitoring actual outcomes against estimated payoffs improves later probabilities, alternatives, and decisions.

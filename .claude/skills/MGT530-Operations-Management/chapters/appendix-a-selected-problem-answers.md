# Appendix A: Selected Problem Answers

## Core Idea
Use the answer section as a checksum, not as a worked solution. First classify the problem, state the assumptions, and show the governing equation or decision rule. Then compare the direction, units, magnitude, and rounding of your result with the reference. A mismatch is a prompt to audit the model, not merely to copy a number. The selected problems span Chapters 2-19 and are especially useful for checking setup, sequencing, probability, capacity, and sensitivity logic.

## Frameworks/Reference Rules
- **Chapters 2-3:** Compute productivity as `output/input` and percentage change as `(new-old)/old`; use moving/weighted averages, exponential smoothing, trend regression, and seasonal forecasts. Check `e=A-F`, `MAD`, `MSE`, `MAPE`, and `tracking signal = RSFE/MAD` against the correct periods.
- **Chapter 4:** Model reliability with `R_series = product(R_i)`, `R_parallel = 1 - product(1-R_i)`, and time-to-failure probabilities. Keep reliability, failure probability, and time units distinct.
- **Chapters 5-6:** Apply `utilization = actual/design` and `efficiency = actual/effective`, capacity break-even/make-or-buy, `EMV = sum(p_i V_i)`, EVPI, and decision criteria. For line balancing, use `cycle time = available time/demand` and round required stations upward.
- **Chapter 7:** Convert observed time to normal time with performance rating, then standard time with allowances; determine observation sample size. For learning curves, use `Y = aX^b` consistently with the cumulative-average or unit-time convention.
- **Chapter 8:** Compare locations with factor ratings, load-distance or cost-volume logic, and threshold quantities. Preserve the same weights, distance basis, and demand volume for every alternative.
- **Chapters 9-10:** Organize quality data with basic quality tools; construct p, x-bar, and R charts; apply run/randomness tests; and assess capability with Cp/Cpk and specification limits.
- **Chapters 11-13:** Cost aggregate plans and master schedules; for MRP, use `projected on hand = prior on hand + receipts - gross requirements`, net requirements, lot sizes, and lead-time offsets. Explode the bill of materials before calculating lower-level demand.
- **Chapters 14-15:** Size kanban/container requirements from demand during lead time, safety factor, and container size; reason about setup and flow reduction, compare maintenance alternatives by expected cost, and select transportation by total cost and service/lead-time requirements.
- **Chapters 16-19:** Sequence jobs with FCFS, SPT, EDD, CR, and flow-shop rules; use CPM/PERT forward-backward passes, `PERT mean = (a+4m+b)/6`, variance `=((b-a)/6)^2`, and crashing. For queues check `rho = lambda/(s mu)` and `L = lambda W`; for LP formulate the objective and constraints, then inspect slack/surplus, binding resources, shadow prices, and allowable ranges.

## Key Concepts
The answer key represents recurring families rather than isolated arithmetic: ratios and percentage changes; time-series forecasts and error control; probability and reliability networks; capacity and decision trees; line balancing and learning; location thresholds; statistical control and capability; aggregate/MRP tables; inventory and reorder-point logic; lean replenishment; dispatching; critical paths and crash tradeoffs; queue performance; and LP corner-point/sensitivity analysis. The same discipline recurs: define the unit of analysis, identify the limiting resource or event, and distinguish a physical constraint from a managerial preference.

## Mental Models
- **Translate before calculating:** words become variables, precedence, demand timing, or probability states.
- **Trace the flow:** material, work, information, or customers must move in the correct period and sequence.
- **Find the constraint:** the bottleneck, critical path, binding LP constraint, utilization limit, or queue capacity governs the result.
- **Triangulate:** verify with a second view such as units, a rough bound, a balance check, or an alternative decision criterion.

## Anti-patterns
- Treating a reference number as proof when the model, units, or assumptions are wrong.
- Mixing design capacity with effective capacity, actual output with demand, or average time with standard time.
- Using a series reliability formula for parallel components, or confusing control limits with specification limits.
- Ignoring lead-time offsets, scheduled receipts, beginning inventory, lot-size multiples, or safety stock.
- Rounding before the final step; reversing forecast-error signs; or choosing a queue formula when utilization is at or above one.
- Reporting an LP optimum without checking feasibility, slack, binding constraints, or sensitivity ranges.

## Worked Example (one compact verification workflow)
For a periodic-demand inventory check, write the assumptions first: demand rate `d`, lead time `L`, demand standard deviation during lead time `sigma_L`, and service factor `z`. Calculate cycle stock independently with `EOQ = sqrt(2DS/H)`, then calculate `ROP = dL + z*sigma_L`. Audit: (1) convert all demand and time units to the same period; (2) confirm safety stock is not counted twice; (3) verify `ROP` exceeds expected lead-time demand when service protection is intended; (4) compare annual ordering plus holding cost against nearby order quantities; and (5) round only where the operating rule requires whole units. Only after these checks should the reference answer be used to locate a discrepancy.

## Key Takeaways
Attempt every selected problem without looking ahead. Label the problem family, write the rule, calculate with units, and perform a boundary or reasonableness check. Use the appendix to diagnose the step that differs, then redo the problem from the assumptions. Correct method plus transparent checks matters more than matching a rounded endpoint.

## Connects To
This appendix is the cross-chapter audit layer for operations management. Productivity links to capacity and strategy; forecasting feeds aggregate planning, MRP, inventory, and scheduling; reliability and quality inform maintenance and service capacity; lean and supply chain decisions change flow and queues; and CPM, queuing, and LP expose the constraints behind cost, throughput, and customer performance.

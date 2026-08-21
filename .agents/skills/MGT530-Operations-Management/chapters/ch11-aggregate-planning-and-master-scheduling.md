# Chapter 11: Aggregate Planning and Master Scheduling

## Core Idea
Aggregate planning is intermediate-range capacity planning, normally covering 2-12 months and sometimes extending to 18 months. It works with product or service families because family-level forecasts are more reliable and preserve flexibility. The planner seeks a feasible, low-cost balance between expected demand and available capacity.

The plan sets broad levels of output, employment, finished-goods inventory, subcontracting, and backorders. It connects the business plan to execution: business plan -> aggregate plan -> master production schedule (MPS) -> detailed plans. It is commonly treated as sales and operations planning (S&OP), integrating sales forecasts, financial limits, operating capacity, and supply-chain capabilities. Plans are revised on a rolling basis.

## Frameworks Introduced
- **Aggregate-plan inputs, decisions, outputs:** Inputs include resources, forecasts, workforce policies, capacity limits, inventory/backlog positions, and costs. Decisions determine regular-time output, overtime, subcontracting, hiring/layoffs, inventory, and backorders. Outputs include total cost and projected operating levels.
- **Option taxonomy:** Demand strategies alter demand (pricing, promotion, delayed fulfillment, or complementary/new demand); capacity strategies alter supply (workforce, hours, inventory, or outside capacity); mixed strategies use both.
- **Three basic plans:** A level plan holds workforce or output steady and uses inventory, overtime, temporary labor, subcontracting, or backorders as buffers. A chase plan adjusts capacity so output follows expected demand. A mixed plan combines the levers.
- **Planning-technique ladder:** Graphs and spreadsheets support trial-and-error comparisons; linear programming (LP) searches for a cost-minimizing allocation; simulation tests plans under alternative conditions.
- **Disaggregation and control:** The aggregate plan is decomposed into specific end items and timing in an MPS. The tentative MPS is checked by rough-cut capacity planning (RCCP), then used to drive detailed short-range planning and MRP.

## Key Concepts
- Aggregate planning exists because hiring, training, supplier commitments, and capacity changes take time, while item-level demand is uncertain. It must consider total demand and uneven demand within periods.
- Demand choices have costs and risks. Price changes work best when demand is elastic. Promotion can shift demand but may intensify the wrong period. Backorders defer fulfillment but risk lost sales and weaker service. Complementary products can consume idle capacity.
- Supply choices trade flexibility against disruption. Hiring and layoffs incur recruiting, training, severance, morale, union, and skill-availability costs. Overtime is quick and preserves a skilled core workforce, but can reduce productivity and quality. Part-time labor is flexible where skills and agreements permit. Inventory transfers output across periods but incurs carrying, space, capital, and obsolescence costs. Subcontracting adds capacity but reduces control and may create quality and cost risks.
- Chase minimizes inventory and works best when capacity changes are inexpensive and holding costs are high. Level stabilizes people and output but may create inventory, overtime, idle-time, backlog, and service costs. Policy, labor agreements, customer service, perishability, and supply-chain timing can outweigh nominal unit cost.
- Service planning is harder because demand and capacity are variable, measures are less standardized, unused capacity perishes, and inventory generally cannot be built. Cross-training, part-time staffing, demand shaping, and yield management are important.
- LP minimizes regular labor, overtime, subcontracting, inventory, backlog, and workforce-change costs subject to constraints. In the transportation formulation, production-period capacities are supply rows and demand periods are columns. Moving output forward adds holding cost `h`; satisfying earlier demand later adds backlog cost `b`. A dummy column can balance unused capacity. Limitations include linear-cost assumptions, coarse adjustments, and a usual single objective.

Useful relationships:

```text
Workers_t = Workers_(t-1) + Hires_t - Layoffs_t
Net inventory_t = Net inventory_(t-1) + Production_t - Demand_t
Average inventory_t = (Beginning inventory_t + Ending inventory_t) / 2
Cost_t = Output cost + Hire/layoff cost + h(Average inventory_t) + b(Backlog_t)
```

Positive net inventory represents stock and a negative balance represents backlog. Output cost expands into regular-time, overtime, and subcontracted quantities times their unit costs.

For master scheduling, use `Requirements_t = max(Forecast_t, Committed orders_t)` and:

```text
Projected on-hand_t = Projected on-hand_(t-1) + MPS_t - Requirements_t
```

When projected on-hand would fall below the threshold, add a production lot to the MPS. Available-to-promise (ATP) is the uncommitted remainder: beginning inventory plus the first MPS quantity less booked orders until the next MPS; for later intervals, MPS quantity less booked orders until the next MPS.

## Mental Models
- **Buffer portfolio:** Level plans buffer demand with inventory, backlog, labor hours, or suppliers; chase plans buffer it with capacity changes. Mixed plans diversify the risk.
- **Granularity ladder:** Plan economically at the family level, then descend to product and time detail when forecasts and capacity information are stronger.
- **Schedule temperature:** Frozen periods are near-term and nearly fixed; slushy periods allow controlled trade-offs; liquid periods are flexible and tentative. The farther out the order, the cheaper a change usually is.
- **ATP is promiseable slack:** ATP is not all projected inventory. It is the amount remaining after committed orders are reserved, so marketing can promise new orders realistically.

## Anti-patterns
- Locking in SKU quantities too early or treating one annual forecast as certainty.
- Counting duplicate bookings as real demand and then interpreting cancellations as lost demand, which can produce excess capacity.
- Choosing the cheapest production source while ignoring inventory, backlog, transition, quality, morale, or customer-service costs.
- Treating an MPS as feasible without RCCP across facilities, labor, warehouses, and suppliers.
- Changing frozen-period schedules casually or quoting ATP without updating committed orders and MPS lots.

## Worked Example
For a six-period skateboard family, demand is `200, 200, 300, 400, 500, 200` units. A level plan produces 300 units each period, starts and ends with zero inventory, and permits backlog. The signed balance changes by `+100, +100, 0, -100, -200, +100`, so early stock absorbs slack and final output clears the shortage. With regular production at $20 per unit, $1 average-inventory cost, and $5 backlog cost, the chapter's period calculation gives total cost of $37,100. A lower regular rate with strategically placed overtime can reduce backlog without building unnecessary early inventory.

For the MPS, suppose beginning inventory is 64 pumps, weekly forecasts are 30 for four June weeks and 40 for four July weeks, committed orders are 33, 20, 10, 4, and 2, and the lot size is 70. Requirements use the larger of forecast and committed orders, yielding projected on-hand values of 31, 1, and -29 in the first three weeks. The negative third-week balance triggers a 70-unit lot; the same rule adds later lots. The MPS is then capacity-checked, and ATP is calculated at the first period and periods where a lot enters, using booked orders in the look-ahead window.

## Key Takeaways
- Aggregate planning balances demand, capacity, cost, policy, and service over a rolling intermediate horizon.
- Level, chase, and mixed plans differ primarily in which resource absorbs variation.
- Spreadsheets are practical; LP is systematic but assumption-bound; simulation explores uncertainty.
- Disaggregation converts family totals into specific products, timing, labor, materials, and inventory requirements.
- MPS inputs are beginning inventory, forecast, and committed orders; outputs include projected on-hand inventory, planned lots, and ATP.
- RCCP and time fences protect the feasibility and stability of promised schedules.

## Connects To
- Long-range capacity and facility decisions set the limits for aggregate plans.
- Inventory and lot-sizing decisions determine holding costs and MPS lot sizes.
- Marketing uses pricing, promotion, order promises, and ATP; finance uses plan costs; HR governs workforce policies.
- Supply-chain partners use plan quantities and timing to coordinate materials and outside capacity.
- The MPS feeds material requirements planning and detailed scheduling.

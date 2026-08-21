# Chapter 12: Inventory Management

## Core Idea
Inventory is stock held for present or future use. The manager's central trade-off is to provide satisfactory customer service without tying up excessive capital in carrying costs. Every policy answers two questions: **how much should be ordered** and **when should replenishment occur**. Good decisions require accurate records, demand and lead-time information, realistic cost estimates, and differentiated control rather than intuition alone.

## Frameworks Introduced
- **Inventory control:** Periodic review counts at set intervals; perpetual review tracks withdrawals and triggers a fixed quantity at a reorder point. Two-bin systems are simple perpetual signals. Bar codes, POS, SKUs, RFID, and cycle counting improve visibility and record accuracy.
- **A-B-C analysis:** Rank items by annual dollar value (unit cost x annual usage) and concentrate control on high-value A items. B items receive moderate control; C items can use two-bin storage or bulk orders. Adjust classifications for obsolescence, stockout consequences, or supplier distance.
- **Model choice:** EOQ/EPQ and quantity discounts set order or run size; ROP sets timing; fixed-order-interval (FOI) sets order size when review timing is fixed; single-period/newsvendor logic sets one-period stock for limited-life items.

## Key Concepts
**Types and functions.** Inventory includes raw materials and purchased parts, work-in-process, finished goods or merchandise, tools and supplies, MRO items, and pipeline goods in transit. It meets anticipated or seasonal demand, smooths production, decouples operations, protects against stockouts, enables economic lots, hedges price increases, permits production and distribution, and captures quantity discounts. Little's Law is `average inventory = average demand rate x average time in system`.

**Relevant costs.** Purchase cost includes shipping. Holding cost includes capital, insurance, taxes, space, labor, tracking, deterioration, obsolescence, spoilage, breakage, and pilferage. Ordering cost covers placing and receiving an order; setup cost is its production analogue. Shortage cost includes lost contribution, backorders, goodwill, late charges, downtime, or lost production. Seek the best service-cost balance, not minimum inventory.

**ABC and cycle counting.** Compute annual dollar value, rank descending, and assign roughly the top 10-15% of items as A, the middle as B, and the largest low-value group as C. Count A items most frequently and control withdrawals tightly. Typical accuracy targets are +/-0.2% for A, +/-1% for B, and +/-5% for C. Trigger counts after an apparent stockout, anomalous balance, or defined activity; investigate theft, receiving, and recordkeeping causes.

**Basic EOQ.** Assume one product, known annual demand, constant usage and lead time, single-delivery receipts, and no quantity discounts. Average cycle stock is `Q/2`; annual carrying cost is `QH/2`; annual ordering cost is `DS/Q`:

`TC = (QH/2) + (DS/Q)`

`EOQ (Q0) = sqrt(2DS/H)`

`orders/year = D/Q`; `cycle length = Q/D`.

At EOQ, carrying and ordering costs are equal. Because D, S, and H are estimates and the cost curve is flat near its minimum, round to practical lot sizes. For internal production, use EPQ when units arrive incrementally: `Qp = sqrt[(2DS/H)(p/(p-u))]`, where `p > u`; `Imax = Qp(p-u)/p`, average inventory is `Imax/2`, and setup replaces ordering cost. With price breaks, compare feasible quantities using `TC = QH/2 + DS/Q + PD`, including each price-break minimum and the relevant H.

**Reorder point and service.** With constant demand and lead time, `ROP = d x LT`. With uncertainty:

`ROP = expected lead-time demand + safety stock = dbar x LTbar + z(sigma_LT demand)`.

If only demand varies, `sigma_LT demand = sigma_d x sqrt(LT)`; if only lead time varies, it is `d x sigma_LT`; if both vary independently, it is `sqrt(LTbar x sigma_d^2 + dbar^2 x sigma_LT^2)`. Safety stock is `z x sigma_LT demand`. More variation or a higher target service level requires more safety stock. Cycle service level is the probability demand will not exceed supply during lead time: `service level = 1 - stockout risk`. Annual fill rate instead measures the percentage of total demand filled directly from stock.

**FOI.** Orders are placed every `OI` time units, so protection covers the next interval plus lead time. For variable demand and constant lead time:

`Q = dbar(OI + LT) + z(sigma_d x sqrt(OI + LT)) - A`,

where `A` is on hand at review. FOI needs more safety stock than continuous fixed-quantity review because an order cannot be placed between scheduled reviews.

**Single-period/newsvendor.** Use this for perishables or items whose leftover value falls sharply after one period. Set shortage cost `Cs = revenue - cost` (or lost production) and excess cost `Ce = cost - salvage value`, including disposal:

`SL = Cs/(Cs + Ce)`.

Choose the demand quantile at or above SL. For uniform or normal demand, use the distribution; for empirical or Poisson demand, select the first discrete level whose cumulative probability meets or exceeds SL. Stockout risk is `1 - SL`.

## Mental Models
- **U-shaped cost curve:** Small lots lower average inventory but increase order frequency; large lots do the reverse. EOQ balances the slopes.
- **Time and insurance:** Cycle stock supports normal operations; safety stock insures against uncertainty during the protection interval.
- **Pareto attention:** A few items consume most value, so control effort should follow financial and service consequences.
- **Newsvendor seesaw:** Stock more when shortage cost dominates; stock less when excess cost dominates.

## Anti-patterns
- Replacing demand, lead-time, and cost analysis with intuition.
- Treating every SKU equally or trusting perpetual records without physical verification.
- Taking a quantity discount without checking space, cash, obsolescence, spoilage, and total cost.
- Applying EOQ to a perishable one-period item, or fixed-quantity ROP when review timing is fixed.
- Confusing cycle service level with the annual fill rate.
- Cutting inventory without reducing variability, forecast error, setup time, or disruptions.

## Worked Example
A distributor has `D = 9,600` tires/year, `S = $75/order`, and `H = $16/tire/year`. Thus `Q0 = sqrt(2 x 9,600 x 75 / 16) = 300` tires, `D/Q = 32` orders/year, and a cycle of `Q/D x 288 = 9` workdays. Annual carrying plus ordering cost is `(300/2)(16) + (9,600/300)(75) = $4,800`, with equal components.

If lead-time demand averages 50 with standard deviation 5 and stockout risk is 3%, `z = 1.88`: safety stock is `1.88 x 5 = 9.4`, so `ROP = 50 + 9.4`, rounded up to about 60. EOQ sets quantity; ROP sets the trigger. For one-period demand with `Cs = $2.40`, `Ce = $0.80`, and uniform demand from 300 to 500, `SL = .75` and stock is `300 + .75(200) = 450` units.

## Key Takeaways
- Match the model to the facts: EOQ for stable carryover, ROP for timing under variability, FOI for scheduled review, and single-period logic for limited life.
- Separate cycle stock from safety stock and make service level an explicit cost-risk choice.
- Use ABC, cycle counting, and technology to make records reliable and control proportional.
- Prefer variation reduction, shorter lead times, lean flow, supplier coordination, and lower setup or transaction costs to simply adding inventory.

## Connects To
Inventory decisions connect forecasting with purchasing and production, finance with working-capital returns, and service promises with stockout risk. Supplier coordination, vendor-managed or blanket orders, cross-docking, and point-of-use replenishment can lower lead time and handling. Lean systems lower buffers by reducing ordering/setup costs and exposing process problems; accurate records make this feasible.

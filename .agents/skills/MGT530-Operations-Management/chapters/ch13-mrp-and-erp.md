# Chapter 13: MRP and ERP

## Core Idea

Material requirements planning (MRP) converts a master production schedule (MPS) for finished goods into a time-phased plan for every dependent-demand assembly, part, and raw material. It answers three operational questions: what is needed, how much is needed, and when is it needed? The logic is powerful because component demand is derived from the end-item plan rather than forecast independently. It is also fragile: inaccurate product structures, inventory balances, receipts, or lead times produce precise-looking but unusable plans.

Enterprise resource planning (ERP) extends this integration beyond materials and manufacturing. It links functions such as finance, purchasing, production, inventory, distribution, sales, human resources, and customer or supplier management through shared data and workflows.

## Frameworks Introduced

- **MRP input-processing-output framework:** MPS + bill of materials (BOM) + inventory records -> level-by-level explosion, netting, and lead-time offsetting -> planned orders, releases, changes, and exception/performance/planning reports.
- **Product-structure explosion:** A BOM/product structure tree states the quantity of each child needed for one parent. Requirements are calculated from the top level downward; low-level coding groups repeated components at their lowest occurrence.
- **Gross-to-net MRP record:** For each item and time bucket, track gross requirements, scheduled receipts, projected on hand, net requirements, planned-order receipts, and planned-order releases.
- **Closed-loop resource planning:** MPS -> MRP -> capacity requirements planning (CRP) -> revise or approve the schedule; repeat until materials and capacity are feasible.
- **MRP II and ERP escalation:** MRP II adds capacity, finance, marketing, and cross-functional planning; ERP adds an enterprise-wide database, transactional modules, and supply-chain visibility.

## Key Concepts

- **Inputs:** The MPS specifies end items, quantities, and completion periods. The BOM specifies all components and usage quantities. Inventory records provide on-hand balances, open/scheduled receipts, suppliers, lot-size rules, lead times, withdrawals, cancellations, and status by time bucket.
- **Gross requirements** are demand before considering inventory. For a component, they come from the planned-order releases of its immediate parent. **Net requirements** are the amount still needed after projected on hand and scheduled receipts are considered.
- **Planned-order receipts** show when a newly planned order must arrive. **Planned-order releases** show when it must be started or placed: receipt date minus lead time. Releases at one level create gross requirements at the next lower level.
- **Projected on hand** rolls the prior ending balance forward, adds scheduled and planned receipts, and subtracts gross demand. Negative calculated requirements are treated as zero.
- **Lot sizing** determines the planned receipt quantity: lot-for-lot minimizes carryover but may create many setups; fixed multiples exploit ordering or setup economies; fixed-period coverage, EOQ, and more sophisticated dynamic models are alternatives. Lumpy dependent demand makes a single economic lot size unreliable.
- **Safety time** (releasing or receiving early) often handles lead-time variation better than safety stock. Safety stock may be justified for end items, bottlenecks, variable scrap, unreliable supply, or selected components, but blanket lower-level buffers undermine MRP's purpose.
- MRP is a rolling, living plan. Regenerative systems periodically recalculate everything; net-change systems propagate only changes as they occur. Pegging works backward from a component requirement to the parent products affected.
- CRP converts planned releases into work-center loads using routings and labor/machine standards. Time fences stabilize the near-term MPS and limit disruptive changes. Distribution resource planning (DRP) applies the same time-phased netting logic across warehouses, factories, retailers, and suppliers.
- ERP benefits include a shared version of financial and operational truth, real-time visibility, automated handoffs, better order fulfillment, process standardization, supply-chain coordination, and data for improvement. Its risks include process misfit, customization and integration defects, dirty-data conversion, underfunded training, consulting and analysis costs, maintenance/upgrades, loss of key staff, post-go-live disruption, and weak change management. ERP also serves universities, hospitals, banking, retail, logistics, professional services, construction, and real estate.

## Mental Models

- **Tree + timeline + ledger:** The BOM is the tree, lead times place work on the timeline, and each item's MRP record is the inventory ledger that reconciles demand with supply.
- **Pull demand backward:** Start with the required finished-good receipt, multiply down the structure, and offset each requirement backward by its lead time.
- **Garbage in, synchronized garbage out:** MRP's arithmetic can be correct while the plan fails if records do not describe the product or actual operations.
- **Stability is capacity:** A small MPS change near the top of the tree can amplify into large changes below it; fences trade responsiveness for executable plans.
- **ERP is organizational change, not merely software:** A shared database exposes interdependencies and forces common definitions, responsibilities, and processes.

## Anti-patterns

- Control dependent components with independent-demand EOQ/ROP logic while ignoring the MPS and BOM.
- Treat scheduled receipts or planned releases as interchangeable; only the former are already committed.
- Assume constant lead times, perfect yields, or that a load report captures queues and delays.
- Add safety stock everywhere instead of fixing suppliers, bottlenecks, scrap, and records.
- Permit continual MPS changes without fences or freeze periods.
- Implement ERP by automating bad processes, selecting by feature count, excluding end users, underbudgeting data/training/testing, or customizing before proving the standard process.

## Worked Example

Suppose 100 shutters are due at the start of week 4 and 150 at the start of week 8. Each shutter needs two frames and four wood sections. Shutter assembly takes one week; frames have a two-week procurement lead time; wood fabrication takes one week. There are 70 wood sections scheduled to arrive in week 1.

With lot-for-lot ordering, shutter planned receipts are 100 in week 4 and 150 in week 8, so releases are 100 in week 3 and 150 in week 7. Those releases create frame gross requirements of 200 in week 3 and 300 in week 7. Frame releases therefore occur in weeks 1 and 5. Wood gross requirements are 400 in week 3 and 600 in week 7. The week-1 receipt covers 70, leaving 330 net wood sections for week 3; release 330 in week 2. The second requirement leaves 600 net; release 600 in week 6.

If frames must be ordered in lots of 320, receive 320 rather than 200 in week 3, carry 120 forward, and the later net requirement becomes 180; receive another 320, carrying 140. If wood is ordered in multiples of 70, receipts round to 350 and 630, creating additional carryover. Lot sizing therefore meets timing but changes inventory and setup economics.

For CRP, 100 units requiring 2 labor hours and 1.5 machine hours consume 200 labor hours and 150 machine hours. Against 200 hours available for each resource, labor utilization is 100% and machine utilization is 75%. An overload would require rescheduling, overtime, alternate routing, subcontracting, lot splitting, or an MPS revision.

## Key Takeaways

1. MRP is a dependent-demand translation and timing system, not a stand-alone forecast.
2. Accurate MPS, BOM, inventory, receipts, and lead times are prerequisites, not administrative details.
3. Netting determines quantity; lead-time offsets determine release timing; lot sizing determines inventory/setup trade-offs.
4. MRP II closes the loop with capacity and cross-functional resources; ERP connects the resulting processes across the enterprise.
5. Integration creates value only when the organization redesigns processes, governs data, trains users, and manages change.

## Connects To

MRP begins with aggregate planning and the MPS, then connects inventory control, purchasing, scheduling, shop-floor control, and CRP. MRP II links those decisions to finance and marketing. DRP extends the same logic through the supply chain, while ERP provides the shared platform for financials, HR, sales, customer relationships, suppliers, service delivery, and operations strategy.

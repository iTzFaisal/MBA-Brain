# Operations Patterns

## Forecast-Feedback Loop
**When to use**: Demand decisions affect capacity, workforce, inventory, purchasing, or schedules.
**How**: Define purpose and horizon; plot and clean data; select judgmental, time-series, or associative methods; forecast; calculate `e`, MAD/MSE/MAPE; inspect tracking signals and control-chart patterns; revise.
**Trade-offs**: Short horizons and responsive methods adapt faster but can be noisy; stable methods cost less attention but lag real change.

## Voice-of-Customer Design
**When to use**: A new or redesigned product/service must satisfy customers and remain deliverable.
**How**: Use QFD to weight customer "whats," translate them into technical "hows," expose conflicts, and carry requirements into components and processes. Check Kano basics before performance and excitement features; use concurrent engineering and a service blueprint.
**Trade-offs**: Early cross-functional coordination costs time and conflict, but reduces late rework, infeasible specifications, and launch delay.

## Capacity Constraint Gate
**When to use**: Demand, expansion, make-or-buy, or technology choices compete for scarce capacity.
**How**: Convert the product mix to processing hours; compare design/effective/actual capacity; locate the bottleneck; exploit and subordinate work to it; evaluate cushion, timing, alternatives, and cost-volume ranges.
**Trade-offs**: A lead strategy captures growth but risks idle capital; a follow strategy improves utilization but risks lost service; flexibility and cushion cost money.

## Cost-Volume and Make-or-Buy Screen
**When to use**: Alternatives have different fixed costs, variable costs, prices, or supplier terms.
**How**: Compare `TC = FC + vQ` and contribution `Q(R-v)-FC` at realistic volumes. For make-or-buy, add relevant freight, quality, control, risk, stranded fixed cost, knowledge, liability, and flexibility effects.
**Trade-offs**: The arithmetic is transparent but assumes stable, linear costs and a sellable output; qualitative and time-value effects can reverse the ranking.

## Volume-Variety Process Fit
**When to use**: Selecting a process, automation level, or layout.
**How**: Map volume, variety, customization, technology, and change frequency. Use job shop, batch, repetitive, or continuous processing as the profile moves toward high volume/low variety; use project or fixed-position logic for unique immovable work.
**Trade-offs**: Specialized flow lowers unit cost but sacrifices flexibility; general-purpose flexibility handles variety but adds labor, routing, setup, and scheduling cost.

## Line-Balance Assignment
**When to use**: Repetitive work has precedence relationships and a target output rate.
**How**: Compute `cycle time = available time/demand`; calculate `N_min = ceil(total task time/cycle time)`; assign eligible tasks without exceeding cycle time; compare idle time and efficiency; recheck equipment and skill restrictions.
**Trade-offs**: Heuristics produce workable candidates, not guaranteed optima; tighter balance improves flow but can reduce slack for absences and disruptions.

## Method-to-Standard Chain
**When to use**: Setting labor standards, capacity, schedules, incentives, or bids.
**How**: Improve and document the method with operator input; observe repeated work; calculate `OT`, rate to `NT = OT*PR`, then add the correct allowance to get `ST = NT*AF`. Use learning-curve data for new repetitive human work.
**Trade-offs**: Detailed stopwatch studies are precise but disruptive; work sampling is cheaper for varied work but less granular. A faster standard is worthless if unsafe or unattainable.

## Stability-Before-Capability SPC
**When to use**: A process must be controlled and shown capable of meeting specifications.
**How**: Define the characteristic and time order; choose x-bar/R, p, or c charts; investigate special causes and run patterns; only after stability compute `Cp` or `Cpk` against specifications; improve the process rather than screen defects.
**Trade-offs**: Wider limits reduce false alarms but can miss shifts; capability numbers are misleading for unstable or markedly nonnormal processes.

## Aggregate Plan to MPS
**When to use**: Intermediate-range demand must become executable product and timing commitments.
**How**: Compare level, chase, and mixed plans; disaggregate families into the MPS; set requirements as `max(forecast, committed orders)`; roll projected on-hand; add lots before shortage; check with RCCP and protect time fences; calculate ATP from uncommitted supply.
**Trade-offs**: Level plans protect workforce stability but create inventory/backlog; chase reduces inventory but creates hiring, overtime, or subcontracting exposure.

## Inventory Policy Match
**When to use**: Choosing order quantity, review timing, or service protection.
**How**: Use ABC for control intensity; EOQ for stable carryover, `ROP = lead-time demand + safety stock` for continuous review, FOI for fixed review intervals, and newsvendor logic for one-period life. Verify records with cycle counts.
**Trade-offs**: More safety stock raises service but ties up capital; smaller lots reduce cycle stock but increase ordering/setup frequency; the right policy depends on variability and item life.

## MRP Explosion and Capacity Loop
**When to use**: Components have dependent demand from a finished-good plan.
**How**: Validate MPS, BOM, inventory, receipts, lot sizes, and lead times; explode parent releases downward; net supply; offset planned receipts into releases; feed CRP; revise until materials and capacity are feasible.
**Trade-offs**: Lot-for-lot limits carryover but creates setups; fixed multiples reduce transaction cost but create inventory. MRP precision cannot repair dirty records or unstable schedules.

## Lean Pull Reset
**When to use**: WIP, delay, defects, setups, or excess movement obscure flow.
**How**: Define customer value; map the value stream; remove waste; stabilize quality and equipment; use SMED, cells, takt, heijunka, kanban or CONWIP, jidoka, poka-yoke, 5S, TPM, and supplier coordination; lower buffers gradually while solving exposed problems.
**Trade-offs**: Lower WIP improves speed and exposes problems, but premature cuts create fragility. Pull needs reliable processes, trained people, and cooperative suppliers.

## Reliability-Maintenance Mix
**When to use**: Breakdown, downtime, quality, or spare-capacity costs differ by asset.
**How**: Rank criticality; compare breakdown, preventive, predictive, and TPM options; estimate `expected breakdown cost = expected failures x cost/failure`; balance PM against failure cost; improve MTBF and reduce MTTR; compare replacement over the lifecycle.
**Trade-offs**: Too little PM creates uncertain downtime; too much PM consumes labor and production time. Redundancy helps only when alternatives and transfer mechanisms are dependable.

## Total-Cost Supply Sourcing
**When to use**: Selecting suppliers, freight, network structure, or outsourcing.
**How**: Use SCOR to map flows; compare purchase price plus freight, inventory, quality, lead time, disruption, sustainability, disposal, and coordination costs; audit capability; share data; set response plans and reverse logistics.
**Trade-offs**: Centralization and lean sourcing gain scale and lower stock but can increase distance and concentration risk; redundancy and near-sourcing improve resilience but cost more.

## Objective-First Scheduling
**When to use**: Jobs compete for a work center or service resources.
**How**: Decide whether flow time, due dates, fairness, urgency, makespan, or bottleneck throughput matters. Then use SPT, EDD, FCFS, CR, Johnson's rule, or TOC/drum-buffer-rope; use finite loading and monitor Gantt/I/O results.
**Trade-offs**: No priority rule wins every measure; SPT can starve long work, EDD ignores processing time, and FCFS may sacrifice flow efficiency for fairness.

## Project Network and Crash Control
**When to use**: One-time work has dependencies, deadlines, or uncertain activity times.
**How**: Build a WBS and network; run forward/backward passes; identify all critical or near-critical paths; use PERT estimates, simulation when paths share risk, and crash slopes only on reducible critical work; recheck after each change.
**Trade-offs**: Faster completion can justify direct crash cost, but overlapping phases and compression increase coordination, rework, and risk. Buffers protect variation without hiding it.

## Queue Capacity Test
**When to use**: Customers, jobs, machines, or trucks wait for variable service.
**How**: Classify source, channels, phases, discipline, and distributions; verify `rho < 1`; estimate `L`, `W`, and waiting cost for each staffing option; reduce variability and improve perceived fairness/information as well as adding servers.
**Trade-offs**: Near-100% utilization creates disproportionate waiting; pooled lines improve balancing and FCFS, while dedicated lines may support specialization or priority.

## LP Formulation and Sensitivity
**When to use**: Scarce resources must be allocated among divisible competing activities with linear relationships.
**How**: Define variables, objective, constraints, RHS values, and nonnegativity; solve corners, simplex, or Solver; verify feasibility; inspect binding resources, slack/surplus, shadow prices, reduced costs, and allowable ranges.
**Trade-offs**: LP makes trade-offs explicit and scalable, but omitted nonlinearities, integer requirements, uncertain data, or out-of-range sensitivity values require a new or different model.

# Operations Management Cheatsheet

Use this as a reasoning aid. Load the linked chapter before relying on a formula outside its assumptions.

## First Decision

| Situation | First move |
|---|---|
| Future demand is unknown | Forecast, state horizon/error, and keep a response plan. |
| Alternative outcomes depend on states | Use a payoff table; add probabilities only when credible. |
| Current flow is slow | Find the bottleneck or variability source before adding capacity. |
| Defects are recurring | Stabilize special causes, then reduce common-cause variation. |
| Work is one-time | Build a WBS and precedence network, not just a task list. |
| Work is repetitive | Match volume-variety to process/layout, then balance and measure. |

## Default Rules and Formulas

- `productivity = output/input`; include usable output, not scrap.
- Capacity: `efficiency = actual/effective`; `utilization = actual/design`; do not treat design capacity as normal output.
- Cost-volume: `TC = FC + vQ`; `Q_break-even = FC/(R-v)`; reject a break-even point outside its capacity range.
- Inventory: `EOQ = sqrt(2DS/H)` sets quantity; `ROP = expected lead-time demand + z*sigma` sets timing. EOQ does not solve a one-period perishability problem.
- Reliability: required series components multiply; alternative independent paths use `1 - product(1-R)`; `availability = MTBF/(MTBF+MTTR)`.
- Quality: stabilize before `Cp/Cpk`; use x-bar/R for measured data, p for defective units, c for defect counts. Control limits are not specifications.
- Projects: `te = (to + 4tm + tp)/6`; variance `=((tp-to)/6)^2`; crash only reducible critical work and recheck the network.
- Queues: keep `rho = lambda/(servers*mu) < 1`; use `L = lambda W`; compare waiting cost with added capacity cost.

## Trade-off Rules

- **Level vs chase**: level protects workforce stability but uses inventory, overtime, or backlog; chase follows demand but changes capacity.
- **Flow vs flexibility**: product layouts and specialized equipment lower unit cost; process layouts and general-purpose equipment absorb variety.
- **Lean vs resilience**: lower buffers improve flow and expose problems; remove causes before removing protection.
- **Central vs local supply**: centralization gains scale; local or redundant sources improve response and disruption tolerance.
- **SPT vs EDD vs FCFS**: SPT favors average flow, EDD due dates, FCFS fairness. Choose the objective first.

## Tells and Smells

- High efficiency with low utilization: effective capacity is the lid; investigate maintenance, quality, scheduling, or training.
- A process is in control but fails specifications: stable does not mean capable; center it or reduce variation.
- Inventory is high and problems are invisible: lower it gradually after fixing defects, setups, suppliers, or bottlenecks.
- A supplier is cheapest per unit: recalculate total cost including freight, lead time, quality, risk, inventory, and ethics.
- An MPS creates negative projected on-hand: add a feasible lot, then run RCCP; do not promise from an unchecked schedule.
- A queue persists despite adequate average capacity: arrival and service variability may be the cause; 100% utilization is not the target.
- A model gives a precise answer with dirty inputs or omitted constraints: audit assumptions before trusting arithmetic.

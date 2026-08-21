---
name: MGT530-Operations-Management
description: "Knowledge base from William J. Stevenson, Operations Management, Fourteenth Edition, for applying operations-management frameworks."
---

<!-- argument-hint: [topic, framework, or chapter number] -->

# Operations Management
**Author**: William J. Stevenson | **Edition**: Fourteenth Edition | **Pages**: 929 | **Numbered chapters**: 19 | **Chapter supplements**: 4 | **Appendices**: 4 | **Generated**: 2026-08-21

## Core Frameworks

- **Transformation system and whole-system lens.** Use `inputs -> transformation -> outputs`, with measurement, feedback, and control, to locate value, variation, and corrective action. Optimize the supply chain and total system, not a local department's ratio.
- **Mission-to-operations hierarchy.** Translate mission into goals, organization and functional strategies, tactics, and daily operations. Use **order qualifiers** as the market entry ticket and **order winners** as the reason to buy. Choose and align low cost, responsiveness, and differentiation; use the **Balanced Scorecard** to execute and measure the strategy.
- **Variability tax.** First remove assignable causes and avoidable demand, supplier, and process variation. Then choose deliberate buffers: capacity cushion, inventory, time, flexibility, or price. Treat every buffer as a cost paid to absorb uncertainty.
- **Six-step forecasting process.** Define purpose and horizon; prepare data; select judgmental, time-series, or associative methods; forecast; measure error; and revise. Use `e = A - F`, MAD/MSE/MAPE, tracking signals, and control-chart patterns. A shorter decision horizon is usually more accurate; a forecast is not a promise.
- **Design-to-delivery alignment.** Use **Quality Function Deployment (QFD)** to convert customer "whats" into technical "hows"; use the **Kano model** to protect basic requirements before performance and excitement features; use **concurrent engineering**, service blueprinting, life-cycle assessment, and the **Three Rs** before launch. Standardize the platform and customize at the edge when variety matters.
- **Reliability and availability.** Define the success event and operating horizon first. Required independent components use `Rs = product(Ri)`; alternative independent paths use `Rs = 1 - product(1 - Ri)`; steady availability is `A = MTBF/(MTBF + MTTR)`. Include switches, shared causes, repair waiting, and stated conditions.
- **Capacity and constraints.** Use design capacity, effective capacity, and actual output together: `efficiency = actual/effective`, `utilization = actual/design`. Convert product-mix demand into processing time, calculate `TC = FC + vQ` and `Q_break-even = FC/(R-v)`, then apply the **Theory of Constraints** cycle: identify, exploit, subordinate, elevate, repeat. Add cushion when uncertainty justifies it.
- **Decision theory under uncertainty.** Build a payoff table with alternatives as rows and states of nature as columns. Under risk, `EMV_i = sum(p_j V_ij)`; under uncertainty, explicitly choose maximin, maximax, Laplace, or minimax regret. Use decision trees backward, value information with `EVPI`, and test probability/payoff sensitivity before committing.
- **Volume-variety-process fit.** Match project, job shop, batch, repetitive, or continuous process to volume, variety, customization, and flexibility. Match product, process, fixed-position, or cellular layout to flow and movement. For a line, `cycle time = available time/demand` and `N_min = ceil(sum task times/cycle time)`; respect precedence and compare idle time.
- **Work measurement chain.** Improve the method before measuring it, then use `OT -> NT = OT*PR -> ST = NT*AF`. Choose stopwatch study for short repetitive work, predetermined times for fitting elemental data, and work sampling for varied work. Distinguish unit-time from cumulative-average **learning curve** estimates.
- **Quality built into the system.** Use quality at the source, prevention, **TQM**, **DMAIC**, **PDSA**, poka-yoke, and Pareto focus. Stabilize first with SPC, then test capability: use x-bar/R for measured data, p for defective proportions, and c for defect counts. Specifications are customer limits, not control limits; use `Cp` for centered processes and `Cpk` when centering is uncertain.
- **Plan at the right granularity.** Use level, chase, or mixed aggregate plans; disaggregate into the **Master Production Schedule (MPS)**; check it with rough-cut capacity planning; then feed MRP and detailed scheduling. For inventory, use `EOQ = sqrt(2DS/H)` for stable carryover, `ROP = expected lead-time demand + safety stock` for timing, and newsvendor logic for one-period items.
- **MRP, ERP, and lean flow.** MRP performs `MPS + BOM + inventory records -> gross-to-net explosion -> lead-time-offset releases`; close the loop with CRP. Lean applies five principles: value, value stream, flow, pull, and perfection. Lower WIP only as capability improves; use **SMED**, takt, cells, kanban, heijunka, jidoka, poka-yoke, TPM, and supplier cooperation to make pull reliable.
- **Network, schedule, and optimize.** Use **SCOR** (Plan, Source, Make, Deliver, Manage Returns), total-cost sourcing, risk mapping, visibility, and reverse logistics. Choose a scheduling rule after naming the objective: SPT favors flow time, EDD favors due dates, FCFS favors fairness, and CR emphasizes urgency. For projects, use WBS, PERT/CPM, critical paths, buffers, and crash slopes. For queues, keep `rho < 1` and compare waiting cost with capacity cost. For LP, formulate variables, objective, constraints, and nonnegativity, then inspect binding constraints, slack, shadow prices, and sensitivity ranges.

## How to Use This Skill

- **No argument**: load Core Frameworks, then use the indexes to choose the relevant chapter.
- **Topic or framework**: identify the linked chapter and read it before answering; use `glossary.md` for a quick definition and `patterns.md` for an actionable method.
- **Chapter request**: ask for `ch03`, `ch05S`, `appendix C`, or a topic such as `EOQ`, `Cpk`, or `PERT`.
- **Quantitative problem**: classify the problem, write assumptions and units, select the formula/model, calculate, and perform a boundary or reasonableness check. Use the appendix files for probability lookup and answer verification.

## Chapter Index

| Ref | Chapter or supplement | Primary use |
|---|---|---|
| [ch01](chapters/ch01-introduction-to-operations-management.md) | Introduction to Operations Management | transformation, systems, variation, ethics |
| [ch02](chapters/ch02-competitiveness-strategy-and-productivity.md) | Competitiveness, Strategy, and Productivity | strategy, qualifiers/winners, productivity |
| [ch03](chapters/ch03-forecasting.md) | Forecasting | methods, seasonality, error, control |
| [ch04](chapters/ch04-product-and-service-design.md) | Product and Service Design | QFD, Kano, concurrent design, services |
| [ch04S](chapters/ch04s-reliability.md) | Supplement: Reliability | series, parallel, life, availability |
| [ch05](chapters/ch05-strategic-capacity-planning.md) | Strategic Capacity Planning for Products and Services | capacity, bottlenecks, cost-volume |
| [ch05S](chapters/ch05s-decision-theory.md) | Supplement: Decision Theory | payoffs, EMV, EVPI, trees |
| [ch06](chapters/ch06-process-selection-and-facility-layout.md) | Process Selection and Facility Layout | volume-variety, layouts, line balance |
| [ch07](chapters/ch07-work-design-and-measurement.md) | Work Design and Measurement | methods, standards, sampling, ergonomics |
| [ch07S](chapters/ch07s-learning-curves.md) | Supplement: Learning Curves | repetition, unit and cumulative time |
| [ch08](chapters/ch08-location-planning-and-analysis.md) | Location Planning and Analysis | screening, factor rating, network location |
| [ch09](chapters/ch09-management-of-quality.md) | Management of Quality | TQM, Six Sigma, PDSA, quality cost |
| [ch10](chapters/ch10-quality-control.md) | Quality Control | SPC, charts, runs, capability |
| [ch11](chapters/ch11-aggregate-planning-and-master-scheduling.md) | Aggregate Planning and Master Scheduling | level/chase plans, MPS, ATP, RCCP |
| [ch12](chapters/ch12-inventory-management.md) | Inventory Management | ABC, EOQ, ROP, safety stock |
| [ch13](chapters/ch13-mrp-and-erp.md) | MRP and ERP | BOM explosion, netting, CRP, integration |
| [ch14](chapters/ch14-jit-and-lean-operations.md) | JIT and Lean Operations | waste, pull, kanban, SMED, takt |
| [ch14S](chapters/ch14s-maintenance.md) | Supplement: Maintenance | PM, predictive maintenance, TPM |
| [ch15](chapters/ch15-supply-chain-management.md) | Supply Chain Management | SCOR, sourcing, risk, visibility |
| [ch16](chapters/ch16-scheduling.md) | Scheduling | loading, sequencing, TOC, service |
| [ch17](chapters/ch17-project-management.md) | Project Management | WBS, PERT/CPM, risk, crashing |
| [ch18](chapters/ch18-management-of-waiting-lines.md) | Management of Waiting Lines | queues, variability, capacity trade-offs |
| [ch19](chapters/ch19-linear-programming.md) | Linear Programming | formulation, corners, shadow prices |

## Appendix Index

| Appendix | File | Use |
|---|---|---|
| [A](chapters/appendix-a-selected-problem-answers.md) | Selected Problem Answers | cross-chapter verification |
| [B](chapters/appendix-b-reference-tables.md) | Reference Tables | normal and Poisson lookup rules |
| [C](chapters/appendix-c-normal-distribution.md) | Working with the Normal Distribution | standardization and tail areas |
| [D](chapters/appendix-d-ten-things-to-remember.md) | Ten Things to Remember Beyond the Final Exam | final system-level check |

## Topic Index

- **ABC analysis** -> [ch12](chapters/ch12-inventory-management.md)
- **Aggregate planning** -> [ch11](chapters/ch11-aggregate-planning-and-master-scheduling.md)
- **Capacity and bottlenecks** -> [ch05](chapters/ch05-strategic-capacity-planning.md), [ch16](chapters/ch16-scheduling.md)
- **Decision theory** -> [ch05S](chapters/ch05s-decision-theory.md)
- **Forecasting** -> [ch03](chapters/ch03-forecasting.md)
- **Inventory and EOQ/ROP** -> [ch12](chapters/ch12-inventory-management.md)
- **Lean, JIT, and kanban** -> [ch14](chapters/ch14-jit-and-lean-operations.md)
- **Linear programming** -> [ch19](chapters/ch19-linear-programming.md)
- **Location and network design** -> [ch08](chapters/ch08-location-planning-and-analysis.md), [ch15](chapters/ch15-supply-chain-management.md)
- **Maintenance and availability** -> [ch04S](chapters/ch04s-reliability.md), [ch14S](chapters/ch14s-maintenance.md)
- **MRP, ERP, and MPS** -> [ch11](chapters/ch11-aggregate-planning-and-master-scheduling.md), [ch13](chapters/ch13-mrp-and-erp.md)
- **Operations strategy and productivity** -> [ch02](chapters/ch02-competitiveness-strategy-and-productivity.md)
- **PERT, CPM, and projects** -> [ch17](chapters/ch17-project-management.md)
- **Process selection and layouts** -> [ch06](chapters/ch06-process-selection-and-facility-layout.md)
- **Quality, SPC, and capability** -> [ch09](chapters/ch09-management-of-quality.md), [ch10](chapters/ch10-quality-control.md)
- **Queues and waiting lines** -> [ch18](chapters/ch18-management-of-waiting-lines.md)
- **Reliability and robust design** -> [ch04](chapters/ch04-product-and-service-design.md), [ch04S](chapters/ch04s-reliability.md)
- **Scheduling and sequencing** -> [ch16](chapters/ch16-scheduling.md)
- **Service design and blueprinting** -> [ch04](chapters/ch04-product-and-service-design.md)
- **Supply chain, sourcing, and risk** -> [ch01](chapters/ch01-introduction-to-operations-management.md), [ch15](chapters/ch15-supply-chain-management.md)
- **Work design, standards, and learning** -> [ch07](chapters/ch07-work-design-and-measurement.md), [ch07S](chapters/ch07s-learning-curves.md)

## Supporting Files

- [glossary.md](glossary.md) - alphabetized terms with chapter references.
- [patterns.md](patterns.md) - concrete operations techniques and methods.
- [cheatsheet.md](cheatsheet.md) - compact decision rules, formulas, trade-offs, and tells.

## Scope & Limits

This skill extracts and operationalizes the audited chapter files from Stevenson's textbook. It preserves textbook formulas and decision conventions but does not replace the chapter files when assumptions, table constants, or model conditions matter. Numerical recommendations require current data, units, and local context; qualitative, ethical, safety, sustainability, and stakeholder effects must be assessed alongside calculated results. It does not provide implementation-specific legal, regulatory, software, or industry advice beyond the book's scope.

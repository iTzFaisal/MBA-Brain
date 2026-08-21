# Chapter 6: Process Selection and Facility Layout

## Core Idea

Process selection and facility layout are strategic, long-lived choices. Match the process to volume, variety, customization, technology, and supply-chain requirements before investing in equipment or space. Then arrange resources for smooth, safe flow at appropriate cost and capacity.

## Frameworks Introduced

- **Volume-variety process spectrum:** Process choice is demand-driven. Low volume/high variety favors a **job shop**; moderate volume/variety, **batch**; high volume/low variety, **repetitive**; and very high volume/very low variety, **continuous** processing. A **project** handles nonroutine work with a unique objective and limited duration. Volume and variety are usually inverse, while required flexibility rises with variety. Choose near the diagonal; processes can be hybrids or change as a product's volume changes over its life cycle.
- **Product or service profiling:** Link offering range, order size, pricing, schedule-change frequency, and order-winning requirements to process capabilities before committing resources.
- **Process strategy trade-off:** Capital intensity is the equipment-labor mix; process flexibility is the ability to adapt to design, volume, or technology changes. Flexibility fits real variety or uncertainty; specialized equipment is often cheaper and more efficient for mature products with stable volume. Better forecasting can reduce the need to buy flexibility.
- **Technology-management screen:** Evaluate product, process, and information technology together. Test capability, economics, integration, training, safety, labor effects, and strategic fit. Remove process waste before automating so the system does not automate waste.
- **Process-layout fit:** Product layouts suit repetitive/continuous flow; process layouts suit intermittent job-shop/batch flow; fixed-position layouts suit projects. Cellular layouts and flexible manufacturing systems seek product-layout flow with more variety.

## Key Concepts

- **Job shop:** Low-volume, high-variety, intermittent work using general-purpose equipment and skilled labor; flexible but costly and difficult to schedule.
- **Batch process:** Moderate volume and variety, intermittent flow, moderate flexibility, and moderate setup/scheduling complexity.
- **Repetitive process:** High-volume standardized output, usually a production or assembly line; low unit cost but low flexibility and high downtime cost.
- **Continuous process:** Very high-volume, nondiscrete, highly standardized flow with specialized equipment, almost no variety, and costly changeovers.
- **Automation:** Sensing and control devices operate machinery automatically. It reduces variability and variable labor cost, but requires standardization and may demand high volume to justify high capital cost.
- **Automation choices:** Fixed automation is specialized and high-volume/low-variety; programmable automation uses computer-controlled general-purpose equipment for small batches; flexible automation minimizes changeover time while retaining family-level variety. CAM controls manufacturing; N/C and CNC machines follow stored instructions; an FMS links machines, handling, and supervisory control; CIM integrates manufacturing with design, purchasing, planning, inventory, and distribution.
- **Emerging technology:** IoT supports machine learning, quality, productivity, and predictive maintenance. 3D printing builds objects layer by layer for prototypes, replacement parts, small quantities, customization, and on-demand production, though it is slower than conventional high-volume production. Drones support remote inspection and urgent delivery but add failure, safety, and regulatory risks.
- **Product layout:** Standardized tasks and equipment follow product sequence, often with conveyors. It offers high output, low unit and handling cost, high utilization, low work-in-process, and routine control; it is inflexible, interdependent, breakdown-prone, and can create repetitive work. A U-shaped line saves space and improves communication and assignment flexibility.
- **Process layout:** Similar functions are grouped into departments; general-purpose equipment and variable-path handling support varied routes. It is flexible and resilient to individual failures, but has higher work-in-process, handling, routing, scheduling, supervision, and unit costs.
- **Fixed-position and combination layouts:** The product stays stationary while labor, materials, and equipment move when size, weight, bulk, or fragility makes movement impractical. Real systems combine layout types.
- **Cellular layout and group technology:** Group machines into cells for part families with similar processing. SMED reduces changeover time; right-sized mobile equipment eases reconfiguration. Cells reduce moves, delay, space, lead time, and work-in-process, but require family analysis, multiskilled teams, and possible relocation cost.
- **Service layouts:** Classify services by customer contact and customization. High contact/high customization needs a flexible job-shop-like layout; high contact/low customization may use self-service; low contact/low customization can separate the customer from an automated core. Warehouses manage pick frequency/correlation; retail manages traffic; hospitals prioritize safety and access.
- **Line balancing:** Set `cycle time = operating time per day / desired output rate` and `output rate = operating time per day / cycle time`. The theoretical minimum is `N_min = sum of task times / cycle time`, rounded up; feasible cycle time ranges from longest task to total task time. Draw precedence, assign eligible tasks that fit, and use most-following-tasks or greatest-positional-weight heuristics. `Idle% = idle time per cycle / (N_actual x actual cycle time) x 100`; efficiency is `100% - Idle%`.
- **Process-layout design rules:** Specify departments, dimensions, future flows, distances, cost per distance, budget, special closeness/separation, utilities, and access. Use from-to charts and evaluate `flow x distance x unit cost`; place high-flow departments close. Muther ratings prioritize A, then E/I/O/U; separate X pairs. Heuristics yield candidates to compare, not guaranteed optima.

## Mental Models

- **Capability must match demand:** Move along the volume-variety spectrum only when the market and process economics justify it; do not select a technology because it is fashionable.
- **Flow versus flexibility:** Product layouts buy efficient, synchronized flow; process layouts buy routing flexibility. Cellular design is the attempt to capture both, not a guarantee of both.
- **Layout is a flow problem:** Optimize movement of work, information, customers, and materials, not merely visual placement.
- **Technology amplifies the process:** Stabilize and simplify first; automation, IT, and robotics then amplify a sound process or magnify hidden waste.

## Anti-patterns

- **Using a job shop for high-volume standardized work, or continuous processing for low-volume variety:** The system falls far from the volume-variety diagonal and pays through cost, rigidity, or missed capacity.
- **Buying flexibility by default:** Flexible equipment is expensive and often less efficient; use it for demonstrated variety or uncertainty, not as a substitute for forecasting.
- **Automating an unstable process:** Waste, defects, bad layouts, and poor handoffs become harder and more expensive to change.
- **Treating a product line as perfectly balanced or invulnerable:** Breakdowns, absenteeism, task incompatibility, skill constraints, and human time variability require preventive maintenance, repair capacity, slack, and cross-training.
- **Treating a layout heuristic as an optimum:** High-flow adjacency and closeness ratings produce satisfactory candidates; compare alternatives and include safety, utilities, building constraints, modification cost, and qualitative requirements.

## Worked Example

Eight-hour operation, desired output 400 units/day, and tasks:

| Task | Time | Predecessor |
|---|---:|---|
| a | 0.2 | -- |
| b | 0.2 | a |
| c | 0.8 | -- |
| d | 0.6 | c |
| e | 0.3 | b |
| f | 1.0 | d, e |
| g | 0.4 | f |
| h | 0.3 | g |

Available time is 480 minutes. Thus, cycle time is `480 / 400 = 1.2 minutes/unit`; total task time is 3.8 minutes, so `N_min = ceil(3.8 / 1.2) = 4` stations. A precedence-feasible assignment is S1 = a, c, b (1.2); S2 = d, e (0.9); S3 = f (1.0); S4 = g, h (0.7). Total idle time per cycle is 1.0 minute, so balance delay is `1.0 / (4 x 1.2) x 100 = 20.83%` and efficiency is 79.17%. The assignment is practical, not necessarily optimal: tasks must be eligible, fit within cycle time, and respect incompatible equipment or contamination constraints.

## Key Takeaways

1. Start process selection with required volume, variety, flexibility, and product/service profile.
2. Treat process type, technology, capacity, supply chain, and layout as connected decisions.
3. Use product layouts for standardized flow, process layouts for variety, fixed-position layouts for immovable projects, and cells for part-family flow.
4. For line balancing, compute cycle time, round the theoretical station minimum up, respect precedence, and compare heuristic assignments using idle time and efficiency.
5. For process layouts, place high-flow departments close, separate incompatible activities, and verify the result against cost, safety, access, and change requirements.

## Connects To

Capacity planning and product/service design determine the demand profile that drives process choice. Lean process design supplies waste and variance-reduction logic, while supply-chain design, maintenance, work design, and quality management determine whether the selected process and layout can deliver reliable flow.

# Chapter 16: Scheduling

## Core Idea
Scheduling determines when organizational resources are used and in what order work is performed. It is the final operating decision before transformation, so it must work within choices already made about capacity, process, layout, product or service design, aggregate planning, and the master schedule. A good schedule trades off utilization of people, equipment, and facilities against customer waiting, inventories or work in process (WIP), flow time, cost, and on-time delivery. There is no universally best sequence: the right rule depends on the performance objective and the operating context.

## Frameworks Introduced
- **Volume-to-scheduling framework**: High-volume flow systems emphasize smooth rate, line balance, maintenance, reliable supplies, and product mix. Intermediate-volume batch systems decide run size, timing, and sequence while managing setup cost. Low-volume job shops require separate loading and sequencing decisions because jobs vary in route, materials, setup, and processing time.
- **Loading and capacity**: Loading assigns jobs to work centers or machines. Infinite loading ignores capacity and may create overloads; finite loading schedules actual start and stop times without exceeding available capacity. The assignment model, solved by the Hungarian method under one-to-one and known-cost assumptions, matches jobs to resources.
- **Priority-rule sequencing**: FCFS, SPT, EDD, and CR are practical heuristics for a queue at a work center. S/O and rush priorities add downstream or customer urgency information. FCFS, SPT, and EDD are local; CR and S/O are global.
- **Two-work-center flow shop**: Johnson's rule minimizes makespan when every job follows the same two-step route, processing times are known and sequence-independent, and a job must finish at center 1 before center 2 starts it. Put the smallest remaining time first if it is at center 1, last if it is at center 2.
- **Theory of constraints (TOC)**: Identify the bottleneck, exploit it, subordinate other work to it, elevate or eliminate the constraint, and repeat. Drum-buffer-rope schedules the bottleneck's pace, protects it with a small buffer, and synchronizes upstream work.
- **Service scheduling**: Appointments control arrivals, reservations estimate and spread demand, yield management allocates perishable fixed capacity across price categories, and workforce/cyclical schedules match staffing to predicted demand.

## Key Concepts
- **Job time** normally includes setup plus processing. Sequence-dependent setups make the order itself a cost decision; similar jobs may be grouped, but setup reduction can conflict with due-date performance.
- **Priority rules**: FCFS processes arrival order; SPT chooses the shortest remaining processing time; EDD chooses the earliest due date; CR chooses the smallest `CR = (due date - current time) / remaining processing time`; S/O chooses the smallest `(due date - remaining processing time) / remaining operations`; rush serves emergency or premium jobs first.
- **Measures**: Completion time `C_i` is a job's flow time when all jobs arrive at time zero. `Flow time` includes processing, queueing, transport, breakdown, parts, and quality delays. `Average flow time = sum(C_i) / n`. `Tardiness_i = max(0, C_i - d_i)` and `Average tardiness = sum(tardiness_i) / n`; lateness retains the signed difference. `Makespan` is the time from the first start to the last completion. `Average number of jobs in the system (or WIP) = total flow time / makespan` for the scheduled group.
- **Gantt charts** put time horizontally and resources or jobs vertically. Load charts show assigned and idle capacity; schedule/progress charts compare planned and actual work. They expose conflicts, idle time, slack, and completion timing, but require updating and do not directly price alternative schedules. I/O control compares planned and actual inputs and outputs and tracks backlog.
- **Forward scheduling** starts now and finds earliest completion, lateness, or slack. **Backward scheduling** starts from the due date and finds the latest feasible start. Finite schedules often need frequent revision as delays, cancellations, and new work occur.
- **Assumptions behind basic priority rules**: the job set is known and fixed, setup is deterministic and sequence-independent, processing times are deterministic, and no interruptions occur. Real systems violate these assumptions.

## Mental Models
- **Objective first**: SPT generally minimizes average flow time, WIP, and congestion; EDD directly prioritizes due dates and often minimizes lateness; FCFS supplies fairness and simplicity; CR emphasizes changing urgency. Select the measure before selecting the rule.
- **Bottleneck lens**: An hour lost at the constraint is an hour lost by the whole system. A busy nonbottleneck is not automatically useful, and improving it may not increase throughput.
- **Schedule as a control loop**: Load, visualize, release work, monitor I/O and backlog, then revise. A schedule is a living operating control, not a permanent promise.
- **Service variability lens**: Because services cannot usually be inventoried and arrivals and service times vary, the manager balances waiting cost against the cost of flexible or excess capacity.

## Anti-patterns
- Applying SPT without protecting long jobs, strategic customers, or promised dates; continuous arrival of short jobs can starve long jobs.
- Using FCFS as an efficiency rule in manufacturing, where a long job can delay many others, or abandoning FCFS in high-contact services where perceived fairness matters.
- Treating EDD as sufficient without considering processing time, or treating CR as an optimal answer rather than a revisable heuristic.
- Infinite-loading a fixed-capacity center and discovering overload only after commitments are made.
- Maximizing utilization at every resource while allowing the bottleneck to wait, or ignoring sequence-dependent setup, variability, no-shows, and machine interruptions.
- Using regular appointments or reservations without accounting for late arrivals, no-shows, and variable service duration.

## Worked Example
Six jobs have processing times A-F of `2, 8, 4, 10, 5, 12` days and due dates `7, 16, 4, 17, 15, 18`; all are available now. Total processing time, hence one-center makespan, is 41 days. FCFS gives A-B-C-D-E-F: total flow time 120, average flow time 20, average tardiness 9, and average WIP `120/41 = 2.93`. SPT gives A-C-E-B-D-F: averages are 18 days flow time, 6.67 days tardiness, and `108/41 = 2.63` jobs. EDD gives C-A-E-B-D-F: 18.33, 6.33, and `110/41 = 2.68`. CR dynamically gives C-F-A-E-B-D: 22.17, 9.67, and `133/41 = 3.24`. SPT is best for flow and WIP in this instance; EDD is slightly better for tardiness. A Gantt chart would make each cumulative completion time and idle interval visible. The result illustrates that sequencing is a trade-off, not a search for one rule that dominates every measure.

## Key Takeaways
1. Scheduling converts higher-level plans into timed resource use and must respect capacity.
2. Loading answers "where?"; sequencing answers "in what order?"
3. Use flow time and WIP to diagnose congestion, tardiness and lateness for delivery performance, and makespan for total completion.
4. Use finite capacity, Gantt/I/O controls, realistic dates, lot splitting, and bottleneck protection to keep schedules feasible.
5. In services, combine demand control, workforce flexibility, and multiple-resource coordination rather than relying on manufacturing rules alone.

## Connects To
- **Chapter 6**: Line balancing and work-system design shape high-volume flow schedules.
- **Chapters 12-13**: Inventory run-size logic, aggregate planning, and MRP supply the quantities and timing that scheduling must execute.
- **Chapter 17**: Project scheduling uses a different network-based logic for one-time work.
- **Chapter 18**: Waiting-line analysis explains the service-capacity consequences of variable arrivals, service times, and queues.

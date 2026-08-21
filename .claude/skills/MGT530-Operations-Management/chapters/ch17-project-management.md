# Chapter 17: Project Management

## Core Idea
Projects are unique, time-bounded operations with specific objectives, so they require an integrated approach to scope, time, cost, performance, resources, people, and risk. The manager converts a broad deliverable into sequenced work, estimates uncertainty, monitors actual progress and cost, and continually trades off time, budget, scope, quality, and risk. PERT/CPM networks make dependencies and schedule exposure visible; judgment, communication, and ethical leadership make the plan executable.

## Frameworks Introduced
- **Project life cycle:** Initiating defines goals, feasibility, expected benefits, costs, risks, and the project manager; planning specifies scope, deliverables, schedule, milestones, resources, budget, quality, staffing, and risk responses; executing performs the work; monitoring and controlling compares actual with plan and corrects deviations; closing transfers deliverables, secures acceptance, records lessons learned, and releases resources. Phases can overlap to save time, but overlap increases coordination and rework risk.
- **Project-management triangle:** Cost, schedule, and scope are interdependent constraints; quality is the resulting performance dimension. Changing one constraint normally forces a change in another.
- **Work breakdown structure (WBS):** Decompose the project hierarchically from the whole project to major elements, supporting activities, and task-level work packages. The resulting activity list anchors sequencing, time estimates, cost estimates, staffing, and the budget.
- **Gantt plus precedence network:** Use a Gantt chart to schedule and monitor activity duration and status; use an AOA or AON network to expose precedence, paths, critical work, and slack. In AOA, arrows are activities and nodes are events; in AON, nodes are activities. AOA may require a zero-time dummy activity to preserve precedence logic.
- **PERT/CPM:** Build the network, calculate activity timing, identify the longest path, quantify slack, and focus control or compression on schedule-threatening work. The methods are now practically interchangeable; deterministic CPM uses one time, while probabilistic PERT uses three.
- **Simulation:** When paths share activities or independence is doubtful, repeatedly sample activity durations from their distributions, calculate the longest path for each trial, and use the resulting project-duration distribution to estimate deadline probabilities.
- **Risk-management cycle:** Identify risks, assess probability and consequence, prioritize them in a probability-impact matrix, reduce or transfer exposure, monitor indicators, and maintain contingency actions and funds. Reassess as the project generates information.
- **Critical chain:** Add resource constraints to precedence logic. Protect the resource-constrained chain with feeding buffers, a project buffer at the end, and capacity buffers across projects.

## Key Concepts
- A **path** is a start-to-finish sequence of activities. The **critical path** is the longest expected path and determines expected project duration; its activities have zero slack. A shorter path has slack equal to critical-path length minus its own length, but slack may be shared among activities on that path.
- For deterministic times, use a forward pass and a backward pass: `EF = ES + t`; start activities have `ES = 0`; a successor with several predecessors has `ES = max(predecessor EF)`. Set final `LF` equal to project duration; `LS = LF - t`; an activity feeding several successors uses `LF = min(successor LS)`. Activity slack is `Slack = LS - ES = LF - EF`.
- For probabilistic activity estimates, `to` is optimistic, `tm` most likely, and `tp` pessimistic. Expected activity time is `te = (to + 4tm + tp) / 6`; activity variance is `sigma^2 = [(tp - to) / 6]^2 = (tp - to)^2 / 36`.
- Expected path duration is `mu_p = sum(te)`; path variance is `sigma_p^2 = sum(sigma^2)`; path standard deviation is `sigma_p = sqrt(sum(sigma^2))`. Activity standard deviations are not added directly.
- For a deadline `T`, `z = (T - mu_p) / sigma_p`, and the probability a path finishes by `T` is the normal-area value `Phi(z)`. If paths are independent, project completion probability is `P(project by T) = product(P_i)` across paths; lateness is its complement. Shared activities violate independence and can make a critical-path-only probability misleading.
- **Crashing** shortens an activity by adding resources, using faster equipment, or relaxing specifications. Compare normal and crash times/costs, available reduction, critical paths, and indirect cost or penalty savings. With total activity costs, the incremental crash slope is `(crash cost - normal cost) / (normal time - crash time)`.
- **Budget control** updates actual and projected cost by activity, compares each with budget, investigates both overruns and possible savings, and triggers corrective action before a projected overrun threatens the project.
- A project manager coordinates specialists who may report elsewhere, manages the ten broad areas of integration, scope, schedule, cost, quality, people, communication, risk, procurement, and stakeholders, and must handle conflict, ethics, motivation, and limited formal authority.

## Mental Models
- **Network as a constraint map:** Every merge waits for the latest predecessor; every split is governed by the earliest successor deadline. Delaying any activity matters only insofar as it consumes available slack or lengthens the longest path.
- **Schedule exposure is dynamic:** The critical path is a current forecast, not a permanent label. Variation can move another path into critical status, and a high-impact risk may sit off the current critical path.
- **Compress the bottleneck, not the busywork:** Crash only work that can reduce project duration, recheck the network after every reduction, and compare incremental cost with time-dependent benefit.
- **Buffers absorb variation:** In critical-chain management, monitor buffer consumption as an early-warning signal rather than hiding uncertainty inside every task estimate.

## Anti-patterns
- Treating a Gantt chart as sufficient for a complex project and ignoring dependency relationships.
- Omitting activities, misstating predecessors, or adding unexplained padding to estimates.
- Assuming the path with the largest expected duration is the only risk; ignoring shared activities, path correlation, emerging critical paths, or off-path risk events.
- Crashing a noncritical activity, or continuing compression after incremental cost exceeds avoided indirect cost, penalty, or strategic benefit.
- Tracking only completed work and not updating projected final cost, schedule, contingencies, or lessons learned.
- Treating software, a matrix structure, or a project manager as substitutes for sponsorship, communication, ethical reporting, and resource decisions.

## Worked Example
In the bank-opening network, the three path lengths are 18 weeks (`1-2-4-5-6`), 20 weeks (`1-2-5-6`), and 14 weeks (`1-3-5-6`). Therefore the project forecast is 20 weeks, the second path is critical, and path slack is 2, 0, and 6 weeks. A forward pass sets early starts and finishes; at a merge, the largest predecessor finish controls the next start. A backward pass from week 20 identifies latest times; zero activity slack confirms activities `1-2`, `2-5`, and `5-6` as critical. If shortening is needed, crash the least-cost reducible activity on the critical path one period at a time. Once the 18-week path also becomes critical, reduce both paths or choose a shared activity if that is cheaper. Stop when the next reduction costs more than the $1,000 daily indirect saving in the example.

## Key Takeaways
1. Start with scope and a WBS; schedule only after the work is complete enough to estimate.
2. Use Gantt charts for visibility and networks for logic, duration, criticality, and slack.
3. Deterministic analysis uses forward/backward passes; PERT converts three estimates into means and variances.
4. Project deadlines depend on all paths, not just the expected critical path; use simulation when paths share activities or dependencies matter.
5. Recalculate critical paths after progress, risk events, resource changes, or crashing.
6. Manage budget, risk, people, and ethics as part of schedule control, not as separate administrative work.

## Connects To
- **Chapter 9:** Six-Sigma improvement projects use the same scope, team, measurement, and control logic.
- **Chapter 16:** Critical-chain buffers extend constraint-management and theory-of-constraints thinking to project resources.
- **Operations strategy:** Projects can create strategic advantage, but uncertainty makes selection, sponsorship, monitoring, and lessons learned essential.
- **Risk and quality management:** WBS deliverables, milestone controls, contingency plans, and acceptance at closing connect project execution to broader operations control.

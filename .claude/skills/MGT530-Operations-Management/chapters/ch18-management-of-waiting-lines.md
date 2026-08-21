# Chapter 18: Management of Waiting Lines

## Core Idea
Waiting lines are the visible result of a temporary mismatch between demand and service capacity. Even an underloaded system develops queues when arrivals and service times vary; management must balance the cost of capacity against the cost of customers, employees, equipment, or work waiting.

## Frameworks Introduced
- **Capacity-waiting cost trade-off**: Minimize `TC = customer waiting cost + capacity cost`. Add servers, speed up service, or reduce variability only when the reduction in waiting cost justifies the added capacity or process cost.
  - When to use: Choosing staffing, docks, lanes, bays, or processing methods.
  - How: Estimate `L_s` and capacity cost for feasible alternatives, compute total cost, and stop increasing capacity after total cost rises.
- **Queuing-system classification**: Select a model by population source, number of channels, number of phases, arrival/service pattern, and queue discipline.
  - When to use: Before applying any waiting-line formula.
  - How: Decide finite versus infinite source; single versus multiple server; single versus multiple phase; FCFS versus priority; then test distribution assumptions.
- **Variability-utilization model**: Random arrivals and variable service create temporary overloads. As utilization approaches 1.0, average queue length and waiting time increase sharply, so 100% utilization is normally a poor target.
  - When to use: Diagnosing why a line exists despite adequate average capacity.
  - How: Reduce arrival bunching or service-time variation before simply adding capacity.
- **Psychology of waiting**: Perceived waiting can be shortened through information, occupation, comfort, fairness, and alternatives even when actual time cannot be reduced.
  - When to use: Customer-facing queues where anxiety, abandonment, or dissatisfaction matters.
  - How: Give a credible finite estimate, explain delays, keep people occupied, show progress, and offer reservations or alternate service paths.

## Key Concepts
- **Infinite-source**: The potential customer population is effectively unrestricted, as in a bank, restaurant, or toll bridge.
- **Finite-source**: The potential population is limited, such as a repairer serving a known group of machines.
- **Channel/server**: A person, crew, machine, or facility that serves one customer or unit at a time.
- **Phase**: A distinct service step at which a separate queue may form; theme-park attractions are successive phases.
- **Queue discipline**: The rule determining service order, usually first-come, first-served (FCFS).
- **Reneging, jockeying, balking**: Leaving a line, switching lines, or refusing to join because it looks too long.
- **Utilization**: The fraction of available capacity being used; for infinite-source systems, `rho = lambda/(M*mu)` and must be below 1.
- **Steady state**: Average arrival and service rates are stable after temporary startup or peak effects have passed.
- **Little's law**: In a stable system, `L = lambda*W`; therefore `L_s = lambda*W_s` and `L_q = lambda*W_q`.

## Mental Models
- **A queue is a variability buffer, not proof of insufficient average capacity.** Smooth arrivals and standardize work before treating every line as a staffing problem.
- **Slack is productive capacity in a variable system.** A server that is occasionally idle can prevent disproportionately expensive queues.
- **Pool when fairness and balancing matter.** One line feeding multiple servers supports FCFS and shares capacity; separate lines are analyzed as separate single-server systems and can leave one server idle while another line grows.
- **Protect the constraint.** In the short term, improve the bottleneck, shift demand, add temporary capacity, or standardize the service rather than assuming facility size is the only lever.

## Anti-patterns
- **Targeting 100% utilization**: In a variable system, small bursts create very long queues and poor customer experience.
- **Using a model without checking assumptions**: Poisson arrivals and exponential service are common approximations, but service often fits less well; use a better model or simulation when necessary.
- **Treating all customers identically when waiting costs differ**: Emergency cases, rush jobs, or short jobs may justify nonpreemptive priority classes, with FCFS within each class.
- **Optimizing only actual elapsed time**: An unexplained, uncertain, unfair, uncomfortable, or unoccupied wait feels longer and can cause balking or lost business.
- **Reporting cost estimates as exact**: Approximate rates and waiting costs do not support false precision; test plausible cost ranges.

## Worked Example
Trucks arrive at a warehouse at `lambda = 15` per hour, and each unloading crew serves at `mu = 5` per hour. With `r = lambda/mu = 3`, the multiple-server table gives `L_q` values of 1.528, 0.354, 0.099, and 0.028 for 4, 5, 6, and 7 crews. Thus `L_s = L_q + r` is 4.528, 3.354, 3.099, and 3.028. At $100 per crew-hour and $120 per truck-driver-hour, total hourly costs are $943.36, $902.48, $971.88, and $1,063.36. Five crews are optimal: the extra crew after five reduces waiting only slightly and costs more than it saves.

## Key Takeaways
1. Start with the source population, channels, phases, discipline, and distribution assumptions; model choice drives useful conclusions.
2. For infinite-source systems, calculate `rho`, then `L_q`, `L_s`, `W_q`, and `W_s`; keep arrival and service rates in the same time units.
3. Core relationships are `r = lambda/mu`, `L_s = L_q + r`, `W_q = L_q/lambda`, and `W_s = W_q + 1/mu = L_s/lambda`.
4. For `M/M/1`, `L_q = lambda^2/[mu*(mu-lambda)] = rho^2/(1-rho)` and `P_0 = 1-rho`; for `M/D/1`, `L_q = lambda^2/[2*mu*(mu-lambda)]`, roughly half the variable-service queue.
5. For `M/M/S`, use a single pooled line, equal-rate servers, `rho = lambda/(M*mu)`, and the multiple-server formulas or table for `L_q` and `P_0`. Conditional wait is `W_a = 1/(M*mu-lambda)`; overall `W_q = P_w*W_a`.
6. For finite sources, use `X = T/(T+U)` and finite-queue tables. With efficiency factor `F`: `J = N*F*(1-X)`, `L = N*(1-F)`, `H = F*N*X`, and `N = J+L+H`.
7. Reduce variability, shift demand to off-peak periods, find bottlenecks, communicate expected waits, and make waiting comfortable or productive.

## Connects To
- **Capacity planning**: Waiting-line analysis converts service-level targets into staffing, equipment, and space decisions.
- **Lean operations**: Waiting is non-value-added waste; standardization and smoother flow address its root causes.
- **Constraint management**: Bottleneck improvements, temporary workers, demand shifting, and faster processing can outperform blanket capacity expansion.
- **Service design and customer experience**: Reservations, priority rules, pooled lines, information, distractions, comfort, and perceived fairness shape both abandonment and satisfaction.

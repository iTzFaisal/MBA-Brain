# Supplement to Chapter 14: Maintenance

## Core Idea

Maintenance preserves the productive capability of a system by keeping facilities and equipment in working order and restoring them after failure. The objective is not to maximize maintenance activity; it is to minimize the total cost of dependable operation. That total includes scheduled maintenance, repairs, spare parts, labor, lost output, idle employees, schedule disruption, quality losses, injuries, and damage to equipment or facilities. Good maintenance therefore balances prevention against the consequences of breakdown while recognizing the different criticality of individual assets.

## Frameworks Introduced

- **Reactive/proactive continuum:** Breakdown maintenance responds after a failure. Preventive maintenance acts before failure through planned care. Predictive maintenance improves preventive timing by forecasting failure from records and technical data.
- **Total productive maintenance (TPM):** Operators perform routine care such as cleaning, inspection, and adjustment on the machines they use, while maintenance specialists handle more complex work. This distributes responsibility for equipment condition and supports lean/JIT operations.
- **Cost-balancing framework:** Increase preventive effort while the reduction in breakdown cost is worth more than the added prevention cost. The optimum is the minimum of combined cost, not the point of maximum prevention.
- **Criticality/Pareto framework:** A few assets usually account for most operational importance. Assign disproportionate protection to them; use moderate controls for important assets and limited expenditure for items that are seldom used or easily substituted.
- **Replacement policy:** Compare continued maintenance with replacement over the relevant operating and demand horizon, including technology, installation, training, downtime, and expected future failures.

## Key Concepts

**Breakdown maintenance** is the run-and-repair approach. It is unavoidable even with a strong preventive program, but relying on it exclusively creates uncertain downtime and exposes the operation to reduced capacity, delays, higher unit overhead, quality problems, and safety risks. Effective breakdown programs use some combination of standby equipment, spare parts and buffers, operators able to make minor repairs, and trained repair personnel who can respond quickly.

**Preventive maintenance (PM)** is periodic lubrication, adjustment, cleaning, inspection, and replacement of worn or critical parts. It can be scheduled from inspection findings, the calendar, accumulated operating hours, or units produced. Longer intervals lower PM spending but increase failure risk and expected breakdown cost; shorter intervals do the reverse. PM should also influence equipment selection and design: durable, accessible equipment is more likely to receive the care it needs. Training, correct operating procedures, and incentives reduce abuse and misuse.

**Predictive maintenance** uses installation data, operating hours, repair history, inspections, and technical signals to estimate when failure is likely. Better records make it possible to use equipment longer without waiting for failure, yet still intervene before a costly interruption. It is a timing method within a broader preventive strategy, not a substitute for basic care.

**Reliability and availability connection:** PM and predictive maintenance primarily improve reliability, the probability that equipment performs without failure for a specified period. Breakdown programs primarily protect availability by reducing the duration and operational impact of failures. Availability depends on both failure frequency and repair speed:

```text
Availability = uptime / (uptime + downtime)
             = MTBF / (MTBF + MTTR)
```

Thus, better PM can raise MTBF, while spare parts, standby capacity, and skilled responders reduce MTTR. The appropriate mix depends on the asset's consequences of failure, not merely its purchase price.

Useful decision formulas are:

```text
Expected breakdowns, E(B) = sum [b x P(b)]
Expected breakdown cost    = E(B) x cost per breakdown
Total maintenance cost     = PM cost + expected breakdown cost
```

Include hidden failure consequences in the breakdown-cost term. A PM policy is preferred when its cost is below the expected cost of repairing failures, subject to quality, safety, and service constraints.

## Mental Models

- **U-shaped cost curve:** With too little PM, breakdown and hidden costs dominate. With too much PM, scheduled labor and interruptions exceed the failures avoided. Seek the bottom of the curve.
- **Reliability versus recoverability:** Prevent failures when they are predictable and consequential; when prevention is uneconomic, make failure quick to detect, easy to repair, and less disruptive.
- **Few vital, many ordinary:** Rank assets by operational importance and substitutability before allocating spares, standby capacity, inspection effort, or specialist response.
- **Lifecycle rather than purchase price:** An old asset may be cheaper to keep today but more expensive across recurring failures, downtime, obsolescence, installation, training, and demand changes.

## Anti-patterns

- Running every asset to failure without accounting for lost production, safety, quality, or customer impact.
- Applying the same PM interval to every machine, regardless of age, condition, usage, or failure pattern.
- Performing excessive routine maintenance after its avoided-risk benefit has become negligible.
- Predicting failures without complete, accurate equipment and repair records.
- Treating maintenance as a specialist-only task and neglecting operator training and ownership.
- Replacing equipment based only on acquisition cost while ignoring removal, installation, learning-curve disruption, technology, and future demand.

## Worked Example

A machine has monthly breakdown probabilities of 0, 1, 2, and 3 failures equal to .20, .30, .40, and .10. With a $1,000 repair cost, the expected number of failures is:

```text
E(B) = 0(.20) + 1(.30) + 2(.40) + 3(.10) = 1.40
Expected repair cost = 1.40 x $1,000 = $1,400 per month
```

If PM costs $1,250 monthly and makes breakdown probability negligible, PM saves $150 per month and is preferred. This conclusion changes if PM disrupts production or if failure consequences were omitted; those amounts belong in the comparison.

For a second policy, suppose time to breakdown is normally distributed with mean 3 weeks and standard deviation .60 week. PM costs $250 and a breakdown costs $1,000. The cost ratio is `.25`. Use the lower-tail normal quantile for .25, `z = -.67`, then set the intervention interval to:

```text
t = mean + z(standard deviation)
  = 3 + (-.67)(.60) = 2.598, or about 2.6 weeks
```

The interval schedules PM shortly before the likely failure region, preserving use while lowering expected breakdown exposure.

## Key Takeaways

- Maintenance protects capacity, quality, delivery performance, safety, and cost.
- Breakdown, preventive, predictive, and TPM practices are complementary rather than mutually exclusive.
- The right PM frequency minimizes combined prevention and failure costs.
- Asset criticality and substitutability determine the strength of breakdown contingencies.
- Replacement is a forward-looking economic and operating decision, not simply a response to age.
- Reliability improves by preventing failures; availability also improves by shortening recovery time.

## Connects To

- **Lean/JIT:** TPM supports employee ownership and stable flow; unreliable equipment undermines lean schedules.
- **Quality and safety:** Equipment condition affects defect rates, product damage, and injury exposure.
- **Capacity and scheduling:** Downtime removes capacity and creates queues, delays, and missed delivery dates.
- **Inventory and service response:** Spare parts, buffers, standby equipment, and repair capability trade carrying cost for availability.
- **Capital budgeting:** Replacement compares lifecycle maintenance and downtime costs with the benefits and disruption of new technology.
- **Operations metrics:** MTBF, MTTR, reliability, and availability translate maintenance choices into operating performance.

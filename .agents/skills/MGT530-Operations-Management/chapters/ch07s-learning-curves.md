# Supplement to Chapter 7: Learning Curves

## Core Idea
Repeated human work generally becomes faster as experience accumulates. A learning curve models the resulting decrease in direct labor time per unit, making early high costs and later productivity gains estimable rather than anecdotal. The effect is most useful for new, complex, repetitive work; routine, mass-production, and machine-paced work usually show little practical learning. The curve approaches, but never reaches, zero time. Improvement reflects worker learning plus design, tooling, methods, planning, scheduling, motivation, and other managerial inputs. Process changes can create temporary setbacks and a scalloped rather than smooth pattern.

## Frameworks Introduced
- **Doubling-rule learning percentage:** The learning percentage (LR) is the fraction of time retained whenever cumulative repetitions double. An 80% curve means a 20% reduction; 90% means a 10% reduction; 100% means no improvement. Typical rates are roughly 70%-90%. Lower percentages represent faster learning.
- **Unit-time model:** The time for the specific nth unit is
  \[
  T_n=T_1n^b, \qquad b=\frac{\ln(LR)}{\ln 2}.
  \]
  This is the incremental time model: it predicts unit n, not the average of all units.
- **Cumulative-average model:** The average for the first n units is
  \[
  \bar T_n=\frac{\text{Total time through }n}{n}.
  \]
  Thus, using a total-time factor, \(\bar T_n=T_1F_{total}(n,LR)/n\). Always distinguish the time for unit n from the average time across units 1 through n.
- **Table-factor method:** A learning table supplies a unit-time factor and a total-time factor. Multiply either factor by the first-unit time: \(T_n=T_1F_{unit}\) or \(Total_n=T_1F_{total}\). If a later unit is more reliable than the first, estimate \(T_1=T_n/F_{unit}\).
- **Data-based rate estimation:** Compare observed times at doublings, such as \(T_2/T_1\), \(T_4/T_2\), and \(T_6/T_3\). Because observations vary, use a smoothed, defensible approximation rather than expecting identical ratios.
- **Time-to-cost translation:** Convert projected labor hours to labor cost, then add setup, materials, and applicable overhead. Divide total production cost by quantity for average unit cost and compare it with a purchase price or bid target.

## Key Concepts
- The log-log relationship between repetitions and time is approximately linear when a constant learning percentage is appropriate.
- **Model assumptions:** the work is repetitive and human-involved; the learning percentage is reasonably stable over the forecast range; the first-unit time and operating conditions are representative; and major process changes, plateaus, carryover, and indirect-cost shifts are recognized separately. Results remain approximations.
- The absolute time saving becomes smaller as repetitions increase, even though the percentage rule remains constant.
- A total-time factor includes every unit through n; a unit-time factor applies only to unit n. The total divided by n gives the cumulative average.
- Carryover experience with similar work can reduce initial time, while the learning rate for the new work may remain unchanged.
- Learning projections quantify expected future improvement for manpower scheduling, purchasing, pricing, inventory, and capacity decisions.
- Productivity gains can increase material usage rates and output requirements, so labor, materials, and capacity must be planned together.

## Mental Models
- **Learning percentage is a retention rule, not an improvement rate:** LR tells you what remains after each doubling.
- **Separate “next unit” from “first n units”:** Unit time answers a marginal question; cumulative total and average answer a batch question.
- **Volume creates a strategic flywheel:** More volume moves operations down the curve, lowering cost and potentially supporting market-share growth, further volume, and a shift from batch to repetitive operations.
- **Treat the curve as a forecast that learns:** Start with the best available base and rate, then update them as reliable production data arrive.

## Anti-patterns
- Calling an 80% learning curve an 80% improvement instead of a 20% reduction.
- Applying a unit factor to estimate a batch total, or using a total factor as if it were the time for one unit.
- Blindly accepting an unusual first-unit time or extrapolating indefinitely through a plateau or end-of-job slowdown.
- Treating a smooth curve as literal when redesigns, tooling changes, or worker transfers create scallops.
- Assuming lower direct labor time means lower total cost while ignoring supervision, maintenance, material handling, setup, materials, and overhead.
- Applying learning curves to stable mass production or machine-paced work without evidence of a meaningful human learning effect.

## Worked Example
An aircraft job has an 80% curve and the first aircraft requires 400 labor-days. From the table at 20 units, the unit factor is 0.381 and the total factor is 10.485:

\[
T_{20}=400(0.381)=152.4\text{ labor-days}
\]
\[
Total_{20}=400(10.485)=4,194\text{ labor-days},\qquad
\bar T_{20}=4,194/20=209.7\text{ days per aircraft}.
\]

If the first estimate is distorted but unit 3 actually took 276 days, use its 80% unit factor, 0.702: \(T_1=276/0.702=393.2\) labor-days. For cost, multiply projected total hours by the labor rate and add setup, per-unit materials, and the stated overhead policy before comparing the resulting average cost with a supplier price.

## Key Takeaways
1. Use learning curves primarily for new or complex repetitive work involving meaningful human performance improvement.
2. Interpret LR as the fraction of time retained after output doubles; validate it with empirical data.
3. Use the unit-time model for a particular repetition and cumulative totals/averages for a production quantity.
4. Base all projections on a credible first-unit estimate, and revise it when later observations are better evidence.
5. Use the estimates in staffing, bids, pricing, procurement, inventory, capacity, and strategic volume decisions, while treating them as approximations.

## Connects To
Learning curves connect work-system design to manpower planning, training and job placement, negotiated purchasing, new-product pricing, budgeting, inventory and material replenishment, and capacity planning. Strategically, faster movement down the curve can support time-based market entry and cost advantage. Operationally, the method complements process improvement and cost accounting but must be adjusted for indirect labor, carryover experience, short product life cycles, flexible manufacturing, cross-functional workers, and changing processes.

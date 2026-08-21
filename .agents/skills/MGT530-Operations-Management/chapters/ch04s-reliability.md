# Supplement to Chapter 4: Reliability

## Core Idea

Reliability is the probability that a product, service, part, or system will perform its intended function under stated conditions, either when it is activated or throughout a specified service interval. It is therefore a design and operations measure, not merely a component attribute. A system can contain highly reliable parts and still be unreliable when many parts must all work. Availability is related but different: it is the fraction of operating time for which equipment is expected to be usable.

## Frameworks Introduced

- **Point-in-time reliability:** Calculate the chance that the system functions when called upon.
- **Time-based reliability:** Calculate the chance that the item survives to a specified time.
- **Reliability block logic:** Series elements require every element to succeed; redundant or parallel elements require at least one successful path.
- **Availability cycle:** Equipment alternates between operating time (MTBF) and repair/down time (MTTR, called MTR in the supplement), so both failure frequency and repair speed matter.
- **Failure-life models:** A bathtub failure-rate pattern separates early defects, relatively random failures, and wear-out. Exponential modeling is useful for a constant/random failure pattern; normal modeling is useful when wear-out life clusters around a mean.

## Key Concepts

- **Independent events:** The success or failure of one component does not change another component's probability. The standard system formulas depend on this assumption.
- **Series system:** If all independent components must operate, 
  \[
  R_s = \prod_{i=1}^{n} R_i.
  \]
  With identical components, \(R_s=R^n\); adding required components lowers reliability unless their reliabilities are perfect.
- **Standby/backup redundancy:** If a primary component is tried first and a backup is used only after primary failure, two components give
  \[
  R_s=R_1+(1-R_1)R_2.
  \]
  For ordered backups, \(R_s=R_1+R_2(1-R_1)+R_3(1-R_2)(1-R_1)\). A transfer switch must also work; if its reliability is \(R_{sw}\), the backup-success term becomes \((1-R_1)R_{sw}R_2\).
- **Parallel/at-least-one logic:** For independent components where any one functioning component is enough,
  \[
  R_s=1-\prod_{i=1}^{n}(1-R_i).
  \]
  This is the complement rule: system success is one minus the probability that every component fails. It is equivalent to adding the first success plus the probability that earlier options fail and a later option succeeds.
- **Exponential life:** If service time \(T\) follows the exponential model with mean MTBF,
  \[
  R(T)=P(\text{no failure before }T)=e^{-T/MTBF},
  \]
  and \(P(\text{failure before }T)=1-e^{-T/MTBF}\). Longer service horizons reduce reliability. The model uses one mean parameter and assumes the applicable failure behavior is exponential; it is not automatically a wear-out model.
- **Normal wear-out life:** If wear-out time has mean \(\mu\) and standard deviation \(\sigma\), standardize with \(z=(T-\mu)/\sigma\). The normal table gives \(P(\text{wear-out}\le T)\); reliability through \(T\) is its complement.
- **Availability:**
  \[
  A=\frac{MTBF}{MTBF+MTTR},
  \]
  where MTTR (the supplement's MTR) is mean time to repair, including waiting time. Availability rises with longer MTBF and shorter repair time.

## Assumptions

- Component reliabilities describe the same operating conditions and the same definition of success; changing load, environment, or service horizon can change the probabilities.
- Product-of-probabilities and all-failures formulas require independent component events. Shared power, controls, environment, or common-cause defects break that simple assumption.
- A series diagram means every required element must function. A parallel or standby diagram means the stated alternative path is genuinely capable of completing the required function.
- Standby calculations assume the backup is available when needed and that activation occurs as specified. A less-than-perfect switch, sensor, or transfer mechanism must be included as another required factor.
- Exponential calculations assume the exponential model is appropriate for the relevant life phase and use MTBF as its mean. Normal calculations assume wear-out times are adequately represented by a mean and standard deviation.
- Availability is a long-run operating measure based on comparable time units and average operating and repair cycles; repair waiting time belongs in MTTR.

## Mental Models

- **The weakest structure matters:** In series, reliability compounds downward because one failure stops the system.
- **Backups buy alternatives, not certainty:** Redundancy improves reliability only when failures are sufficiently independent and the activation path is dependable.
- **Reliability is horizon-sensitive:** A product may be likely to work now but unlikely to survive a long warranty period.
- **Design for uptime in two directions:** Prevent failures and make recovery fast; improving only one side may leave availability constrained by the other.

## Anti-patterns

- Multiplying reliabilities for a system that needs only one successful path; use the complement of all failures instead.
- Treating a backup as perfect without checking its switch, transfer mechanism, or standby assumptions.
- Assuming high component reliability guarantees high system reliability when many components are in series.
- Confusing MTBF with repair time, or omitting repair waiting time from MTR.
- Applying the exponential model to wear-out data without evidence that its assumptions fit.

## Worked Example

Three independent components are used in ordered standby: primary reliability \(0.94\), first backup \(0.90\), and second backup \(0.80\). Assuming a perfect transfer mechanism,

\[
R_s=0.94+0.90(0.06)+0.80(0.10)(0.06)=0.9988.
\]

For a time-based check, if MTBF is 10 years, reliability at 5 years is \(e^{-0.5}=0.6065\), while failure before 5 years is \(0.3935\). If MTTR is 2 hours, availability with MTBF 200 hours is \(200/(200+2)=0.9901\), approximately 0.99. The example shows why redundancy and repairability address different failure consequences.

## Key Takeaways

- Start by defining success: all components, at least one component, or survival through time.
- Use products for independent required elements and \(1-\)all-failures for independent alternatives.
- Evaluate switches and shared dependencies; a common failure can invalidate apparent redundancy.
- Use \(e^{-T/MTBF}\) for the stated exponential-life assumption and \(A=MTBF/(MTBF+MTTR)\) for steady operating availability.
- Reliability, maintainability, cost, and interruption consequences should be evaluated together in design decisions.

## Connects To

Reliability analysis supports product design, warranty and service-period decisions, preventive maintenance, spare/backup capacity, repairability, and operations continuity. It also connects probability rules to system architecture: a line with required sequential machines behaves as a series system, whereas duplicate lines or independent alarms create alternative paths whose value depends on switching, common-cause risk, cost, and the severity of downtime.

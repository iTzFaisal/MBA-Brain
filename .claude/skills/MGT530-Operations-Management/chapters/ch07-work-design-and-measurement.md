# Chapter 7: Work Design and Measurement

## Core Idea
Work design specifies what a job contains, who performs it, how it is performed, and where it is performed. Good design balances productivity, quality, safety, flexibility, and quality of work life. The chapter connects four decisions: job design sets content; methods analysis determines the method; motion study removes unnecessary movement; and work measurement estimates the time a qualified worker should need. A standard is useful only when method, tools, materials, layout, conditions, and human factors are treated as one system.

## Frameworks Introduced
- **Systems view:** Link work design to product or service design, process choice, layout, technology, safety, compensation, and the supply chain. A local efficiency that damages flow, quality, or worker well-being is not a system improvement.
- **Two schools of job design:** The efficiency school emphasizes specialization, logical methods, and low unit cost; the behavioral school emphasizes meaningful work, satisfaction, involvement, and motivation. Effective practice combines both.
- **Job-breadth continuum:** Specialization narrows work; enlargement adds horizontal variety; rotation exchanges assignments; enrichment adds vertical responsibility for planning and coordination. Use the least narrow design that still supplies needed efficiency and control.
- **Quality-of-work-life and ergonomics screen:** Evaluate leadership and relationships together with temperature, ventilation, lighting, noise, vibration, breaks, health, safety, compensation, posture, cognitive load, communication, teamwork, and work arrangements. Ergonomics fits tasks and equipment to human abilities and limits.
- **Methods-analysis cycle:** Identify and document the job, consult the operator, question movements and delays, propose and install a better method, retrain as needed, and follow up. Participation improves diagnosis and adoption.
- **Motion-study toolkit:** Apply motion principles to body use, workplace arrangement, and tool design; use therbligs for elemental motions, micromotion study for very rapid work, and flow or simultaneous-motion charts for sequence and interaction. Eliminate, combine, simplify, or rearrange motions while reducing fatigue.
- **Measurement choice:** Use stopwatch study for short repetitive work; standard elemental times from a reliable internal file when available; predetermined standards such as MTM when published elemental data fit; and work sampling for nonrepetitive work, ratio-delay questions, and activity proportions.
- **Stopwatch standard chain:** Validate the method, observe time, rate performance, then apply allowances: `OT -> NT -> ST`. Skipping any link makes a standard misleading.
- **Compensation choice:** Time pay is stable and simple; output pay can raise output but needs credible standards and quality safeguards; knowledge-based pay rewards horizontal, vertical, and depth skills and supports cross-training.

## Key Concepts
- **Job design and specialization:** Job design addresses what, who, how, and where, with objectives of productivity, safety, and quality of work life. Specialization simplifies training and can produce high productivity and low unit cost, but narrow work can create monotony, low control, weak quality ownership, absenteeism, turnover, and limited advancement. Enlargement adds tasks at similar responsibility; rotation periodically exchanges jobs; enrichment adds discretion, planning, and coordination. Enlargement without autonomy may only add fatigue.
- **People, teams, and safety:** Trust enables delegation and positive response. Self-directed teams can change processes under their control, but need training in quality, improvement, and teamwork; conflict and threatened middle-management roles are risks. Working conditions, hours, breaks, health care, and safety affect fatigue, quality, productivity, and accidents. Control unsafe acts and conditions with training, housekeeping, guards, protective equipment, emergency provisions, and enforcement. Ethical design also requires accurate records, unbiased appraisal, fair pay, and real advancement.
- **Methods analysis:** Study work from the whole operation to workplace arrangement and worker/material movement. Prioritize high-labor, frequent, unsafe, unpleasant, bottleneck, or quality-problem jobs. A flow process chart exposes operation, transport, storage, delay, and inspection; a worker-machine chart exposes busy and idle time and possible machine loading.
- **Motion study:** Typical motion principles include fixed locations, gravity feed, accessible controls, fixtures, balanced hand use, and smooth curved motions. Therbligs include search, select, grasp, hold, transport load, release, inspect, position, plan, rest, and delay. Micromotion uses motion pictures and slow replay and is justified mainly for repetitive or unusually important work.
- **Standard time:** A fully trained, qualified worker should complete the specified task at an efficient, sustainable pace using specified methods, tools, materials, conditions, and workplace arrangement. A material change in any parameter can require a new study. Standard elemental times reuse historical internal data; predetermined standards such as MTM use published research on basic motions, but both depend on accurate element definitions and fit.
- **Observed, normal, and standard time:** Observed time is the average recorded time, `OT = sum(x_i) / n`. Normal time adjusts pace: `NT = OT * PR`; with element ratings, `NT = sum(xbar_j * PR_j)`. Standard time adds personal, fatigue, unavoidable-delay, and break allowances: `ST = NT * AF`. A normal pace has `PR = 1.00`; `0.90` is slower and `1.05` faster. Machine time is normally rated `1.00`. Ratings are judgmental, so analysts need training, recalibration, documentation, and sometimes a second analyst.
- **Allowance factors:** For an allowance based on job time, `AF_job = 1 + A`. For an allowance based on the workday, `AF_day = 1 / (1 - A)`. They are not interchangeable: 20 percent of job time gives `1.20`, while 20 percent of workday time gives `1.25`.
- **Stopwatch sample size:** For error stated as a percentage of the mean, `n = (z*s / (a*xbar))^2`; for error stated as time, `n = (z*s / e)^2`. Use a pilot `xbar` and `s`, choose `z` for confidence, round up, and recompute as data improve. Discard an unusually short observation only when investigation supports observational error; investigate a long observation because a recurring delay may belong in the standard.
- **Work sampling:** Make brief, random observations and record activity categories rather than continuously timing work. It suits ratio-delay studies, machine idle time, nonrepetitive jobs, job-content validation, and time by skill level. The sample proportion is `p_hat = occurrences / n`; for a large sample, maximum probable error is `e = z * sqrt(p_hat*(1-p_hat)/n)`, and required sample size is `n = (z/e)^2 * p_hat*(1-p_hat)`. If `p_hat` is unknown, start with `0.50`, round up, and revise.
- **Valid sampling and technique fit:** Define the worker, machine, activity, and study period; notify participants; generate random days, hours, and minutes; spread observations across the period; count categories; and recompute sample size. Stopwatch study is detailed, element-based, and disruptive but best for short repetitive cycles. Work sampling is cheaper, less disruptive, interruptible, and better for varied work, but is coarser and depends on random timing.

## Mental Models
- **Design before measure:** A precise standard for an unsafe or wasteful method institutionalizes the wrong behavior.
- **Normalize, then allow:** Performance rating answers whether the observed pace is normal; allowances answer what sustainable time includes. Do not merge the two adjustments.
- **A standard is conditional:** Read it as "under these methods, tools, materials, layout, conditions, and allowance assumptions."
- **Two customers:** Management needs capacity and cost information; workers need sustainable pace, safety, fairness, and participation. Ignoring either customer makes gains temporary.
- **Resolution follows variability:** Use detailed timing for repeating elements and random snapshots when the question is how varied work time is distributed.

## Anti-patterns
- Treating specialization as automatically superior or adding tasks without adding meaning.
- Measuring before validating the method, or using one worker or one observation as the standard.
- Hiding, inconsistently applying, or failing to recalibrate performance ratings.
- Confusing job-time and workday allowance bases.
- Deleting long observations automatically or retaining short observational errors without investigation.
- Sampling predictably, in a cluster, or over too short a period.
- Using stopwatch study for irregular work, work sampling for short repetitive cycles, or predetermined data when the elemental breakdown does not fit.
- Rewarding quantity without quality, safety, breakdown, and fairness controls.

## Worked Example
**Stopwatch standard.** Nine observations of an assembly element total `10.35` minutes. With `PR = 1.13` and a job-time allowance `A = 0.20`:

1. `OT = 10.35 / 9 = 1.15` minutes.
2. `NT = 1.15 * 1.13 = 1.2995`, or about `1.30` minutes.
3. `AF_job = 1 + 0.20 = 1.20`.
4. `ST = 1.2995 * 1.20 = 1.5594`, or about `1.56` minutes per cycle.

If the 20 percent allowance were workday-based instead, `AF_day = 1/(1-.20) = 1.25`, producing about `1.62` minutes. The analyst must first confirm that the method is efficient and that unusual delays were handled correctly.

**Sample-size checks.** With `xbar = 6.4`, `s = 2.1`, and 95 percent confidence (`z = 1.96`), a 10 percent error requires `n = (1.96*2.1/(0.10*6.4))^2 = 41.36`, so plan `42` observations. A half-minute error requires `n = (1.96*2.1/0.5)^2 = 67.77`, so plan `68`.

**Work sampling.** With `p_hat = 0.30`, `n = 400`, and 90 percent confidence (`z = 1.65`), `e = 1.65*sqrt(0.30*0.70/400) = 0.038`, or about 3.8 percentage points. For a 5-point target, `n = (1.65/0.05)^2*0.30*0.70 = 228.69`, rounded up to `229`.

## Key Takeaways
1. Work design integrates job content, methods, measurement, safety, compensation, and quality of work life.
2. Balance specialization's efficiency with motivation, autonomy, learning, quality, and retention.
3. Use enlargement, rotation, enrichment, cross-training, and teams deliberately; they are not interchangeable.
4. Treat ergonomics and working conditions as productivity and quality variables.
5. Improve and stabilize the method before establishing a standard, and involve the operator.
6. Use charts to expose transport, delay, storage, inspection, and idle time.
7. Compute `OT`, adjust to `NT`, and apply the correct allowance factor to obtain `ST`.
8. Use stopwatch study for repetitive detail and work sampling for broad, nonrepetitive proportions.
9. Align compensation with effort, quality, safety, and controllable results rather than output alone.

## Connects To
- **Product/service design and process/layout:** Complexity, customization, process type, and layout determine work content, travel, machine interaction, and skill needs.
- **Productivity and capacity:** Standard times support labor cost, capacity, workforce planning, scheduling, budgeting, and incentives.
- **Quality and lean operations:** Fatigue, poor methods, quantity-only incentives, cross-training, empowerment, reduced motion, visual flow, and delay elimination affect defects and improvement.
- **Human resources and ethics:** Teams, training, appraisal, compensation, safety, and fair advancement determine whether efficiency gains are sustainable.

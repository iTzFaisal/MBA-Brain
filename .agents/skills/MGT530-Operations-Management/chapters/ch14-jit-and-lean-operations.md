# Chapter 14: JIT and Lean Operations

## Core Idea

Lean is a philosophy and operating method for producing value with fewer resources by removing activities that do not add customer value. Just-in-time (JIT) is the tightly coordinated form of lean in which materials, work, and services arrive or occur when needed. The ultimate goal is a balanced, rapid, uninterrupted flow that matches supply to customer demand. Low inventory is a consequence of a capable system, not the whole definition of lean.

Three supporting goals make that flow possible: eliminate disruptions, make the system flexible, and eliminate waste, especially excess inventory. Lean works best when quality, equipment reliability, setup speed, worker capability, supplier performance, and demand are stable enough to support close coordination. Its benefits include lower cost, lead time, space, scrap, and rework, plus better quality, flexibility, productivity, and equipment use. Its risks are equally practical: little inventory or spare capacity is available when a breakdown, defective supply, demand surge, or transport disruption occurs.

## Frameworks Introduced

- **Five lean principles:** define value from the customer's perspective; identify value-creating processes; remove waste to create flow; produce only in response to demand; pursue perfection through continuous improvement.
- **Toyota Production System (TPS):** *muda* means waste; *kanban* signals replenishment or movement; *heijunka* levels workload and mix; *kaizen* means continuous improvement; *jidoka* or autonomation builds quality at the source by detecting a problem and stopping for correction.
- **Lean building blocks:** product design, process design, personnel/organizational elements, and manufacturing planning/control. Speed and simplicity link all four.
- **Eight wastes:** excess inventory, overproduction, waiting, unnecessary transportation, processing waste, inefficient work methods, defects, and underused people. Each is a target for investigation, not merely a label.
- **Flow-control choices:** a push system sends work onward when it is completed; a pull system lets the next operation authorize work as needed. Kanban controls local replenishment, while CONWIP limits total system WIP and can tolerate more variability.

## Key Concepts

**Design for lean.** Standard parts reduce variety in purchasing, handling, training, and processing. Modular design groups parts into manageable units. Quality must be designed into the product and process because small lots and minimal buffers expose defects immediately. Concurrent engineering reduces disruptive late changes.

**Process design.** Small lots reduce WIP, space, carrying cost, defect exposure, and response time. They require fast, inexpensive setups. Shingo's SMED separates internal activities, possible only while equipment is stopped, from external activities, which can be prepared while it runs; convert internal work to external work, then simplify what remains. Manufacturing cells group equipment for part families, reducing movement and setup while supporting cross-training. Line balance assigns each station work no greater than takt time, the cycle time needed to match demand. Fail-safe *poka-yoke* prevents or signals errors.

**People, quality, and reliability.** Workers are assets: they need training, authority, and responsibility for quality and improvement. Cross-training lets teams cover absences, bottlenecks, and changing demand. Andon makes abnormalities visible; jidoka stops the process so root causes are corrected rather than passed forward. Preventive maintenance, operator care, and clean, orderly workspaces protect flow. The five S behaviors are sort, straighten, sweep, standardize, and self-discipline. Managers act as leaders and facilitators, not merely order givers. Activity-based costing can assign overhead more realistically to setups, inspections, machine time, movement, and other activities.

**Planning and supply.** Heijunka creates a level daily mix and stable short-term schedule. Mixed-model sequencing spreads products across the day while balancing setup cost against smoothness. Kanban cards or containers authorize production (*p-kanban*) or conveyance (*c-kanban*); no signal means no movement or production. A useful sizing relationship is `N = D T (1 + X) / C`, where `D` is usage rate, `T` is replenishment plus production time, `X` is an inefficiency allowance, and `C` is container capacity. WIP is also governed by Little's law: `WIP = arrival rate x cycle time`.

Lean extends beyond the factory. Close, long-term vendor relationships replace price-only, adversarial sourcing: certified suppliers provide frequent, small, high-quality deliveries, often through tiered supplier networks. Direct-to-floor delivery, fewer transactions, bar coding, and supplier certification reduce the "hidden factory" of ordering, expediting, inspection, and change processing.

## Mental Models

- **Inventory is water covering rocks.** High inventory hides breakdowns, quality problems, late suppliers, and poor schedules. Lower it gradually, solve the exposed problem, then lower it again. Removing buffers before building capability is not lean; it is fragility.
- **Takt is the system heartbeat.** Demand sets the pace; line balance and capacity must fit that pace. A station that exceeds takt becomes a bottleneck that interrupts the whole flow.
- **Pull is a customer-supplier chain.** Each downstream process is the customer of the preceding process and sends a demand signal backward. Production should replenish actual use, not create work merely because capacity is available.
- **Lean is socio-technical.** Tools cannot substitute for quality at the source, reliable equipment, trained workers, cooperative suppliers, and leadership that supports problem reporting.

## Anti-patterns

- Equating lean with aggressive inventory cuts or treating kanban as a complete lean system.
- Reducing WIP before fixing defects, long setups, unreliable equipment, bottlenecks, or supplier performance.
- Pushing large batches that maximize local utilization while creating queues, hidden defects, and long response times.
- Keeping suppliers adversarial, changing schedules unpredictably, or demanding small deliveries without sharing support and risk.
- Performing a ceremonial gemba walk that observes without learning, coaching, or inviting worker concerns.
- Giving workers more accountability without authority, training, psychological safety, or recognition.
- Applying a rigid manufacturing template to services without considering customer participation, variety, and the value of speed.

## Worked Example

Suppose two shifts each contain 480 minutes, with two 20-minute breaks and a 30-minute meal period per shift. Net time is `480 - 40 - 30 = 410` minutes per shift, or `820` minutes per day. With demand of 80 units, takt time is `820 / 80 = 10.25 minutes per unit`. Each workstation must therefore receive no more than about 10.25 minutes of work if the line is to match demand.

For a kanban check, if a work center uses 300 parts per day, a container circuit takes 0.12 day, management allows 20 percent inefficiency, and each container holds 25 parts, then `N = 300 x 0.12 x 1.20 / 25 = 1.728`. Round up to two containers. As the process becomes more reliable and the allowance or circuit time falls, fewer containers can support the same flow.

## Key Takeaways

1. Lean pursues customer value, flow, demand pull, and perfection; JIT is coordinated execution of that philosophy.
2. The three supporting goals are disruption elimination, flexibility, and waste elimination.
3. Product/process design, people, and planning must reinforce one another; a kanban card cannot repair poor quality or unstable flow.
4. Small lots require SMED, cells, level loading, balanced work, quality at the source, and preventive maintenance.
5. Gemba, value stream mapping, 5W2H questioning, five S, and lean plus Six Sigma turn observation into improvement: lean attacks delay and non-value-added work, while Six Sigma reduces variation.
6. Lean services reduce waiting, errors, duplicate work, excess supplies, and processing time; JIT II extends pull through vendor-managed inventory, with a supplier representative managing replenishment on-site.
7. Conversion usually takes substantial time and may take one to three years. It needs top-management commitment, worker cooperation and training, staged implementation, supplier partnership, and a willingness to preserve or add temporary buffers while root causes are fixed.

## Connects To

Lean links directly to line balancing and capacity planning through takt time; inventory and queue analysis through Little's law; quality management and Six Sigma through jidoka and variation reduction; maintenance through reliability and preventive work; supply chain management through supplier tiers, certification, and JIT delivery; ERP/MRP through planning-execution hybrids; and operations strategy through the decision about whether demand stability, process capability, and organizational culture justify conversion. In services, the same logic appears as fast, standardized, flexible delivery with minimal waiting and work-in-process.

# Chapter 3: Process Cost Systems

## Core Idea
A process cost system accumulates costs by department or process for continuous production of indistinguishable units. The cost of production report allocates departmental costs between transferred-out units and partially completed ending WIP using equivalent units and a cost-flow assumption.

## Frameworks Introduced
- **Process cost system**: Use for standardized, continuous production such as chemicals, food, paper, fuel, or electricity.
- **Cost of production report**: Apply four steps: determine units to account for, compute equivalent units, compute cost per equivalent unit, and allocate costs to transferred-out and ending WIP.
- **Equivalent-units framework**: Translate partially completed physical units into completed-work equivalents, normally separately for materials and conversion.
- **FIFO method**: Isolate current-period work and cost; charge only the remaining work needed to complete beginning WIP.
- **Weighted-average method**: Blend beginning WIP costs with current-period costs; do not separately identify current work on beginning WIP.
- **Yield analysis**: Use `output quantity / input quantity` to expose material loss, scrap, or waste.
- **Spoilage rule**: Treat expected normal spoilage as product cost; treat abnormal spoilage beyond expected levels as a loss.

## Key Concepts
- **Whole units**: Physical units in production, complete or incomplete.
- **Equivalent unit of production**: One fully completed unit of work for a particular cost category.
- **Conversion costs**: Direct labor plus factory overhead.
- **Transferred-in costs**: Accumulated cost received from a preceding department and added to the receiving department's WIP.
- **Cost reconciliation**: Costs to account for must equal costs assigned to transfers and ending WIP.
- **Started and completed**: Transferred-out units less beginning WIP units under FIFO.

## Mental Models
- Materials and conversion have separate completion clocks.
- Equivalent units measure work performed, not physical units sitting in a department.
- Cost follows the product through the production pipeline and across department boundaries.
- Normalize total costs to cost per equivalent unit before diagnosing operations.

## Anti-patterns
- Treating all whole units as fully complete.
- Using one completion percentage when materials and conversion enter at different points.
- Counting prior-period work in current-period FIFO equivalent units.
- Blending beginning and current costs while calling the result FIFO.
- Omitting transferred-in costs from the receiving department.
- Failing to reconcile both units and dollars.
- Treating abnormal spoilage as ordinary product cost.

## Worked Example
Frozen Delight's Mixing Department has beginning WIP of `5,000` gallons at `70%` conversion, adds `60,000` gallons, transfers out `62,000`, and ends with `3,000` gallons at `25%` conversion. Materials added are `$66,000`; current conversion costs are `$17,775`; beginning WIP cost is `$6,225`.

1. Started and completed = `62,000 - 5,000 = 57,000` gallons.
2. FIFO equivalent units: materials `0 + 57,000 + 3,000 = 60,000`; conversion `1,500 + 57,000 + 750 = 59,250`.
3. Materials cost per EU = `$66,000 / 60,000 = $1.10`; conversion cost per EU = `$17,775 / 59,250 = $0.30`.
4. Complete beginning WIP = `$6,225 + (1,500 x $0.30) = $6,675`.
5. Started-and-completed cost = `57,000 x ($1.10 + $0.30) = $79,800`.
6. Transferred out = `$86,475`; ending WIP = `(3,000 x $1.10) + (750 x $0.30) = $3,525`.
7. Reconciliation: `$6,225 + $83,775 = $86,475 + $3,525 = $90,000`.

## Key Takeaways
1. Process costing is for homogeneous, continuous production; job costing is for custom work.
2. Use the four-step cost-of-production report before interpreting costs.
3. Compute materials and conversion equivalent units separately when completion differs.
4. FIFO isolates current-period performance; weighted average blends periods.
5. Transferred-in cost is part of the receiving department's product cost.

## Connects To
- **Ch 2**: Provides the alternative to job order costing.
- **Ch 4-5**: Uses the same product-cost and allocation foundations.
- **Ch 13**: Yield, spoilage, flow, and zero-defect ideas support lean improvement.
- **Ch 15-16**: Departmental inventories and cost flows reach financial statements.

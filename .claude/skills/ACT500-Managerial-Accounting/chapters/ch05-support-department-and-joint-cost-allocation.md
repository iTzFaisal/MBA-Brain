# Chapter 5: Support Department and Joint Cost Allocation

## Core Idea
Support departments provide services to production departments, while joint processes create multiple outputs before a split-off point. Allocation methods distribute shared costs for pricing, reporting, planning, and evaluation, but an allocated joint cost is an estimate rather than proof that a product caused that cost.

## Frameworks Introduced
- **Support allocation sequence**: Trace or distribute overhead, select each support department's driver, measure usage, compute proportions, allocate costs, then apply production-department costs to products.
- **Direct method**: Allocate each support department only to production departments; ignore inter-support services for simplicity.
- **Sequential/step-down method**: Allocate support departments in an order; recognize some inter-support service but do not allocate back to a closed department.
- **Reciprocal method**: Recognize all inter-support services simultaneously using equations; use when the extra accuracy justifies complexity.
- **Joint-cost allocation**: Allocate pre-split-off costs using physical units, weighted average, market value at split-off, or net realizable value (NRV).
- **Process-further decision**: Compare additional revenue after further processing with additional separable processing costs; ignore joint costs already incurred.

## Key Concepts
- **Support/service department**: Provides necessary services but does not directly make the product.
- **Cost driver**: Usage measure that reflects service consumption, such as square feet, employees, requisitions, or hours.
- **Joint cost**: Shared cost incurred before outputs become separately identifiable.
- **Split-off point**: The point where joint products become separately identifiable.
- **Separable cost**: Cost incurred after split-off that can be traced to an individual product.
- **By-product**: Low-value output of a joint process.

## Mental Models
- Direct -> sequential -> reciprocal is an accuracy ladder, not a mandatory hierarchy.
- The allocation denominator defines who may receive the current cost pool.
- Before split-off, costs are shared; after split-off, costs are product-specific.
- A cost assigned to a manager is not necessarily a cost controlled by that manager.

## Anti-patterns
- Including support departments in a direct-method denominator.
- Allocating sequential costs back to a department already closed.
- Allocating a department's costs to itself under the reciprocal method.
- Treating one joint-cost method as objectively true.
- Using allocated joint cost in a process-further decision.
- Ranking managers using allocated costs without a controllability analysis.

## Worked Example
Decker Tables has initial costs, in thousands, of Janitorial `$310`, Cafeteria `$169`, Cutting `$1,504`, and Assembly `$680`. Janitorial uses square feet; Cafeteria uses employees.

- **Direct**: Allocate Janitorial 20%/80% to Cutting/Assembly and Cafeteria 75%/25%. Final costs are Cutting `$1,692.75` and Assembly `$970.25`.
- **Sequential**: Allocate Janitorial first: 50% to Cafeteria, 10% to Cutting, 40% to Assembly. Revised Cafeteria is `$324`; allocate 75%/25% to production. Final costs are Cutting `$1,778` and Assembly `$885`.
- **Reciprocal**: Let `J = 310 + 0.20C` and `C = 169 + 0.50J`. Solving gives `J = 382`, `C = 360`; final production costs are Cutting `$1,758.20` and Assembly `$904.80`.

Total cost remains `$2,663`; only its distribution changes. For joint products, allocate a pool with `joint cost x product share`, where the share may be physical quantity, weighted quantity, split-off value, or NRV. Process further only if final value less separable cost exceeds split-off value.

## Key Takeaways
1. Choose a method by decision benefit relative to implementation cost.
2. Use drivers that reflect service usage or cost behavior.
3. Treat joint allocations as useful estimates, not causal facts.
4. Keep joint costs before split-off separate from separable costs after split-off.
5. Evaluate managers on controllable costs and decisions, not arbitrary shared allocations.

## Connects To
- **Ch 2-4**: Supplies support-allocation inputs for product-cost systems.
- **Ch 10**: Controllability determines whether allocated support costs belong in performance evaluation.
- **Ch 11**: Differential analysis supplies the process-further rule.
- **Ch 13**: Activity analysis can reveal waste hidden by broad allocations.

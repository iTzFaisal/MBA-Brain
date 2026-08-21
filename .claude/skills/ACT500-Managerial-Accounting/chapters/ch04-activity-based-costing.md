# Chapter 4: Activity-Based Costing

## Core Idea
Activity-based costing (ABC) assigns overhead through activities, activity cost pools, and activity bases instead of assuming that one broad volume measure explains all resource consumption. ABC is most valuable when products or customers consume setups, inspections, engineering, handling, or support activities in different proportions.

## Frameworks Introduced
- **Single plantwide rate**: Use when products consume overhead similarly and simplicity is valuable; divide total budgeted overhead by one plantwide base.
- **Multiple production-department rates**: Use when departments have different overhead patterns; calculate a rate for each production department.
- **Activity-based costing**: Identify activities, group costs into pools, select logical cost drivers, compute activity rates, and assign cost from usage.
- **ABC product-cost reduction**: Reduce cost by lowering activity-base usage, lowering the activity rate, eliminating activities, or redesigning the process.
- **ABC for services/customers**: Assign support activities such as orders, service requests, tests, or patient days to the users that consume them.

## Key Concepts
- **Activity**: A type of work that consumes resources.
- **Activity cost pool**: Costs grouped around a common activity.
- **Activity base/cost driver**: Measurable usage that explains activity cost.
- **Activity rate**: `Budgeted activity cost / estimated activity-base usage`.
- **Product-cost distortion**: Undercosting or overcosting created by an allocation base unrelated to resource consumption.
- **Value-added/non-value-added activity**: A process lens for finding work that should be reduced or eliminated.
- **Engineering change order (ECO)**: A document that initiates a design or process change.

## Mental Models
- Plantwide costing averages; departmental costing separates; ABC follows the work performed.
- Equal unit volume does not imply equal complexity or support cost.
- Every assigned activity cost is rate times usage.
- Cost distortion becomes strategy distortion when it drives prices, product mix, or discontinuation decisions.

## Anti-patterns
- Using a plantwide rate when products consume activities differently.
- Assuming departmental rates are automatically accurate.
- Assigning setup, inspection, or engineering costs using direct labor hours when usage is driven by counts.
- Choosing a convenient driver instead of a causal driver.
- Using managerial ABC allocations to manipulate GAAP inventory or external income.
- Cutting one activity without checking quality or total system cost.

## Worked Example
Ruiz makes 1,000 snowmobiles and 1,000 riding mowers. Both use 10,000 direct labor hours, but support usage differs.

| Activity | Pool | Base | Snowmobile usage | Mower usage |
|---|---:|---:|---:|---:|
| Fabrication | $530,000 | 10,000 DLH | 8,000 | 2,000 |
| Assembly | $70,000 | 10,000 DLH | 2,000 | 8,000 |
| Setup | $480,000 | 120 setups | 100 | 20 |
| Inspection | $312,000 | 104 inspections | 100 | 4 |
| ECOs | $208,000 | 16 ECOs | 12 | 4 |

Activity rates are `$53/DLH`, `$7/DLH`, `$4,000/setup`, `$3,000/inspection`, and `$13,000/ECO`. ABC assigns `$1,294` overhead per snowmobile and `$306` per mower. A plantwide rate assigns `$800` to each. The plantwide method undercosts the snowmobile by `$494` and overcosts the mower by `$494`, potentially leading to an underpriced complex product and an over-priced simple product.

## Key Takeaways
1. Select the simplest allocation method that is decision-useful.
2. Use activity drivers that reflect actual resource consumption.
3. Compare ABC with plantwide and departmental results to detect distortion.
4. Use ABC for pricing, product mix, customer profitability, and process redesign, not as a substitute for every external-reporting rule.

## Connects To
- **Ch 2-3**: Extends job and process cost-system logic.
- **Ch 5**: Uses the broader cost-allocation framework.
- **Ch 11**: Improves relevant cost and pricing analysis by reducing distortion.
- **Ch 13-14**: Supplies activity and operational measures for lean improvement and strategic scorecards.

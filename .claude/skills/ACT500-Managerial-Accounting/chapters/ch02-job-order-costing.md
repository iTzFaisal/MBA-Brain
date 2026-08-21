# Chapter 2: Job Order Costing

## Core Idea
A job order cost system accumulates direct materials, direct labor, and applied factory overhead for each identifiable job or batch. It fits custom products and unique service engagements. The job cost sheet links source documents to inventory, pricing, cost control, and profitability decisions.

## Frameworks Introduced
- **Job order cost system**: Use for custom or separately identifiable jobs; accumulate costs by job rather than by department.
- **Job cost sheet/subsidiary ledger**: Record direct materials, direct labor, and applied overhead for each job; the sheets support the Work in Process control account.
- **Predetermined factory overhead rate**: Use estimated annual overhead divided by estimated activity to price and control jobs before actual overhead is known.
- **Source-document chain**: Match receiving reports and supplier invoices; use materials requisitions for material issues and time tickets for job labor.
- **Perpetual manufacturing-cost flow**: Materials -> WIP -> finished goods -> COGS. Completed service jobs move to cost of services rather than finished goods.
- **Under/overapplied overhead check**: Actual overhead is debited to Factory Overhead and applied overhead is credited; the ending debit is underapplied and the ending credit is overapplied.

## Key Concepts
- **Direct materials**: Materials traceable to a job.
- **Direct labor**: Labor hours traceable to a job.
- **Factory overhead**: All manufacturing costs other than direct materials and direct labor.
- **Activity base**: A measure such as direct labor hours, direct labor cost, or machine hours used to apply overhead.
- **Applied overhead**: Job activity multiplied by the predetermined overhead rate.
- **Underapplied overhead**: Actual overhead exceeds applied overhead.
- **Overapplied overhead**: Applied overhead exceeds actual overhead.
- **Cost of services**: The expense recognized when a completed service engagement is delivered.

## Mental Models
- Trace what is economically traceable; allocate what is not.
- The job cost sheet is the job's cost passport: source documents become an auditable total and unit cost.
- The Factory Overhead account is an estimator check, not a measure of job-level actual overhead.
- Inventory status describes production status: WIP is incomplete, finished goods are complete but unsold, and COGS is sold.

## Anti-patterns
- Using job order costing for continuous, homogeneous production; use process costing instead.
- Charging indirect materials or indirect labor directly to jobs.
- Waiting until year-end to calculate overhead when managers need timely job costs.
- Treating applied overhead as actual overhead.
- Assuming an overhead credit balance is an accounting error.
- Carrying a material under/overapplied balance into the next year without disposition.
- Moving labor to a job or customer to manipulate a cost-plus price.

## Worked Example
Legend Guitars estimates factory overhead of `$50,000` and `10,000` direct labor hours, so the predetermined rate is `$5` per direct labor hour. Job 71 has beginning cost of `$3,000`, direct materials of `$2,000`, direct labor of `$3,500`, and `350` direct labor hours.

1. Applied overhead = `350 x $5 = $1,750`.
2. Total Job 71 cost = `$3,000 + $2,000 + $3,500 + $1,750 = $10,250`.
3. If the job produced 20 guitars, unit cost = `$10,250 / 20 = $512.50`.
4. If actual December overhead is `$4,600`, applied overhead is `$4,250`, and the opening Factory Overhead balance is a `$200` credit, the ending balance is a `$150` debit: `200 credit + 4,600 debit - 4,250 credit`.
5. Close underapplied overhead to COGS: `Dr COGS $150; Cr Factory Overhead $150`.

## Key Takeaways
1. Select job order costing when jobs are separately identifiable and economically different.
2. Use receiving reports, requisitions, time tickets, and job sheets to support assignments.
3. Apply overhead with a rational, predetermined activity driver.
4. Investigate large overhead balances and dispose of them at year-end.
5. Use unit-cost comparisons to diagnose waste, supplier quality, training, equipment, and pricing.

## Connects To
- **Ch 1**: Supplies product-cost and inventory foundations.
- **Ch 3**: Contrasts job-level accumulation with department-level process costing.
- **Ch 4-5**: Refines overhead and support-cost allocation.
- **Ch 6-11**: Supplies cost information for CVP, budgets, variance, responsibility, and differential decisions.

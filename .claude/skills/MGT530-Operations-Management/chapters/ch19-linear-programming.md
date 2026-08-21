# Chapter 19: Linear Programming

## Core Idea
Linear programming (LP) is a constrained-optimization method for allocating scarce resources among competing activities. A manager defines feasible combinations of decisions, then chooses the combination that maximizes profit, revenue, efficiency, or return, or minimizes cost, time, distance, or waste. LP is useful only when the model is a reasonable representation of the operating problem: relationships are linear, fractional decisions are acceptable, parameters are sufficiently certain, and negative activity levels make no sense. The quality of the recommendation therefore depends as much on identifying the right variables, restrictions, and data as on solving the equations.

## Frameworks Introduced
- **LP model formulation**: Define decision variables as controllable quantities; write one objective function; translate resource limits and minimum requirements into constraints; add parameter values and nonnegativity. A maximization model has the form `Maximize Z = c1x1 + ... + cnxn`, subject to constraints such as `a1x1 + ... + anxn <= b`, `>= b`, or `= b`, with `xj >= 0`.
- **Graphical LP procedure**: For two variables, formulate the model, replace each inequality by an equality to plot its boundary, find axis intercepts, use a test point to identify the feasible side, and intersect all restrictions. Plot an isoprofit or isocost line and slide it parallel until it reaches the last feasible point.
- **Corner-point and enumeration logic**: A bounded feasible region is a polygon, and a linear objective reaches an optimum at a corner point. Either slide the objective line graphically or calculate every corner and compare objective values. A constraint whose removal would not change the feasible region is redundant. If the objective line is parallel to a feasible boundary, every point on the touching segment is optimal.
- **Simplex and computer solution**: The simplex algorithm generalizes corner-point search to models with many variables. In spreadsheet Solver, place decision-variable cells in a worksheet, calculate the objective and left-hand sides, choose Max or Min, identify changing cells, enter each inequality, enforce nonnegative variables, and select the Simplex LP method. Inspect the answer and sensitivity reports rather than accepting a numerical result without checking the model.
- **Sensitivity analysis**: Test how changes in objective coefficients, right-hand-side (RHS) resource amounts, and constraint coefficients affect the recommendation. The range of optimality keeps the same decision quantities when an objective coefficient changes. The range of feasibility keeps an RHS shadow price valid when a resource amount changes. For simultaneous changes, divide each change by its allowable change in the relevant direction and require the sum of the positive fractions to be no more than `1.00`.

## Key Concepts
- **Decision variables**: The quantities the decision maker controls, such as units of products, assignments, shipments, or resource levels.
- **Objective function**: The linear score to optimize. Each coefficient is the per-unit profit, cost, time, or other contribution.
- **Constraint and RHS**: A restriction with coefficients showing resource use or required relationships and an RHS showing the available amount, minimum, or exact target.
- **Feasible solution space**: All combinations satisfying every constraint and nonnegativity. A feasible solution is not necessarily optimal.
- **Nonnegativity**: `xj >= 0`; negative production, shipments, or assignments are not meaningful.
- **Binding constraint**: A restriction exactly met at the optimum. Relaxing it could improve the objective, so it identifies a limiting resource. A nonbinding `<=` constraint has **slack**, `RHS - LHS`; a nonbinding `>=` constraint has **surplus**, `LHS - RHS`.
- **Shadow price**: The marginal change in the optimal objective value from a one-unit RHS change, valid only within its range of feasibility. A nonbinding constraint has shadow price zero.
- **Basic and nonbasic variables**: Basic variables are in the solution, usually with positive values; a nonbasic variable is at zero. Its reduced cost indicates how much its objective coefficient must improve before it can enter the solution.

## Mental Models
- **The model is an operating contract**: Every coefficient encodes an assumption. If demand, setup effects, overtime, integer requirements, or nonlinear economies matter, add them or use a method suited to them; do not hide them in a linear model.
- **The feasible region is the operating envelope**: Constraints define what can be done. The optimum is the point where the best objective direction first meets that envelope, usually where scarce resources intersect.
- **Slack is unused capacity; a shadow price is the value of capacity**: A binding resource deserves managerial attention. Compare its shadow price with the incremental cost of obtaining more resource, while respecting the stated range.
- **Sensitivity converts an answer into a decision rule**: Within a reported range, quantities or marginal values can be updated without resolving the whole model. Outside the range, the active constraints or optimal mix may change and the model must be solved again.

## Anti-patterns
- **Optimize a bad formulation**: A mathematically precise answer is operationally useless if a product, requirement, demand limit, or resource has been omitted.
- **Treat signs mechanically**: A `<=` availability limit, a `>=` minimum requirement, and an equality target have different feasible sides. Plot boundaries as equalities, then test a point.
- **Assume every constraint matters**: Redundant constraints and slack resources do not limit the current optimum, although they may matter after other changes.
- **Use sensitivity values outside their ranges**: A shadow price is not a permanent price, and an objective coefficient can leave its range of optimality. Recompute after a boundary is crossed.
- **Round fractional answers casually**: Divisibility is an LP assumption. If whole units are essential, rounding can violate constraints or lose optimality; use integer programming or validate the rounded plan.

## Worked Example
A computer assembler chooses daily quantities `x1` and `x2`:

```text
Maximize Z = 60x1 + 50x2
Subject to  4x1 + 10x2 <= 100   (assembly hours)
            2x1 + x2 <= 22       (inspection hours)
            3x1 + 3x2 <= 39      (storage cubic feet)
            x1, x2 >= 0
```

For the graphical solution, plot each constraint boundary using its intercepts, test the origin to select the feasible side, and retain their intersection in the first quadrant. The relevant corners are `(0,10)`, `(5,8)`, `(9,4)`, and `(11,0)`, plus the origin. Their profits are `$500`, `$700`, `$740`, `$660`, and `$0`, respectively. Therefore the optimum is `x1 = 9`, `x2 = 4`, with maximum profit `$740`.

At that plan, assembly use is `76`, leaving `24` hours of slack. Inspection uses all `22` hours and storage uses all `39` cubic feet; both are binding. Solving the inspection and storage equations simultaneously gives the optimal corner. The same result is obtained by enumeration or Solver.

Sensitivity interpretation: the type 1 profit coefficient can range from `$50` to `$100`, and type 2 from `$30` to `$60`, without changing quantities, although profit changes. Inspection has a shadow price of `$10` per hour, applicable over an RHS range of `18` to `26` hours. Storage is feasible over `33` to `43.5` cubic feet; assembly, being nonbinding, can fall from `100` to `76` before it becomes binding and has no upper limit in this solution. A one-hour inspection increase within range adds `$10` to profit; beyond the range, resolve the model.

## Key Takeaways
1. Formulation comes first: variables, objective, constraints, RHS values, and nonnegativity must reflect the real decision.
2. Graphical LP exposes the feasible region, objective direction, binding constraints, redundancy, and corner-point logic.
3. Simplex and Solver make the same logic usable for larger models, but managers must validate inputs and interpret reports.
4. Slack identifies unused capacity; surplus identifies excess over a minimum; binding constraints identify current bottlenecks.
5. Ranges of optimality and feasibility support controlled what-if analysis, while changes beyond those ranges require a new solution.

## Connects To
- **Capacity and bottleneck management**: Binding constraints and shadow prices identify which labor, material, machine, or storage increases can justify investment.
- **Product mix and production planning**: LP converts contribution margins and resource requirements into an optimal mix, schedule, shipment, or assignment plan.
- **Forecasting and managerial control**: Sensitivity ranges show how robust a plan is to changes in prices, demand, and available capacity; uncertainty beyond those ranges calls for revised data or scenario analysis.

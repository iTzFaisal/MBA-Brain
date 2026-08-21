# Chapter 6: Business Intelligence, Data Science, and Data Analytics

## Core Idea
Analytics creates value by moving from describing what happened to predicting what could happen and prescribing what to do. The strongest practice starts with a business decision, uses trustworthy and contextual data, combines algorithms with domain expertise, communicates results clearly, and monitors outcomes so models can be improved.

## Frameworks Introduced
- **Four phases of decision-making**: Use **intelligence** to identify the problem or opportunity, collect information, and establish goals and criteria; **design** to generate and evaluate feasible alternatives; **choice** to select an action; and **review** to monitor, control, and revisit earlier phases if the solution fails.
- **Three levels of data analytics**: **Descriptive data analytics** asks what happened and summarizes historical data; **predictive data analytics** asks what could happen and models unknown events; **prescriptive data analytics** asks what should be done and selects among actions under known constraints. Use the lowest level that answers the decision, then move upward when prediction or action is required.
- **Business Intelligence (BI) vs. Data Science**: Use BI for highly structured data, reporting, dashboards, and actionable views of current or historical performance. Use data science when structured, semi-structured, and unstructured big data must be combined with domain expertise, scientific methods, programming, algorithms, and statistics to predict and prescribe. BI often answers known questions; data science explores known unknowns and unknown unknowns.
- **Seven-stage decision science lifecycle**: (1) **capture** data and understand business requirements, (2) **store** and clean data securely, (3) **model** and evaluate algorithms, (4) **analyze** through exploratory and statistical methods, (5) **communicate** reports, visualizations, and decisions, (6) **deploy** and test in the real world with business buy-in, and (7) **reiterate** by monitoring KPIs and retraining when performance degrades.
- **Four Vs of Big Data**: Evaluate **Volume**, **Variety**, **Velocity**, and **Veracity** before claiming analytical value. The first three describe scale, forms, and speed; veracity asks whether data are authentic, available, trustworthy, cleansed, and complete.
- **Descriptive analytics toolkit**: Use **data mining** to find patterns, **data visualization** to make relationships understandable, **digital dashboards** to present current KPIs and alerts, and **data mashups** to combine internal, external, SaaS, and Web data into one interactive view.
- **Predictive and prescriptive methods**: Use **text mining and sentiment analysis**, **spatial data mining/GIS and geocoding**, **linear and time-series regression**, **decision optimization and rules-based decision-making**, and **machine learning**. Combine a forecast with optimization when constraints and trade-offs determine the best action.

## Key Concepts
- **Business intelligence (BI)**: Practices, software, infrastructure, and tools that transform structured data into actionable insight.
- **Data science**: A multidisciplinary field that extracts knowledge from structured, semi-structured, and unstructured big data to predict and prescribe.
- **Bounded rationality**: Decisions are limited by cognitive capacity, problem tractability, and available time.
- **Satisficing vs. optimizing**: Satisficing accepts the first acceptable solution; optimizing seeks the best achievable performance under constraints.
- **Advanced data analytics**: Predictive and prescriptive analysis beyond traditional BI.
- **Dashboard**: A graphical interface showing relevant KPIs, alerts, and metrics at a glance.
- **Data mashup**: Integration of data and applications from multiple sources without first loading everything into a warehouse.
- **Predictive model**: A statistical model using factors likely to influence future behavior.
- **Decision optimization**: Calculating variable values that produce the best outcome under constraints.
- **Machine learning**: Algorithms that identify patterns, predict outcomes, detect unexpected behavior, and improve from data.

## Mental Models
- Start with **decision first, data second**: define the action, criteria, and constraint before collecting every available field.
- Think of the analytics ladder as **describe -> predict -> prescribe**, with human judgment closing the loop.
- Keep the model proportionate. If a simple model meets the KPI and business constraints, extra complexity is not automatically value.

## Anti-patterns
- **Collecting big data without veracity**: More volume does not repair missing, duplicated, biased, or context-free data.
- **Dashboard theater**: Attractive charts without current KPIs, definitions, ownership, or a decision path do not improve performance.
- **Optimizing before defining the problem**: A precise solution to the wrong objective is still a failure.
- **Replacing domain expertise with software**: Algorithms need business context to select variables, interpret patterns, and act safely.
- **One-time model deployment**: Business conditions change; without KPI monitoring and retraining, performance decays.

## Worked Example
NASCAR faced shrinking attendance, falling television ratings, and the departure of major stars. It used big data and augmented reality to extend the live experience to fans who could not attend. The NASCAR mobile app offered a 3D burnout simulation using optimized offline video data, and the organization added live 360-degree streams from race cars. Apple, Google, an external development agency, and an internal team supplied platform and domain capabilities. The solution linked the business problem, customer experience, data design, visualization, and feedback rather than treating AR as a standalone gadget.

## Key Takeaways
1. Use intelligence, design, choice, and review to make analytics part of a disciplined decision process.
2. BI explains current performance; data science uses broader data and methods to predict and prescribe.
3. Validate all four Vs, especially veracity, before trusting a model or dashboard.
4. Use visualization and mashups to make insights accessible, but keep governance and definitions visible.
5. Combine predictive forecasts with optimization and rules when the decision has competing constraints.
6. Deploy, monitor, communicate, and reiterate; analytics is a lifecycle, not a report.

## Connects To
- **Chapter 2**: TPS, MIS, DSS, EIS, cloud, and architecture provide the analytical flow and computing capacity.
- **Chapter 3**: Warehouses, lakes, governance, and master data determine analytical quality.
- **Chapter 4**: IoT and edge computing supply high-velocity sensor data for real-time models.
- **Chapter 7**: Search, semantic technologies, and recommendation engines use analytics to personalize information.

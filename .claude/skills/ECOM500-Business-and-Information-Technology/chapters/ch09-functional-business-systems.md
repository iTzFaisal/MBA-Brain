# Chapter 9: Functional Business Systems

## Core Idea
Functional business systems (FBSs) improve the work of production and operations, sales and marketing, accounting and finance, and human resources. Their real value appears when they break data silos and connect end-to-end, cross-functional processes while preserving secure, valid, and accurate data.

## Frameworks Introduced
- **Four traditional functional business units**: Use the frame to assign process ownership and identify missing capabilities: production and operations; sales and marketing; accounting and finance; human resources.
  - How: Map each unit's processes, then identify where a transaction, decision, or customer outcome crosses departmental boundaries.
- **Cross-functional business system**: Use when an end-to-end process depends on two or more departments.
  - How: Connect the sales TPS and its order data to accounting, production, transportation, and customer support. Replace duplicated handoffs with shared data and coordinated workflows.
- **Production and operations management (POM) input-transformation-output model**: Use to optimize a service or production system.
  - How: Identify capital, people, facilities, materials, IT, information, time, and energy as inputs; inspect, alter, transport, or store them; then measure the value-added goods or services produced.
- **Economic order quantity (EOQ) model**: Use when deciding when and how much inventory to order.
  - How: Balance inventory carrying costs, ordering costs, and the cost of shortages rather than minimizing inventory blindly. The source names the model but does not provide its equation.
- **Principles of Lean Management**: Use to remove work that does not add customer value.
  - How: **Value**, **Map Value Stream**, **Create Flow**, **Establish Pull**, and **Seek Perfection**. Repeat the cycle and empower people closest to the process to improve it.
- **Just-in-Time (JIT) inventory management**: Use in repetitive operations with reliable suppliers and accurate, timely usage data.
  - How: Receive inventory when it is needed, reduce carrying costs and waste, and accept more frequent ordering and greater stockout exposure.
- **Five activities of financial planning and budgeting**: Use to connect financial control to business decisions: budgeting, forecasting, financial ratio analysis, profitability analysis, and cost control.
  - How: Use integrated data to compare planned and actual performance, model cash needs, evaluate capital investments, and locate cost and profit drivers. The source defines `profit margin = sale price - cost of good`.

## Key Concepts
- **Functional business system (FBS)**: An information system designed to improve efficiency and performance in a specific functional area.
- **Cross-functional business process**: Departments working together toward a shared business outcome.
- **Standard operating procedure (SOP)**: Written instructions that reduce variation and support consistent execution.
- **Data security**: Protection against corruption, unauthorized modification, theft, or natural causes.
- **Data validity**: Tests and evaluations that detect and correct input errors.
- **Data integrity**: Maintaining data accuracy and validity throughout its life cycle.
- **Safety stock**: Buffer inventory held to reduce stockout risk.
- **Quality management system (QMS)**: A documented system of processes and responsibilities for consistent quality, assurance, control, and improvement.
- **Manufacturing execution system (MES)**: A real-time system that manages shop-floor work, bills of materials, scheduling, work in progress, lots, and work orders.
- **eXtensible Business Reporting Language (XBRL)**: A standards-based language that tags financial data so software can search, compare, validate, and exchange it.

## Mental Models
- **Function, process, enterprise**: Start with specialized expertise, then follow the data across the customer or product process. A functional optimization that harms the whole flow is not an improvement.
- **Inventory is a three-cost trade-off**: Lower carrying cost can increase ordering cost or shortage cost. Select EOQ, JIT, or safety stock from demand and supplier reliability.
- **HR is a lifecycle, not a hiring event**: Use HRIS across planning, recruiting, developing, deploying, retaining, and assessing people.

## Anti-patterns
- **Protecting functional data silos**: Marketing cannot evaluate pricing or promotion if sales and accounting data are inaccessible or unusable.
- **Using JIT without resilient partners**: Strikes, bad weather, quality failures, or poor communication can stop the entire chain.
- **Optimizing cost while ignoring customer value**: POM must improve service and customer value, not only manufacturing cost or product quality.
- **Treating compliance as a report at the end**: Use controls, audit trails, XBRL, and updated regulatory systems throughout the process.
- **Relying on one person or informal control**: Document SOPs and separate duties to preserve data and prevent fraud.

## Worked Example
**MAHLE and SAP Transportation Management.** MAHLE lacked visibility into shipping efficiency and costs, had short planning horizons, and used resources poorly across its global automotive network. With SAP and MHP, it implemented SAP TM to manage inbound and outbound freight in one environment and expose orders, shipments, items, and logistics processes. Results included a transport cockpit, a six-week planning horizon, almost doubled inbound load-capacity use, and significantly lower inbound transfer costs. The lesson is to select a cross-functional system that exposes the process, not merely another departmental application.

## Key Takeaways
1. FBSs are the foundation for enterprise systems, but cross-functional integration is where business value compounds.
2. Preserve security, validity, and integrity as explicit data requirements.
3. Use EOQ and JIT as context-dependent trade-offs, not universal inventory rules.
4. Lean management removes non-value work through value-stream visibility, flow, pull, and continuous improvement.
5. QMS, CIM, MES, TMS, financial planning systems, XBRL, and HRIS turn routine work into measurable, auditable processes.
6. Use technology to improve decisions and collaboration while keeping managers accountable for interpretation and control.

## Connects To
- **Chapter 3**: Data management, data governance, and dirty-data prevention support trustworthy FBS data.
- **Chapter 5**: Security, controls, and regulatory compliance protect functional systems.
- **Chapter 8**: Omnichannel retail depends on sales, inventory, logistics, finance, and customer data working together.
- **Chapter 10**: ERP, SCM, and CRM extend functional systems across the enterprise.
- **Chapter 13**: Systems development and project management govern implementation and process change.
- **Chapter 14**: Ethical controls and sustainable operations depend on accountable functional systems.

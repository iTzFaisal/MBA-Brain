# Chapter 2: Information Systems, IT Infrastructure, and the Cloud

## Core Idea
An information system (IS) is the coordinated combination of technology and people's activities that supports processes, operations, management, and decisions. Value depends on matching the system level, architecture, data, and delivery model to the business problem while balancing scalability, control, security, and cost.

## Frameworks Introduced
- **IPOS cycle**: Use **Input -> Processing -> Output -> Storage**, with **feedback** from users and performance metrics, to diagnose an IS. Input captures data, processing manipulates it, output presents results, storage preserves them, and feedback improves future performance.
- **Six components of an IS**: Check every system for **hardware, software, people, procedures, network, and data**. Data is central; the other components collect, process, secure, communicate, and use it.
- **Data, Information, Knowledge, and Wisdom model**: Move from raw data to meaningful information (who, what, where, when), add experience to create knowledge (how), and apply values, ethics, and judgment to produce wisdom (why). Use this model when a report exists but a decision still does not.
- **IS hierarchy**: Use a **transaction processing system (TPS)** at the operational level to capture transactions; a **management information system (MIS)** at the middle-management level for structured, periodic or exception reports; a **decision support system (DSS)** for semistructured decisions, models, what-if analysis, goal seeking, and risk analysis; and an **executive information system (EIS)** for C-level trend analysis and unstructured strategic decisions. Real-time processing keeps balances current; batch processing is cheaper but temporarily less current.
- **Enterprise architecture (EA)**: Use EA as the conceptual blueprint connecting strategy, information, processes, and IT assets. Build from business, application, information, and technology perspectives. Describe the baseline architecture, target architecture, and sequencing plan, then update the plan as business priorities change. Evaluate it with capability, operational, project, and financial KPIs.
- **Cloud and Anything-as-a-Service (XaaS)**: Select the service layer that fits the need: **software as a service (SaaS)**, **platform as a service (PaaS)**, **infrastructure as a service (IaaS)**, **data as a service (DaaS)**, or **technology solutions as a service (TSaaS)**. Use public clouds for shared, scalable resources; private clouds when control and regulation require a single-tenant environment.
- **Virtualization**: Use a virtualization layer to separate applications and data from physical hardware, pool underused resources, and run multiple virtual machines (VMs) on fewer physical servers. Storage, server, desktop, application, network, and hardware virtualization are distinct forms.

## Key Concepts
- **Information system (IS)**: Technology plus human activities supporting business processes and decision-making.
- **Data**: Raw or unorganized facts and figures.
- **TPS/MIS/DSS/EIS**: The operational-to-strategic progression from transactions to wisdom.
- **IT infrastructure**: The inventory of physical IT devices, facilities, networks, software, and data centers owned or operated by an organization.
- **IT architecture**: Policies and a blueprint guiding the planning, acquisition, building, modification, interfacing, and deployment of IT resources within a department.
- **Data center**: Networked servers and facilities used for storage, processing, and distribution of data.
- **Software-defined data center (SDDC)**: A unified, software-managed infrastructure that dynamically provisions compute, storage, networking, and security.
- **Cloud service agreement (CSA)**: A negotiated agreement defining service expectations, responsibilities, performance, security, recovery, remedies, and termination.
- **Virtual machine (VM)**: A software-created computer with virtual CPU, RAM, storage, and network interface behavior.

## Mental Models
- Choose an IS by the **decision structure**: automate repeatable transactions, report patterns, model alternatives, then apply executive judgment.
- Think of EA as a **city plan**, not a static diagram. The baseline is where the organization is, the target is where it needs to go, and sequencing controls the transition.
- Cloud is a **cost-versus-control trade-off**. Scalability and agility rise as the provider takes on more management; legal, security, performance, and vendor dependence must be explicit.

## Anti-patterns
- **Calling an asset inventory an architecture**: Infrastructure lists what exists; architecture guides future choices; EA aligns all of it to strategy.
- **Using MIS for questions it cannot answer**: Scheduled, structured reports do not replace a DSS model for ad hoc what-if decisions.
- **Treating EA as static**: A fixed blueprint becomes misaligned as business goals, applications, regulations, and cloud options change.
- **Moving to cloud without governance**: A provider does not remove the customer's duties for privacy, compliance, recovery, vendor management, or measurable service levels.
- **Keeping one physical server per application**: Dedicated hardware creates low utilization, unnecessary cost, and poor flexibility when workloads fluctuate.

## Worked Example
California Pizza Kitchen initially used an MIS for financial and restaurant information, but managers needed current, ad hoc inventory reports for daily ordering. The MIS was too inflexible, so CPK replaced it with a DSS that allowed on-demand reports and updated inventory decisions at corporate and restaurant levels. Many restaurants reported a 5% sales increase. The decision followed the IS hierarchy: a TPS supplies transaction data, while a DSS adds models and flexible questions for a less structured operational decision.

## Key Takeaways
1. An IS succeeds only when its six components and human users work together around reliable data.
2. Use the IPOS cycle and feedback to find where an information flow breaks down.
3. Match TPS, MIS, DSS, or EIS to the structure and time horizon of the decision.
4. Use EA to align departmental technology choices with enterprise direction and measurable KPIs.
5. Select cloud and virtualization for business agility, but contract for security, recovery, performance, and exit.

## Connects To
- **Chapter 1**: Digital business models depend on scalable infrastructure and architecture.
- **Chapter 3**: Databases, warehouses, governance, and data quality supply the IS hierarchy.
- **Chapter 4**: Networks provide the connectivity, bandwidth, and protocols that cloud services require.
- **Chapter 5**: Cloud, virtualization, and IS controls expand the security and privacy responsibility.
- **Chapter 6**: DSS, EIS, BI, and data science build on the flow from operational data to insight.

# Chapter 3: Data Management, Data Warehouses, and Data Governance

## Core Idea
Data becomes a strategic asset only when the organization can find it, trust it, protect it, interpret it, and retire it appropriately. Data management connects transactional systems, analytical stores, governance, master data, information practices, and document or record controls across the full data lifecycle.

## Frameworks Introduced
- **Data lifecycle and data principles**: Track data from sources and databases to storage, analysis, results, and business applications. Apply the **principle of diminishing data value** (older data usually becomes less useful), the **principle of 90/90 data use** (up to 90% of stored data is seldom accessed after 90 days except for audit), and the **principle of data in context** (integrate, process, analyze, and format data into actionable information).
- **Data ACID Test**: Use **Atomicity, Consistency, Isolation, and Durability** for database transactions. Atomicity commits all changes or none; consistency preserves integrity; isolation prevents concurrent transactions from interfering; durability makes a committed transaction permanent.
- **Database-to-analytics pipeline**: Use **extract, transform, and load (ETL)** to extract selected data, clean and standardize it, integrate it, and load it into a data warehouse or data mart. Use **change data capture (CDC)** to propagate only source changes and **data deduplication** to remove duplicates and standardize formats. Use databases for fast OLTP; use warehouses and marts for OLAP and complex analysis; use a data lake when raw structured, semi-structured, and unstructured data must be retained before requirements are known.
- **Blockchain distributed ledger**: Use blockchain when multiple parties need a shared, tamper-evident history without one administrator. Each block contains transaction data, a timestamp, its hash, and the previous block's hash. A peer-to-peer network, proof-of-work, consensus, and smart contracts reinforce trust and automation.
- **Data governance and Master Data Management (MDM)**: Establish a governing body, formal procedures, and an execution plan so data availability, usability, integrity, and security are controlled. Use MDM to link dispersed customer, product, supplier, employee, location, and asset records into a **Master Reference File** that feeds consistent data back to applications.
- **Confidence in Data-Dependent Assumptions (CIDDA)**: Use CIDDA to make the value of governance visible and track improvement. The exact formula is `CIDDA = G * M * TS`, where `G` is confidence that data are good enough for their purpose, `M` is confidence that data mean what users think they mean, and `TS` is confidence in the source.
- **Framework for Generally Accepted Recordkeeping Principles**: Use its eight principles for electronic records: **accountability, transparency, integrity, protection, compliance, availability, retention, and disposition**.

## Key Concepts
- **Database management system (DBMS)**: Software that defines, stores, retrieves, validates, secures, synchronizes, and manages data.
- **OLTP vs. OLAP**: Online transaction processing favors fast operational changes; online analytics processing favors complex warehouse analysis.
- **Centralized vs. distributed database**: Centralization simplifies control and integrity; distribution improves local speed, availability, and scalability but adds network, expense, and security complexity.
- **Relational data model**: Tables of rows and columns related through common fields.
- **NoSQL**: Non-relational, schema-flexible databases suited to distributed, very large, unstructured or unpredictable data; they trade among consistency, availability, and partition tolerance under the CAP theorem.
- **Data warehouse/data mart**: An integrated analytical repository versus a smaller, function-specific version.
- **Data governance**: Enterprise-wide control of data availability, usability, integrity, and security.
- **Dirty data**: Incomplete, outdated, incorrect, duplicated, conflicting, nonstandardized, or unusable data.
- **EDMS/ERMS/ECMS**: Systems for living documents, finalized records and retention, and the broader management of structured and unstructured content.

## Mental Models
- Think **operational truth vs. analytical truth**: a live transaction database optimizes current execution; a cleansed warehouse optimizes comparison, trend, and decision support.
- Apply **garbage in, garbage out (GIGO)** before trusting an impressive model or dashboard.
- Treat master data as the stable reference layer between changing transactions and analytical decisions.

## Anti-patterns
- **Loading dirty data into a warehouse or lake without a quality plan**: Scale multiplies errors and gives bad decisions an appearance of precision.
- **Using an OLTP database for heavy analytics**: Constant updates create volatility and consume the processing capacity needed for transactions.
- **Allowing departmental data silos**: Unshared, inconsistent copies force users to verify data instead of analyzing it.
- **Managing records like editable documents**: Final records need original-format retention, access control, schedules, and secure disposition.
- **Treating governance as an IT-only project**: Data crosses functions, so ownership, policy, culture, and executive sponsorship are required.

## Worked Example
ThyssenKrupp Elevator processed roughly 700 documents for each elevator and almost one million documents per year. Paper red folders, email attachments, nine-level shared folders, long paths, and inconsistent names caused lost files, duplicates, version problems, delays, and about $25,000 per month in shipping. A cross-functional team mapped the process and implemented M-Files. Metadata such as job number, branch, customer, type, and date made content searchable by what it was rather than where it was stored. Automated workflows assigned and approved drawings, tracked deadlines, replaced more than 13 physical handoffs, and improved visibility. The case shows that metadata, workflow, governance, and content management must be redesigned together.

## Key Takeaways
1. Manage data end to end: create, store, use, protect, archive, and dispose.
2. Use ACID for transaction integrity and ETL/CDC for dependable analytical data movement.
3. Choose databases, warehouses, marts, lakes, or blockchain according to workload, structure, trust, and governance needs.
4. MDM creates a common reference for business entities and reduces inconsistent customer or product views.
5. Quantify data quality and governance; the cost of prevention is lower than the cost of repeated correction.
6. Separate living documents, legally retained records, and broader enterprise content.

## Connects To
- **Chapter 2**: EA, infrastructure, and cloud choices determine how data stores are integrated and governed.
- **Chapter 4**: Sensors and networks create the high-volume, high-velocity data that require lifecycle controls.
- **Chapter 5**: Governance, retention, access, and encryption support privacy and cyber defense.
- **Chapter 6**: BI and advanced analytics depend on timely, clean, contextual data.
- **Chapter 7**: Search, semantic technologies, and recommendation engines depend on metadata and trustworthy master data.

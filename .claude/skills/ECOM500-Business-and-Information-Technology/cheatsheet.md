# Cheatsheet

## If/then rules

| If you see... | Prefer... | Because / watch for... |
|---|---|---|
| A slow, handoff-heavy process | BPR before automation | "Don't automate, obliterate!"; redesign the flow first. |
| A transaction, report, what-if, or strategic question | TPS, MIS, DSS, or EIS respectively | Do not use a scheduled MIS report as a DSS model. |
| Live updates vs. complex comparisons | OLTP vs. warehouse/OLAP | Protect transaction performance; govern the analytical copy. |
| Urgent local action or costly/unreliable links | Edge first, cloud second | Filter locally; send relevant results for broad analysis/storage. |
| A cyber control proposal | Calculate `P1 * P2 * L`, then run BIA | Expected loss is not the full regulatory, reputation, continuity, or recovery cost. |
| A dashboard request | Define the decision and KPI owner first | If no action follows the chart, it is dashboard theater. |
| A need to predict or choose action | Move descriptive -> predictive -> prescriptive | Use the lowest complexity that answers the decision; verify Four Vs, especially Veracity. |
| Customers switch channels | Build omnichannel shared context | Coordinate identity, price, inventory, payment, fulfillment, service, and returns. |
| A system touches multiple functions | Evaluate enterprise integration | Select ERP/SCM/CRM/EKM/ECM/ESP by process need, fit, TCO, and adoption. |
| An AI proposal has no data, owner, or explanation path | Stop at a bounded POC | Advance through Gartner maturity stages only after production evidence. |
| A vendor promises savings or uptime | Require POC, TCO, SLA, transition, and exit terms | A demo is not a governed operating relationship. |
| Requirements are stable vs. volatile | Waterfall vs. Agile/DevOps | Do not use sequential delivery when late discovery is likely. |
| A change affects scope, time, or cost | Revisit all three and quality; rebaseline if approved | Never hide scope creep in an unchanged plan. |
| Tracking, automation, AI, or surveillance is proposed | Name responsibility, accountability, liability; test profits/people/planet | Consent, civil rights, accessibility, job impact, and lifecycle emissions are requirements. |

## Defaults, formulas, and thresholds

- `Expected loss = P1 * P2 * L`; compare the control's cost and effectiveness, then add qualitative BIA impacts.
- `CIDDA = G * M * TS`; a weak factor makes overall confidence weak. Do not let a polished dashboard hide low confidence.
- The **90/90 data principle** is a storage signal: up to 90% of data may be seldom accessed after 90 days, except for audit. Confirm retention obligations before archiving or disposing.
- Use **ACID** for transaction integrity; use ETL/CDC, deduplication, and MDM for analytical consistency.
- Use public cloud for shared scale and private cloud for stronger control or regulatory isolation; contract security, recovery, performance, and exit.
- Use supervised ML when labeled answers exist, unsupervised ML for pattern discovery, and reinforcement learning for reward-based trial and error.
- Retain a customer when CLV, not a vanity loyalty metric, exceeds acquisition, service, return, and promotion costs.

## Tells and smells

- Technology is being selected before the business need, workflow, customer promise, or data owner is named.
- A new platform preserves the old forms, handoffs, silos, or local metrics.
- "Big data" has volume but no veracity, context, access control, retention plan, or decision owner.
- Security is password-only, compliance-only, or waiting for detection after a breach.
- An AI result is accurate but cannot be explained in a regulated or high-impact decision.
- A retailer has separate customer histories, prices, inventory, or returns by channel.
- A project reports green status while scope changes, risks, training, testing, or stakeholder objections remain hidden.
- Sustainability counts device electricity but ignores manufacturing, data centers, networks, use, and disposal.

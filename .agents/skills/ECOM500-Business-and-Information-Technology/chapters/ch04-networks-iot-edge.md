# Chapter 4: Networks, the Internet of Things (IoT), and Edge Computing

## Core Idea
Networks are business infrastructure for communication, search, mobility, collaboration, and relationships. Mobile devices and sensors extend that infrastructure into the physical world; edge computing then moves time-sensitive processing close to where data is produced so organizations can respond faster with less traffic and cost.

## Frameworks Introduced
- **Five basic business functions of computer networks**: Evaluate a network by its support for **communication**, **search**, **mobility**, **collaboration**, and **relationships**. A network should also enable file/resource sharing, data protection, streamlined administration, internal communication, and distributed computing power.
- **Network scope and access model**: Use a **LAN** for a limited area under one owner, a **WAN** to connect geographically dispersed LANs, and an **SD-WAN** to select optimal paths across public or private links from a central application. Use an intranet for internal collaboration, an extranet for authorized partners, and a **virtual private network (VPN)** to encrypt traffic across an untrusted network.
- **TCP/IP layered protocol suite**: Use its four layers to reason about communication: **Application**, **Transport**, **Network (Internet)**, and **Data Link (Network Interface)**. TCP reliably segments and retransmits; UDP sends with less overhead; IP routes packets to an address. APIs provide reusable functions and protocols for connecting applications, services, and business assets.
- **IoT data movement model**: Design the flow as **collect at sensors -> aggregate and prepare -> transmit over a network -> analyze with software -> store to comply with regulations -> generate reports, KPIs, and business insights**. Before buying technology, specify data type, source, volume, transfer speed, reliability, timeliness, analysis, compliance, storage location, and retention period.
- **Edge computing architecture**: Use local device or edge processing, optional fog nodes, and cloud or data-center storage. Filter, analyze, and compress data near the source; send the smaller, relevant result to the cloud. This is appropriate for latency-sensitive workloads, high bandwidth costs, unreliable connectivity, or safety-critical local decisions.
- **Quality of Service (QoS) models**: Use **Integrated Services (IntServ)** with resource reservation and guaranteed or controlled-load service for smaller private networks. Use **Differentiated Services (DiffServ)**, which marks packets by service class without maintaining every flow, for large networks such as the Internet. QoS prioritizes latency-sensitive traffic and throttles traffic that can wait.
- **Technology assessment**: Use the five-step cycle before replacing equipment: (1) analyze workflow, (2) inventory and review existing technology, (3) generate recommendations, (4) research products and vendors, and (5) repeat as business needs change.

## Key Concepts
- **Bandwidth and bps**: Capacity is the maximum bits per second a medium can transmit; actual speed depends on traffic, devices, noise, and server use.
- **Packet switching**: Breaks messages into packets, routes them independently, and reassembles them at the destination; it is more efficient for digital traffic than circuit switching.
- **Router, switch, hub, and NIC**: A router chooses paths between networks, a switch connects devices efficiently, a hub broadcasts to connected segments, and a network interface card connects a device.
- **IPv4/IPv6**: IPv4 uses a 32-bit address space (`2^32`, roughly 4.3 billion); IPv6 uses 128 bits (`2^128`) and supports vastly more devices.
- **4G/5G**: 4G LTE-A is widely deployed and packet-based; 5G increases speed, capacity, device density, and response time but needs new infrastructure and devices.
- **QR code/RFID/NFC**: Technologies for scanning, contactless identification and tracking, and short-range two-way communication.
- **Internet of Things (IoT)**: Connected physical objects with electronics, software, sensors, and network connectivity that collect and exchange data.
- **Quality of Service and Net Neutrality**: QoS manages traffic priorities; Net Neutrality is the principle that legal Internet traffic should receive equal access without unfair fast or slow lanes.

## Mental Models
- Think of a network as a **business value chain**, not as plumbing: every delay can affect a customer, decision, relationship, or safety outcome.
- Use **edge for urgent local action** and cloud for broad analysis, sharing, and long-term storage.
- Match QoS to consequences: protect voice, video, control, and safety traffic before bulk transfers.

## Anti-patterns
- **Centralizing every raw sensor event in the cloud**: It increases latency, bandwidth cost, congestion, and dependence on connectivity.
- **Deploying IoT before defining the data and governance questions**: Devices may generate data that cannot be trusted, analyzed, secured, or retained appropriately.
- **Confusing bandwidth with service quality**: More capacity does not by itself solve latency, packet loss, uptime, or prioritization problems.
- **Buying technology before studying workflow**: A technically impressive device can preserve the same bottleneck and fail to improve the business process.

## Worked Example
Cedar Park, Texas replaced drive-by water readings collected twice a month with digital meters and a FlexNet Advanced Metering Infrastructure communication network. Encrypted readings reached the utility database, while a secure portal gave customers near-real-time usage, comparisons, threshold alerts, vacation alerts, and leak notifications every four hours. Alerts identified leaks ranging from 20 to 300 gallons per hour, saving customers money and conserving water. The network improved billing accuracy and customer transparency because sensing, secure transmission, analytics, and a usable interface were designed as one service.

## Key Takeaways
1. Judge network investments by the five business functions they improve, not only by technical speed.
2. Use standards, IP addressing, APIs, and layered protocols to make heterogeneous devices interoperable.
3. 5G and IoT expand opportunity while also expanding endpoint, privacy, and security exposure.
4. Use QR, RFID, NFC, IoT, and edge only after clarifying the workflow and decision they support.
5. QoS makes network performance measurable and aligned with business priorities.

## Connects To
- **Chapter 2**: Cloud, data centers, virtualization, and EA provide the networked infrastructure.
- **Chapter 3**: IoT data must be cleaned, stored, governed, and placed in context.
- **Chapter 5**: Every connected device is an attack surface requiring layered controls.
- **Chapter 6**: IoT streams become useful through BI, predictive models, and prescriptive action.

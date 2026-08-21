# Chapter 5: Data Privacy and Cyber Security

## Core Idea
Data privacy and cyber security are business, governance, and continuity responsibilities, not isolated technical functions. Protect personal information and critical assets by recognizing threats, quantifying exposure and impact, selecting proportionate controls, and layering people, processes, technology, and recovery capabilities.

## Frameworks Introduced
- **Four data privacy concerns and the Privacy Paradox**: Ask how data are **shared with third parties**, **collected and stored**, **used**, and **regulated**. The **privacy paradox** is the disconnect between how important people say online privacy is and how they actually behave. Use it to identify consent, transparency, and user-behavior gaps.
- **Cyber risk and cost-benefit analysis**: A cyber risk exists when a threat exploits a vulnerability; the source gives `risk = cyber threat * vulnerability`. For a particular attack, calculate `Expected loss = P1 * P2 * L`, where `P1` is probability of attack, `P2` is probability of success, and `L` is loss if successful. Use risk assessment for quantitative exposure and **business impact analysis (BIA)** for operational and financial consequences and recovery priorities.
- **Cyber Defense Strategies**: Use six complementary strategies: **prevention and deterrence**, **detection**, **containment**, **recovery**, **correction**, and **awareness/compliance**. Prevention is preferable, but detection and containment reduce damage when prevention fails; correction prevents recurrence.
- **Risk mitigation strategies**: Choose **acceptance** when low-probability exposure is tolerable, **avoidance** when exposure can be eliminated, **limitation** when controls reduce exposure, or **transference** when a willing third party assumes part of the risk. Match the choice to asset value and consequences.
- **IT Security Defense-in-Depth Model**: Build redundancy across perimeter, network, host, application, and data layers. The four steps are: (1) gain senior management commitment and support, (2) develop acceptable use policies and IT security training, (3) create and enforce IT security procedures, and (4) implement and maintain hardware and software defenses.
- **General and application defense controls**: The five general controls are **physical**, **access**, **data security**, **communication**, and **administrative**. The eight application controls are **completeness**, **validity**, **authentication**, **authorization**, **input controls**, **availability**, **whitelisting**, and **blacklisting**.
- **Enterprise Risk Management (ERM) Framework and COBIT 2019**: ERM uses eight components: internal environment, objective setting, event identification, risk assessment, risk response, control activities, information and communication, and monitoring. COBIT 2019 aligns IT governance, security, and risk with business objectives through 40 governance and management objectives, six governance-system principles, three governance-framework principles, and seven components.

## Key Concepts
- **Data privacy**: The right to determine what information about a person is accessible, to whom, when, and for what purpose.
- **Personally identifiable information (PII)/protected health information (PHI)**: Data whose exposure can identify a person or reveal protected medical information.
- **Cyberattack/cyber threat**: An actual attempt to expose, alter, disable, destroy, steal, or gain unauthorized access, and the method used to do so.
- **Vulnerability/attack vector**: A security gap and the path used to exploit it.
- **Unintentional threats**: Human error, environmental hazards, and computer system failures.
- **Intentional threats**: Hacking, social engineering and phishing, malware, botnets, ransomware, cryptojacking, SQL injection, man-in-the-middle attacks, denial-of-service attacks, insider threats, physical theft or loss, and miscellaneous errors.
- **Zero-day/advanced persistent threat (APT)**: An exploit unknown to the organization until attack, versus a prolonged targeted intrusion that remains undetected while stealing information.
- **Shadow IT/BYOD/social media exposure**: Unapproved apps, personal devices, and social platforms that bypass enterprise controls or provide attack paths into the network.
- **IT resilience/business continuity**: The ability to protect data and apps from planned or unplanned disruption and maintain or rapidly restore essential functions.

## Mental Models
- Use **defense in depth**: assume any one control can fail, then make the next layer slow, detect, contain, or block the attack.
- Treat people as both an attack surface and a control. Training, acceptable-use policies, separation of duties, and incident response matter as much as firewalls.
- Protect the highest-value assets first. Do not spend equally on everything; compare probability, exposure, impact, control cost, and effectiveness.

## Anti-patterns
- **Password-only security**: Reused credentials, phishing, and weak authentication defeat a single layer; use multifactor authentication, authorization, monitoring, and encryption.
- **Assuming antivirus is complete protection**: Signature-based tools may not recognize zero-day malware or variants.
- **Uncontrolled BYOD or shadow IT**: Personal devices and cloud apps can bypass authentication, encryption, access control, and monitoring.
- **Delayed detection and disclosure**: Long undetected breaches multiply investigation, notification, reputation, regulatory, and customer costs.
- **Treating compliance as the whole security program**: Compliance is a baseline; resilience, testing, training, and business continuity must continue.

## Worked Example
For a hypothetical attack, an organization estimates a 2% probability of attack, a 10% probability that the attack succeeds, and a $1,000,000 loss if successful. The expected loss is `0.02 * 0.10 * $1,000,000 = $2,000`. That number can be compared with the cost of a control, but it is not the whole BIA: lost business, customer backlash, investigation, notification, post-breach response, reputation, and intellectual property may be harder to quantify. Marriott's four-year reservation-system breach illustrates why an apparently manageable technical exposure can create large strategic and regulatory consequences.

## Key Takeaways
1. Privacy requires control over collection, storage, sharing, use, and regulation, not only encryption.
2. Calculate risk and expected loss, then add qualitative business impacts through a BIA.
3. Use prevention, detection, containment, recovery, correction, and awareness together.
4. Layer general controls, application controls, governance frameworks, and trained people.
5. Assume mobile, cloud, social, and IoT connectivity expands the attack surface.
6. Test recovery and continuity before a crisis; resilience is an operating capability.

## Connects To
- **Chapter 2**: Cloud, virtualization, and IS architecture introduce control, vendor, and access decisions.
- **Chapter 3**: Data governance, retention, records, and master data support privacy and compliance.
- **Chapter 4**: Networks and IoT create endpoints, communications paths, and critical infrastructure exposure.
- **Chapter 6**: Analytics can improve detection but also magnify the consequences of poor or unlawfully used data.
- **Chapter 7**: Social platforms create both customer value and privacy, identity, and disinformation risk.

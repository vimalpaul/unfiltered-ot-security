---
title: "OT Security Glossary, Master Index and Knowledge Architecture"
document_id: "UOTS-20-GLOSSARY"
version: "1.0"
status: "Core reference and navigation standard"
owner: "Unfiltered OT Security"
created: "2026-11-17"
last_reviewed: "2026-11-17"
review_due: "2027-02-17"
scope: "Terminology, acronym dictionary, cross-chapter navigation, knowledge relationships and repository governance"
classification: "Public"
---

# OT Security Glossary, Master Index and Knowledge Architecture

**Document ID:** UOTS-20-GLOSSARY | **Version:** 1.0 | **Status:** Core reference and navigation standard

**Audience:** OT security professionals, industrial engineers, operators, researchers, consultants, auditors, students, AI knowledge system designers and repository contributors.

> **Terminology notice:** Definitions in this glossary are concise educational descriptions, not substitutes for definitions in applicable laws, contracts, licensed standards or vendor documentation. Where a term has multiple meanings, context is stated. Verify the edition and authoritative source before using a definition in a compliance or engineering decision.

# 1. Purpose

This chapter is the navigation and terminology layer for Unfiltered OT Security. It connects technical, regulatory, operational, research and governance content through consistent terms, identifiers and cross references.

It provides:
1. A shared vocabulary for OT, ICS, SCADA, industrial cybersecurity and safety.
2. Navigation from a term to its relevant technical chapter.
3. Relationships between assets, protocols, threats, vulnerabilities, controls, evidence and use cases.
4. A consistent method for adding, reviewing and retiring knowledge.
5. A foundation for search, graph navigation and AI-assisted retrieval while preserving source provenance.

# 2. How to use this chapter

- Search the glossary for the term or acronym.
- Follow the related chapter reference for technical detail.
- Check the source register and authoritative publisher for formal definitions.
- Check standards edition and jurisdiction before treating a term as a requirement.
- Use master indexes to navigate by asset, protocol, sector, threat, control or deliverable.
- Report missing, ambiguous or conflicting terminology through the contribution process.

# 3. Glossary conventions

| Convention | Meaning |
|---|---|
| Term | Preferred display name |
| Acronym | Common abbreviation, if one exists |
| Definition | Concise context-specific explanation |
| Context | Engineering, security, safety, governance, AI or regulatory |
| Related terms | Concepts that should be read together |
| Repository link | Relevant chapter or guide |
| Authority | Primary source to consult for formal use |

Definitions use neutral language. "Typically" indicates common usage, not a universal requirement. "May" indicates possibility, not mandatory behavior.

# 4. OT and industrial control fundamentals

| Term | Acronym | Definition | Related concepts |
|---|---|---|---|
| Operational Technology | OT | Hardware and software that monitor or cause changes in physical devices, processes and events | ICS, SCADA, DCS |
| Industrial Control System | ICS | Systems used to monitor or control industrial processes | PLC, RTU, DCS, SCADA |
| Supervisory Control and Data Acquisition | SCADA | Supervisory systems that gather telemetry and support remote monitoring and control | HMI, RTU, historian |
| Distributed Control System | DCS | Integrated control architecture commonly used for complex continuous or batch processes | Controller, operator station |
| Programmable Logic Controller | PLC | Industrial controller that executes logic to monitor inputs and control outputs | I/O, ladder logic |
| Remote Terminal Unit | RTU | Field device used for remote telemetry and control, often in geographically distributed infrastructure | SCADA, telemetry |
| Human Machine Interface | HMI | Operator interface for viewing process status and interacting with control functions | SCADA, DCS |
| Safety Instrumented System | SIS | Instrumented system designed to achieve or maintain a safe process state | SIF, safety lifecycle |
| Safety Instrumented Function | SIF | Specific safety function implemented by a SIS to reduce a defined risk | Sensor, logic solver, final element |
| Intelligent Electronic Device | IED | Microprocessor-based device used in electrical protection, control, measurement or automation | Substation, IEC 61850 |
| Engineering Workstation | EWS | Engineering system used to configure, program or maintain industrial automation equipment | PLC, DCS |
| Operator Station | OS | Workstation used by operators to monitor and interact with process systems | HMI, DCS |
| Historian | | System that stores time-series process and operational data | Telemetry |
| Input / Output | I/O | Signals and interfaces through which controllers receive measurements and drive devices | Analog, digital |
| Programmable Automation Controller | PAC | Controller platform combining PLC-like and computing capabilities | PLC, automation |
| Process Control | | Regulation or sequencing of an industrial process to achieve intended operating conditions | PID, setpoint |
| Batch Process | | Production process executed in defined batches or recipes | Recipe, batch control |
| Continuous Process | | Process that operates with continuous material or energy flow | Refining, chemical production |
| Discrete Manufacturing | | Production involving distinct units, assembly steps or events | PLC, robotics |
| Telemetry | | Remote measurement and transmission of status or process data | RTU, SCADA |
| Setpoint | | Desired target value for a controlled process variable | PID, controller |
| Process Variable | PV | Measured value of a process parameter | Temperature, pressure, flow |
| Manipulated Variable | MV | Variable adjusted by a control system to influence a process | Valve position, motor speed |
| Control Loop | | Feedback arrangement that measures a process variable and adjusts an output | PID, sensor, actuator |
| Supervisory Control | | Higher-level monitoring and coordination of lower-level control functions | SCADA, DCS |

# 5. Instrumentation, process and safety terminology

| Term | Acronym | Definition | Related concepts |
|---|---|---|---|
| Sensor | | Device that detects a physical quantity or condition | Transmitter, input |
| Transmitter | | Device that converts a measurement into a signal for monitoring or control | 4 to 20 mA, fieldbus |
| Actuator | | Device that produces physical movement or action in response to a control signal | Valve, motor |
| Final Control Element | FCE | Component that directly changes the process, such as a control valve or drive | Actuator, SIF |
| Pressure Transmitter | PT | Instrument that measures pressure and provides a corresponding output | Process variable |
| Temperature Transmitter | TT | Instrument that measures temperature and provides a corresponding output | Thermocouple, RTD |
| Flow Transmitter | FT | Instrument that measures fluid or gas flow | Flow meter |
| Level Transmitter | LT | Instrument that measures material level in a vessel or tank | Radar, hydrostatic |
| Emergency Shutdown System | ESD | System designed to bring a process or equipment to a defined safe state during specified conditions | SIS, shutdown |
| Fire and Gas System | F&G | System that detects fire or hazardous gas conditions and initiates defined alarms or actions | Detector, ESD |
| Basic Process Control System | BPCS | System responsible for normal process control | DCS, PLC |
| Safety Lifecycle | | Lifecycle activities for specifying, designing, operating and maintaining safety instrumented functions | IEC 61511 |
| Safety Integrity Level | SIL | Discrete level used to specify safety integrity requirements for a safety function | IEC 61508, IEC 61511 |
| Process Hazard Analysis | PHA | Structured examination of process hazards and safeguards | HAZOP, LOPA |
| Hazard and Operability Study | HAZOP | Structured team-based method for identifying process deviations and hazards | PHA |
| Layer of Protection Analysis | LOPA | Method for evaluating independent protection layers against a defined initiating event | PHA, SIS |
| Independent Protection Layer | IPL | Safeguard that meets defined criteria for independence, effectiveness and auditability in a risk analysis | LOPA |
| Management of Change | MOC | Formal process for evaluating, approving, implementing and reviewing changes | Engineering governance |
| Permit to Work | PTW | Formal authorization and coordination process for specified work activities | Isolation, maintenance |
| Lockout / Tagout | LOTO | Procedures to control hazardous energy during maintenance or servicing | Isolation, safety |
| Functional Safety | | Part of overall safety relating to systems that depend on correct operation of safety-related systems | IEC 61508 |
| Proof Test | | Test intended to reveal dangerous undetected failures in a safety function | SIL, maintenance |

# 6. Industrial architecture and networking terminology

| Term | Acronym | Definition | Related concepts |
|---|---|---|---|
| Purdue Enterprise Reference Architecture | PERA | Reference model often used to discuss industrial and enterprise system layers | Purdue model |
| Purdue model | | Layered conceptual view of industrial operations and enterprise systems | Levels 0 to 5 |
| Zone | | Grouping of assets with common security requirements under an architecture risk model | IEC 62443 |
| Conduit | | Logical grouping of communication channels between zones with defined security requirements | Segmentation |
| Demilitarized Zone | DMZ | Network segment used to control exchanges between security domains | Industrial DMZ |
| Industrial DMZ | IDMZ | DMZ architecture separating enterprise and industrial networks | Firewall, proxy |
| Segmentation | | Separation of networks or systems to limit unnecessary communication and contain risk | Zones, conduits |
| Microsegmentation | | Fine-grained policy separation between workloads or assets | Identity, network policy |
| Network Tap | TAP | Device or interface that provides a copy of network traffic for monitoring | Passive monitoring |
| Switched Port Analyzer | SPAN | Switch feature that mirrors selected traffic to a monitoring port | Packet capture |
| Intrusion Detection System | IDS | System that identifies suspicious activity or policy violations | NIDS, HIDS |
| Network Intrusion Detection System | NIDS | IDS that analyzes network traffic | OT NDR |
| Network Detection and Response | NDR | Technology and process for identifying and investigating network activity | IDS, analytics |
| Firewall | | Network security control enforcing traffic policy | ACL, zones |
| Access Control List | ACL | Rules that permit or deny specified traffic or access | Firewall, router |
| Virtual LAN | VLAN | Logical Layer 2 network segmentation mechanism | Switching |
| Internet Protocol | IP | Network-layer protocol used for addressing and routing | IPv4, IPv6 |
| Transmission Control Protocol | TCP | Connection-oriented transport protocol | Port, session |
| User Datagram Protocol | UDP | Connectionless transport protocol | Telemetry, DNS |
| Open Systems Interconnection | OSI | Reference model describing network communication functions in layers | Ethernet, IP |
| Quality of Service | QoS | Mechanisms for prioritizing or managing network traffic | Latency, availability |
| Network Time Protocol | NTP | Protocol used to synchronize clocks across networks | Time source |
| Precision Time Protocol | PTP | Protocol for precise clock synchronization in suitable networks | IEEE 1588 |
| Remote Access | RA | Connectivity allowing users or systems to access a remote environment | VPN, jump host |
| Jump Server | | Controlled intermediary system used to access other systems | Bastion, PAM |
| Bastion Host | | Hardened host designed to provide controlled access across a boundary | Jump server |
| Unidirectional Gateway | | Technology designed to allow information flow in one direction | Data diode |
| Data Diode | | Hardware-enforced one-way data transfer mechanism | Unidirectional gateway |
| Virtual Private Network | VPN | Encrypted network connection over an underlying network | Remote access |
| Network Address Translation | NAT | Address translation performed by a network device | Firewall, routing |
| Intrusion Prevention System | IPS | System designed to detect and block specified malicious activity | Inline inspection |
| Packet Capture | PCAP | Recorded network packet data or a common file format for it | Wireshark |
| Latency | | Time delay in communication or processing | Jitter |
| Jitter | | Variation in packet delay | Real-time communications |
| Availability | | Ability of a system or service to perform when required | Resilience |
| Resilience | | Ability to withstand, adapt to and recover from disruption | Continuity, recovery |

# 7. Industrial protocol glossary

| Protocol / Standard | Definition and context | Common research chapter |
|---|---|---|
| Modbus | Industrial application protocol with serial and TCP variants | 04 Industrial Protocols |
| Modbus TCP | Modbus messaging carried over TCP/IP | 04 Industrial Protocols |
| Modbus RTU | Serial Modbus transmission mode | 04 Industrial Protocols |
| DNP3 | Distributed Network Protocol used in utility and control applications | 04 Industrial Protocols |
| IEC 60870-5-101 | Telecontrol communication standard commonly associated with serial links | 04 Industrial Protocols |
| IEC 60870-5-104 | Telecontrol communication standard using TCP/IP transport | 04 Industrial Protocols |
| IEC 61850 | Standard suite for communication and systems in power utility automation | 07 Power Systems |
| GOOSE | Generic Object Oriented Substation Event messaging defined within IEC 61850 | 07 Power Systems |
| MMS | Manufacturing Message Specification, used in IEC 61850 client/server communication | 07 Power Systems |
| OPC | Family of industrial interoperability technologies | 04 Industrial Protocols |
| OPC UA | Platform-independent industrial interoperability architecture with security capabilities | 04 Industrial Protocols |
| PROFINET | Industrial Ethernet communication technology | 04 Industrial Protocols |
| PROFIBUS | Fieldbus technology used in industrial automation | 04 Industrial Protocols |
| EtherNet/IP | Industrial protocol using the Common Industrial Protocol over Ethernet and IP | 04 Industrial Protocols |
| Common Industrial Protocol | CIP | Industrial protocol family used by technologies including EtherNet/IP | 04 Industrial Protocols |
| EtherCAT | Industrial Ethernet technology designed for real-time control applications | 04 Industrial Protocols |
| BACnet | Building automation and control networking protocol | 07 Building Automation |
| KNX | Standardized building control communication technology | 07 Building Automation |
| HART | Highway Addressable Remote Transducer communication protocol | Instrumentation |
| WirelessHART | Wireless sensor network technology based on HART | Instrumentation |
| ISA100.11a | Wireless networking standard for industrial automation | Instrumentation |
| MQTT | Lightweight publish/subscribe messaging protocol | IIoT |
| AMQP | Advanced Message Queuing Protocol | Integration |
| REST API | HTTP-based application interface style | OT integration |
| IEEE 1588 | Precision clock synchronization standard | Time synchronization |

Protocol support, security properties and implementation behavior vary by product and version. Do not infer that a protocol is secure merely because a standard defines authentication, encryption or integrity features. Verify the specific profile, configuration and deployment.

# 8. Cybersecurity terminology

| Term | Acronym | Definition | Related concepts |
|---|---|---|---|
| Confidentiality, Integrity and Availability | CIA | Three widely used information security objectives | Risk |
| Risk | | Effect of uncertainty on objectives, often assessed through likelihood and consequence | Risk assessment |
| Threat | | Potential cause of an unwanted incident | Threat actor |
| Threat Actor | | Person, group or entity that conducts or may conduct activity affecting systems | Campaign |
| Vulnerability | | Weakness that can be exploited or triggered by a threat | CVE |
| Exposure | | Condition in which an asset or weakness is reachable or otherwise accessible to a threat | Attack surface |
| Attack Surface | | Set of points where an attacker could attempt to interact with a system | External exposure |
| Attack Path | | Sequence of access and actions that could lead to an objective | Threat modelling |
| Exploit | | Method or code that takes advantage of a vulnerability or weakness | Exploitability |
| Indicator of Compromise | IOC | Observable artifact associated with potential malicious activity | Threat intelligence |
| Indicator of Attack | IOA | Observable behavior or sequence that may indicate an attack | Detection |
| Tactics, Techniques and Procedures | TTPs | Adversary goals, methods and operational patterns | ATT&CK |
| Threat Intelligence | TI | Analyzed information about threats that supports decisions | Intelligence lifecycle |
| Security Operations Centre | SOC | Function responsible for security monitoring, analysis and response | SIEM |
| Security Information and Event Management | SIEM | Platform for collecting and analyzing security events and logs | SOC |
| Security Orchestration, Automation and Response | SOAR | Technology and workflows for coordinating security operations | Playbooks |
| Endpoint Detection and Response | EDR | Endpoint telemetry and investigation capability | Endpoint security |
| Extended Detection and Response | XDR | Integrated detection and response across multiple telemetry domains | SOC |
| Multi-Factor Authentication | MFA | Authentication using multiple distinct factor types | Identity |
| Privileged Access Management | PAM | Controls for managing privileged identities and sessions | Least privilege |
| Identity and Access Management | IAM | Processes and systems for managing identities and access | Authentication |
| Zero Trust | | Security approach that avoids implicit trust based solely on network location | Continuous verification |
| Least Privilege | | Granting only the access necessary for an authorized task | RBAC |
| Role-Based Access Control | RBAC | Access control based on assigned roles | IAM |
| Attribute-Based Access Control | ABAC | Access control based on subject, resource, action and environmental attributes | Policy |
| Defense in Depth | | Use of multiple complementary security controls | Layered security |
| Hardening | | Reducing attack surface through configuration and service controls | Baseline |
| Patch Management | | Governance and process for evaluating, testing and deploying updates | Vulnerability management |
| Vulnerability Management | VM | Lifecycle for identifying, assessing, prioritizing and treating vulnerabilities | CVE |
| Penetration Testing | PT | Authorized security testing intended to evaluate exploitability and control effectiveness | Rules of engagement |
| Security Assessment | | Structured evaluation of security controls, architecture or risk | Audit |
| Red Team | | Authorized adversary-emulation function | Purple team |
| Blue Team | | Defensive security function | SOC |
| Purple Team | | Collaborative approach combining offensive simulation and defensive improvement | Detection engineering |
| Incident | | Event or series of events requiring response under an organization's criteria | Incident response |
| Digital Forensics | DFIR | Methods for preserving and analyzing digital evidence | Chain of custody |
| Business Continuity | BC | Capability to continue prioritized business activities during disruption | Resilience |
| Disaster Recovery | DR | Processes for restoring systems and services after disruption | Recovery |
| Recovery Time Objective | RTO | Target time within which a service or system is to be restored | Recovery |
| Recovery Point Objective | RPO | Target maximum data loss measured in time | Backup |
| Mean Time to Detect | MTTD | Average time taken to detect an event under a defined measurement method | SOC metrics |
| Mean Time to Respond | MTTR | Metric whose exact meaning must be defined by the organization | Response metrics |
| Chain of Custody | CoC | Record of evidence collection, handling, transfer and access | Forensics |

# 9. Vulnerability and advisory terminology

| Term | Acronym | Definition | Important caution |
|---|---|---|---|
| Common Vulnerabilities and Exposures | CVE | Public identifier system for disclosed vulnerabilities | A CVE does not prove asset applicability |
| Common Vulnerability Scoring System | CVSS | Framework for communicating vulnerability severity | Not a complete OT risk rating |
| Exploit Prediction Scoring System | EPSS | Model estimating probability of exploitation activity for a CVE over a defined horizon | Not proof of exploitation at a site |
| Known Exploited Vulnerabilities | KEV | CISA catalogue of vulnerabilities with evidence of exploitation | Verify relevance and current status |
| National Vulnerability Database | NVD | NIST vulnerability data resource | Enrichment and records may change |
| Common Weakness Enumeration | CWE | Categorization of software and hardware weakness types | Weakness category is not a CVE |
| Common Platform Enumeration | CPE | Structured naming scheme for IT products and platforms | Product matching may be ambiguous |
| Vendor Security Advisory | VSA | Vendor-issued security notice about a product or service | Check affected and fixed versions |
| End of Life | EOL | Product lifecycle point at which support or updates may end | Verify exact vendor policy |
| End of Support | EOS | Point at which a vendor no longer provides defined support | Contract and product terms matter |
| Zero-Day | | Vulnerability or exploit situation where effective remediation or prior disclosure may be absent; usage varies by context | Define the exact meaning used |
| Compensating Control | | Alternative control that reduces risk when the preferred control is unavailable | Effectiveness must be validated |
| Risk Acceptance | | Formal decision by an authorized owner to retain specified residual risk | Must be reviewed under policy |

# 10. Standards, frameworks and governance terminology

| Term | Acronym | Definition | Reference context |
|---|---|---|---|
| International Electrotechnical Commission | IEC | International standards organization for electrotechnical domains | IEC standards |
| International Organization for Standardization | ISO | International standards organization | ISO standards |
| International Society of Automation | ISA | Professional association and standards developer in automation | ISA/IEC 62443 |
| ISA/IEC 62443 | | Standards series for security of industrial automation and control systems | OT security |
| IEC 61508 | | Functional safety standard series for electrical, electronic and programmable electronic safety-related systems | Functional safety |
| IEC 61511 | | Functional safety standard for process industry sector safety instrumented systems | SIS |
| NIST | | US National Institute of Standards and Technology | NIST publications |
| NIST Cybersecurity Framework | CSF | Framework for managing cybersecurity risk outcomes | Enterprise security |
| NIST SP 800-82 | | NIST guide to OT security | OT security |
| MITRE ATT&CK | | Knowledge base of adversary tactics and techniques | Threat analysis |
| ATT&CK for ICS | | ATT&CK knowledge base focused on industrial control system environments | ICS threat analysis |
| MITRE ATLAS | | Adversarial threat landscape for AI systems | AI security |
| National Cybersecurity Strategy | NCS | National policy or strategy document; status and legal effect vary by country | Regulatory research |
| Critical Information Infrastructure | CII | Term used in some jurisdictions for designated critical information infrastructure | National regulation |
| Critical Information Infrastructure Protection | CIIP | Activities and governance for protecting designated critical information infrastructure | National policy |
| Information Security Management System | ISMS | Management system for information security | ISO/IEC 27001 |
| AI Management System | AIMS | Management system for artificial intelligence under ISO/IEC 42001 context | AI governance |
| Statement of Applicability | SoA | Document identifying applicable controls and treatment decisions in an ISMS context | ISO/IEC 27001 |
| Plan-Do-Check-Act | PDCA | Iterative management improvement cycle | Management systems |
| Statement of Work | SOW | Contractual description of services, scope and deliverables | Engagement governance |
| Rules of Engagement | RoE | Authorized boundaries and conditions for security testing | Assessment governance |
| Key Performance Indicator | KPI | Measure used to evaluate performance against an objective | Governance |
| Key Risk Indicator | KRI | Measure used to indicate changes in risk exposure | Risk management |
| Service Level Agreement | SLA | Agreement defining service expectations and measures | Operations |

# 11. AI, data and agentic security terminology

| Term | Acronym | Definition | Related concepts |
|---|---|---|---|
| Artificial Intelligence | AI | Machine-based system capability to perform tasks associated with human intelligence | ML, LLM |
| Machine Learning | ML | Methods that learn patterns from data | Training |
| Deep Learning | DL | Machine learning using multi-layer neural networks | Neural network |
| Large Language Model | LLM | Model trained to process and generate language | Generative AI |
| Generative AI | GenAI | AI that generates content such as text, code, images or audio | LLM |
| Retrieval-Augmented Generation | RAG | Approach that retrieves external information and provides it as model context | Knowledge base |
| Embedding | | Numerical representation of data used in similarity and retrieval systems | Vector search |
| Vector Database | | Database designed to store and query vector representations | RAG |
| Agent | | Software workflow that uses a model and permitted tools to perform a defined task | Tool calling |
| Agentic Workflow | | Workflow where one or more agents plan or select bounded steps toward an objective | Orchestration |
| Multi-Agent System | MAS | System in which multiple agents interact or coordinate | Agent orchestration |
| Tool Calling | | Model-directed invocation of a defined external function or API | Tool gateway |
| Prompt Injection | | Attack in which malicious instructions influence model behavior through prompts or retrieved content | LLM security |
| Indirect Prompt Injection | | Prompt injection delivered through external content processed by a model | RAG security |
| Hallucination | | Generated content that is unsupported or incorrect but presented as plausible | Grounding |
| Grounding | | Linking generated output to supplied evidence or authoritative sources | Citation |
| Model Drift | | Change in model performance or input distribution over time | Monitoring |
| Data Poisoning | | Manipulation of training or retrieval data to influence system behavior | Data integrity |
| Human-in-the-Loop | HITL | Human review or approval integrated into a workflow | Oversight |
| Human-on-the-Loop | HOTL | Human supervision of an automated process with ability to intervene | Oversight |
| Model Card | | Structured description of a model's intended use, evaluation and limitations | Model governance |
| System Card | | Documentation describing an AI system and its safety or deployment characteristics | AI assurance |
| AI Risk Management Framework | AI RMF | NIST framework for managing AI risks | NIST |
| Inference | | Model operation that generates an output from an input | Model serving |
| Fine-Tuning | | Additional model training or adaptation using selected data | Model lifecycle |
| Retrieval Corpus | | Collection of documents or data made available to a retrieval system | RAG |
| Evaluation Dataset | | Dataset used to assess model or workflow performance | Benchmark |
| Guardrail | | Control that constrains model input, output or permitted actions | Safety |
| Model Supply Chain | | Models, datasets, dependencies, services and processes used to build and operate AI | AI security |

# 12. Global regulatory terminology

| Term | Definition | Caution |
|---|---|---|
| Law | Binding legal instrument enacted through a jurisdiction's legal process | Confirm scope and commencement |
| Regulation | Binding instrument or delegated rules, depending on jurisdiction | Meaning varies by legal system |
| Directive | Instrument that may require implementation through national law, depending on issuing authority | Check transposition and applicability |
| Decree | Formal legal or executive instrument under a jurisdiction's system | Verify authority and legal effect |
| Policy | Organizational or governmental statement of intent and rules | Not necessarily legislation |
| Strategy | Document setting goals and direction | Does not automatically create binding duties |
| Guideline | Recommended approach from an authority or body | Verify whether incorporated into a binding requirement |
| Standard | Published technical or management specification | Legal force depends on adoption, contract or law |
| Mandatory Requirement | Obligation imposed by applicable law, regulation, contract or binding direction | Record exact source and entity scope |
| Supervisory Authority | Body responsible for oversight in a defined domain | Powers vary by jurisdiction |
| Sector Regulator | Authority overseeing a specific regulated sector | Sector and entity scope matter |
| Critical Infrastructure | Assets or services designated as important to societal or economic functioning | Definition varies by country |
| Data Residency | Requirement or practice concerning where data is stored or processed | Distinguish residency from sovereignty |
| Data Sovereignty | Concept concerning legal authority and jurisdiction over data | Analyze law and control relationships |
| Cross-Border Transfer | Transfer of data across national borders | Legal conditions vary |
| Regulatory Applicability | Determination whether a requirement applies to an entity, sector, system or activity | Requires evidence and qualified review |

# 13. Acronym master dictionary

This is a quick lookup list. Use the detailed sections and primary sources for formal definitions.

| Acronym | Expanded term |
|---|---|
| ACL | Access Control List |
| AI | Artificial Intelligence |
| AIMS | AI Management System |
| ABAC | Attribute-Based Access Control |
| AMQP | Advanced Message Queuing Protocol |
| API | Application Programming Interface |
| BCP | Business Continuity Plan |
| BPCS | Basic Process Control System |
| BACnet | Building Automation and Control Network |
| CII | Critical Information Infrastructure |
| CIA | Confidentiality, Integrity and Availability |
| CIP | Common Industrial Protocol |
| CSF | Cybersecurity Framework |
| CVE | Common Vulnerabilities and Exposures |
| CVSS | Common Vulnerability Scoring System |
| CWE | Common Weakness Enumeration |
| DCS | Distributed Control System |
| DNP3 | Distributed Network Protocol |
| DR | Disaster Recovery |
| EDR | Endpoint Detection and Response |
| EOL | End of Life |
| EOS | End of Support |
| ESD | Emergency Shutdown |
| EWS | Engineering Workstation |
| F&G | Fire and Gas |
| HAZOP | Hazard and Operability Study |
| HMI | Human Machine Interface |
| HITL | Human-in-the-Loop |
| HOTL | Human-on-the-Loop |
| IACS | Industrial Automation and Control Systems |
| ICS | Industrial Control System |
| IDMZ | Industrial Demilitarized Zone |
| IDS | Intrusion Detection System |
| IEC | International Electrotechnical Commission |
| IED | Intelligent Electronic Device |
| IIoT | Industrial Internet of Things |
| I/O | Input / Output |
| IOC | Indicator of Compromise |
| IOA | Indicator of Attack |
| IP | Internet Protocol |
| IPS | Intrusion Prevention System |
| ISA | International Society of Automation |
| ISMS | Information Security Management System |
| IT | Information Technology |
| KPI | Key Performance Indicator |
| KRI | Key Risk Indicator |
| LOPA | Layer of Protection Analysis |
| LLM | Large Language Model |
| LOTO | Lockout / Tagout |
| MAS | Multi-Agent System |
| MFA | Multi-Factor Authentication |
| ML | Machine Learning |
| MMS | Manufacturing Message Specification |
| MOC | Management of Change |
| MQTT | Message Queuing Telemetry Transport |
| NDR | Network Detection and Response |
| NIST | National Institute of Standards and Technology |
| NTP | Network Time Protocol |
| OT | Operational Technology |
| OSI | Open Systems Interconnection |
| PAC | Programmable Automation Controller |
| PAM | Privileged Access Management |
| PCAP | Packet Capture |
| PDCA | Plan-Do-Check-Act |
| PERA | Purdue Enterprise Reference Architecture |
| PHA | Process Hazard Analysis |
| PLC | Programmable Logic Controller |
| PT | Penetration Testing or Pressure Transmitter, depending on context |
| PTW | Permit to Work |
| PV | Process Variable |
| QoS | Quality of Service |
| RAG | Retrieval-Augmented Generation |
| RBAC | Role-Based Access Control |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| RTU | Remote Terminal Unit |
| SCADA | Supervisory Control and Data Acquisition |
| SIF | Safety Instrumented Function |
| SIL | Safety Integrity Level |
| SIEM | Security Information and Event Management |
| SIS | Safety Instrumented System |
| SLA | Service Level Agreement |
| SOC | Security Operations Centre |
| SOAR | Security Orchestration, Automation and Response |
| SOW | Statement of Work |
| SPAN | Switched Port Analyzer |
| TCP | Transmission Control Protocol |
| TI | Threat Intelligence |
| TTP | Tactics, Techniques and Procedures |
| UDP | User Datagram Protocol |
| VLAN | Virtual LAN |
| VPN | Virtual Private Network |
| WAN | Wide Area Network |
| XDR | Extended Detection and Response |

# 14. Master chapter index

The repository's top-level README is the canonical entry point. This map describes the intended knowledge domains and main navigation path.

| Chapter / directory | Knowledge domain | Main relationships |
|---|---|---|
| 00 Project Governance | Charter, documentation, research quality, contribution rules | All chapters |
| 01 OT Fundamentals | OT concepts and industrial context | Architecture, assets, protocols |
| 02 Industrial Architecture | Reference architectures, Purdue, zones and conduits | Assets, networks, standards |
| 03 Industrial Assets and Systems | PLC, RTU, DCS, SCADA, HMI, SIS, IED | Protocols, risks, lifecycle |
| 04 Industrial Protocols and Networks | Industrial communications and network design | Assets, segmentation, monitoring |
| 05 Standards and Frameworks | IEC, ISO, NIST and industry frameworks | Controls, assurance, regulation |
| 06 Global Regulatory Mapping | Country, regional and sector requirements | Governance, evidence, controls |
| 07 Industry and Use Cases | Sector-specific process and security scenarios | Assets, threats, controls |
| 08 Threat Intelligence | Actors, campaigns, malware and incidents | ATT&CK, detection, response |
| 09 Vulnerabilities and Advisories | CVEs, product advisories and applicability | Assets, risk, remediation |
| 10 OT Security Engineering | Hardening, segmentation and defensive design | Architecture, standards |
| 11 Assessment and Testing | Authorized assessment and evidence methods | Scope, controls, findings |
| 12 Monitoring and Detection | OT SOC, NDR, SIEM and detection engineering | Threats, assets, response |
| 13 Incident Response and Recovery | Incident management, forensics and restoration | Detection, evidence, continuity |
| 14 Risk Governance and Assurance | Risk, policies, audit and control assurance | Regulation, standards, CISO |
| 15 Tools and Technology | Security products and engineering platforms | Assessment, monitoring, operations |
| 16 Labs and Simulations | Cyber ranges, digital twins and exercises | Learning, testing, detection |
| 17 AI and Agent Workflows | AI architecture, agents and governance | Data, SOC, assurance |
| 18 Templates and Reference Materials | Registers, checklists and professional deliverables | All operational chapters |
| 19 Research and Learning | Research sources, evidence grading and learning paths | Threat intelligence, standards |
| 20 Glossary and Indexes | Shared terminology and knowledge navigation | All chapters |

# 15. Cross-chapter knowledge relationships

| Starting question | Read in sequence | Expected outcome |
|---|---|---|
| What is this industrial asset and why is it important? | 01 → 03 → 07 → 14 | Context, ownership and consequence |
| How should this network be segmented? | 02 → 03 → 04 → 05 → 10 | Architecture and control design |
| Is this vulnerability relevant to the plant? | 03 → 07 → 09 → 14 → 18 | Applicability and risk decision |
| How should OT activity be monitored? | 02 → 04 → 08 → 12 → 13 | Visibility, detection and response |
| How should an incident be investigated? | 08 → 12 → 13 → 18 → 19 | Evidence-led response |
| How do we assess IEC 62443 alignment? | 05 → 02 → 10 → 11 → 14 → 18 | Scoped control assessment and evidence |
| How do we review supplier access? | 02 → 06 → 07 → 10 → 14 → 18 | Access, jurisdiction and supplier risk |
| How do we introduce AI into OT security? | 03 → 04 → 12 → 17 → 18 → 14 | Bounded, governed AI assistance |
| How do we validate recovery? | 03 → 07 → 13 → 14 → 18 | Recovery evidence and ownership |
| How do we build a safe lab? | 02 → 03 → 04 → 15 → 16 → 18 | Isolated simulation and evaluation |

# 16. Knowledge relationship model

Use a consistent entity model for future indexes, search and graph-based navigation.

## 16.1 Core entity types

| Entity | Example identifier | Description |
|---|---|---|
| Country | COUNTRY-SA | Jurisdiction |
| Regulator | REGULATOR-EXAMPLE | Government or sector authority |
| Requirement | REQ-EXAMPLE-001 | Legal, contractual or framework requirement |
| Standard | STD-IEC62443 | Standard or framework |
| Control | CTRL-OT-001 | Internal control statement |
| Sector | SECTOR-OIL-GAS | Industrial sector |
| Site | SITE-RESTRICTED-001 | Facility reference; sensitive values stay private |
| Process | PROCESS-EXAMPLE-001 | Industrial process |
| Asset class | ASSET-PLC | Asset category |
| Asset | ASSET-EXAMPLE-001 | Specific managed asset; sensitive inventory stays private |
| Protocol | PROTO-MODBUS-TCP | Industrial communication protocol |
| Zone | ZONE-EXAMPLE-001 | Security zone |
| Conduit | CONDUIT-EXAMPLE-001 | Communication path between zones |
| Threat | THREAT-EXAMPLE-001 | Threat scenario or actor record |
| Technique | ATTACK-ICS-REF | Verified behavior reference |
| Vulnerability | CVE-YYYY-NNNN | Vulnerability record |
| Advisory | ADV-VENDOR-001 | Vendor or authority advisory |
| Detection | DET-OT-001 | Detection use case |
| Incident | INCIDENT-PUBLIC-001 | Publicly documented incident |
| Risk | RISK-OT-001 | Risk scenario |
| Evidence | EVIDENCE-REF-001 | Controlled evidence reference |
| Lab | LAB-OT-001 | Isolated exercise |
| AI system | AI-OT-001 | Governed AI use case |
| Deliverable | DOC-OT-001 | Template, report or register |

Identifiers above are examples. Never publish real site identifiers, asset details or sensitive evidence references in a public index.

## 16.2 Relationship types

| Relationship | Example |
|---|---|
| applies_to | Requirement applies to defined entity scope |
| implemented_by | Requirement implemented by control |
| evidenced_by | Control supported by evidence |
| affects | Threat or vulnerability affects an asset class |
| communicates_with | Asset communicates with another asset |
| belongs_to | Asset belongs to a zone |
| connected_by | Zones communicate through a conduit |
| detected_by | Behavior is detected by a use case |
| mitigated_by | Risk is reduced by a control |
| reported_in | Claim is reported in a source |
| corroborated_by | Claim supported by independent evidence |
| mapped_to | Technique or control mapped to another framework |
| tested_in | Control or behavior tested in a lab |
| documented_in | Concept described in a chapter |
| supersedes | New version replaces prior record |
| reviewed_by | Record has an accountable reviewer |

# 17. Traceability and evidence chain

For a consequential claim, preserve the path from source to decision:

**Source → Claim → Analysis → Threat or requirement → Asset and process context → Risk → Control → Test → Evidence → Decision → Review**

Every link should have a stable identifier or reference. Do not create an unsupported relationship simply because two topics appear in the same chapter.

# 18. Master indexes to maintain

| Index | Key fields | Source of truth |
|---|---|---|
| Acronym index | Acronym, expansion, context, chapter | Chapter 20 |
| Asset index | Asset type, function, lifecycle, chapter | Chapter 03 |
| Protocol index | Protocol, version/profile, transport, security notes | Chapter 04 |
| Standards index | Publisher, identifier, edition, status, scope | Chapter 05 |
| Regulatory index | Jurisdiction, regulator, instrument, effective date, applicability | Chapter 06 |
| Sector index | Sector, process, asset classes, risk scenarios | Chapter 07 |
| Threat index | Actor/campaign, source, confidence, time period | Chapter 08 |
| Vulnerability index | CVE, vendor, product, version, advisory, status | Chapter 09 |
| Control index | Control ID, objective, owner, evidence, mappings | Chapters 10 and 14 |
| Assessment index | Method, authorization, test boundary, evidence | Chapter 11 |
| Detection index | Use case, telemetry, logic reference, validation | Chapter 12 |
| Incident index | Public case, timeline, source quality, lessons | Chapters 13 and 19 |
| Tool index | Tool, function, supported platform, limitations | Chapter 15 |
| Lab index | Lab ID, objective, prerequisites, isolation, assessment | Chapter 16 |
| AI index | System, model, data, tools, risk, oversight, evaluation | Chapter 17 |
| Template index | Deliverable, format, owner, revision, related process | Chapter 18 |
| Research index | Source, claim, evidence grade, review date | Chapter 19 |

# 19. Knowledge quality and source governance

Every substantive page should contain:
- Title and unique document ID.
- Scope and intended audience.
- Version and status.
- Author or accountable owner where known.
- Created and last-reviewed dates.
- Review due date.
- Definitions and assumptions.
- Technical or regulatory source references.
- Applicable edition and publication status.
- Limitations and known gaps.
- Related repository chapters.
- Revision history.

## 19.1 Content status model

| Status | Meaning |
|---|---|
| Draft | Work in progress and not yet reviewed |
| Technical Review | Awaiting subject matter review |
| Source Verification | Claims and references being validated |
| Published | Approved for general repository use |
| Needs Update | New source, edition or technical change requires review |
| Superseded | Replaced by a newer controlled record |
| Withdrawn | Removed from active use with reason retained |

Do not label content compliant, certified or approved without the specific formal basis and authority.

## 19.2 Review triggers

Review a page when:
- A standard or framework edition changes.
- A law or regulatory instrument is amended.
- A regulator publishes new guidance.
- A vendor changes product support or affected versions.
- A major technical correction is identified.
- A source is withdrawn or materially revised.
- A vulnerability or incident changes the risk context.
- A tool or product changes supported functionality.
- A reader submits a substantiated correction.

# 20. Contribution and terminology rules

Contributors should:
1. Search for an existing term before adding a new one.
2. Prefer a widely accepted term and explain aliases.
3. Expand an acronym on first use in a page.
4. Avoid using one acronym for multiple meanings without context.
5. Link terms to relevant chapters.
6. Cite primary sources for formal or disputed definitions.
7. Record edition and jurisdiction where relevant.
8. Mark uncertain or locally defined terminology.
9. Avoid copying licensed standards text.
10. Submit corrections with a source and explanation.

## 20.1 Naming convention

Use descriptive file names in uppercase with hyphens, for example:
- INDUSTRIAL-PROTOCOL-SECURITY.md
- OT-ASSET-INVENTORY.md
- GLOBAL-REGULATORY-MAPPING.md

Use stable IDs in content where cross references need to survive a file rename. Avoid relying only on line numbers or display titles as identifiers.

# 21. Repository navigation and publishing standards

- The root README is the primary landing page.
- Each chapter directory should have a README when it contains multiple resources.
- Every published guide should be linked from its chapter README and root index where appropriate.
- Relative links should be used for files inside the repository.
- External links should point to authoritative publishers wherever possible.
- Links should be checked periodically.
- Avoid duplicate copies of the same authoritative content.
- Keep public educational content separate from private customer evidence.
- Keep generated indexes reproducible from source metadata where feasible.
- Use pull requests for substantive multi-author changes where repository permissions allow.
- Review generated changes before merging.

# 22. Search and AI retrieval readiness

Future search and AI retrieval should use structured metadata rather than treating the repository as unstructured text.

Recommended metadata fields:
- document_id
- title
- chapter
- topic
- sector
- asset_classes
- protocols
- standards
- jurisdictions
- source_ids
- publication_date
- last_reviewed
- review_due
- status
- classification
- owner
- related_documents

AI retrieval controls:
- Respect public, internal, confidential and restricted classifications.
- Keep source metadata attached to retrieved passages.
- Do not merge contradictory sources without showing the conflict.
- Preserve the exact standards edition and legal jurisdiction.
- Return an explicit unknown when evidence is absent.
- Cite the repository page and original primary source.
- Do not generate compliance conclusions from keyword similarity.
- Require human review for safety, legal, regulatory and operational decisions.
- Keep private customer data out of public indexes and embeddings.

# 23. Repository-wide quality audit checklist

- [ ] All 20 chapter directories exist and have clear scope.
- [ ] Root README links resolve.
- [ ] Chapter READMEs link to their substantive guides.
- [ ] Every guide has document ID, version, status and review date.
- [ ] Mermaid diagrams render correctly where used.
- [ ] No malformed Markdown tables or code fences remain.
- [ ] Internal links resolve.
- [ ] External source links point to intended publishers.
- [ ] Standards editions and status are stated.
- [ ] Legal claims identify jurisdiction and legal instrument.
- [ ] Framework mappings include rationale and evidence.
- [ ] ATT&CK mappings cite behavior evidence.
- [ ] CVE claims include product/version applicability caveats.
- [ ] Operational recommendations include safety and change constraints.
- [ ] AI content distinguishes assistance from operational authority.
- [ ] No secrets, credentials or sensitive customer topology are published.
- [ ] Licensed standards text is not reproduced without permission.
- [ ] Duplicated or conflicting pages are identified.
- [ ] Stale and superseded content is marked.
- [ ] Each chapter has an owner and review trigger.

# 24. Roadmap beyond the 20 core chapters

The 20 chapters establish a broad knowledge architecture, but they do not mean every topic is complete. Future releases should deepen and validate the content.

Priority workstreams:
1. Source-backed country and sector regulatory registers.
2. Clause-level standards mapping with licensed-source verification.
3. Sector-specific engineering reference architectures.
4. Detailed protocol security guides and lab validation.
5. Verified public incident case studies with claim evidence matrices.
6. Vendor and product lifecycle catalogue.
7. OT SOC detection content with testable synthetic datasets.
8. Incident response and recovery exercise packs.
9. Native spreadsheet and document templates.
10. Isolated cyber range build guides and instructor materials.
11. AI agent reference implementation with a policy gateway.
12. Automated link, metadata and Markdown quality checks.
13. A controlled knowledge graph and search interface.
14. Translation and localization with technical review.
15. Community contribution and peer review programme.

# 25. References and formal terminology sources

Use the current authoritative publication and applicable edition for formal interpretation.

1. **NIST SP 800-82 Rev. 3, Guide to Operational Technology Security.** https://csrc.nist.gov/pubs/sp/800/82/r3/final
2. **ISA/IEC 62443 series.** Industrial automation and control systems security. https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
3. **IEC 61508 series.** Functional safety of electrical, electronic and programmable electronic safety-related systems. https://www.iec.ch/
4. **IEC 61511 series.** Functional safety for the process industry sector. https://www.iec.ch/
5. **NIST Cybersecurity Framework 2.0.** https://www.nist.gov/cyberframework
6. **MITRE ATT&CK for ICS.** https://attack.mitre.org/matrices/ics/
7. **MITRE ATLAS.** https://atlas.mitre.org/
8. **CISA ICS resources.** https://www.cisa.gov/ics
9. **ISO/IEC standards catalogue.** https://www.iso.org/standards.html
10. **ISA standards catalogue.** https://www.isa.org/standards-and-publications

# 26. Limitations and professional use

This glossary and index do not establish legal interpretation, engineering approval, safety approval, standards conformity or certification. Definitions are concise navigation aids. Verify formal terminology against the authoritative source, exact edition, jurisdiction and site context before using it in design, audit, procurement, incident response or regulatory submissions.

## Revision history

| Version | Date | Change | Status |
|---|---|---|---|
| 1.0 | 2026-11-17 | Initial OT security glossary, master index and knowledge architecture | Published reference |

## Expansion backlog

1. Expand the glossary with country-specific legal terms and regulator terminology.
2. Add clause-aware standards terminology with licensed references.
3. Add a machine-readable YAML or JSON metadata schema.
4. Generate acronym and chapter indexes automatically from source metadata.
5. Add a protocol-to-asset-to-threat relationship catalogue.
6. Add a sector-to-process-to-asset taxonomy.
7. Add a source-backed regulator and authority directory.
8. Add a searchable graph of controls, requirements and evidence.
9. Add automated internal link and diagram validation to CI.
10. Add a peer-reviewed terminology change process.

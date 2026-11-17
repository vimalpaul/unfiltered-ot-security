---
title: "OT Cybersecurity Labs, Digital Twins and Industrial Simulation Playbook"
document_id: "UOTS-16-LABS"
version: "1.0"
status: "Engineering and training reference"
owner: "Unfiltered OT Security"
created: "2026-11-17"
last_reviewed: "2026-11-17"
review_due: "2027-02-17"
scope: "Isolated OT cybersecurity labs, industrial process simulation, digital twins, validation and training"
classification: "Public"
---

# OT Cybersecurity Labs, Digital Twins and Industrial Simulation Playbook

**Document ID:** UOTS-16-LABS | **Version:** 1.0 | **Status:** Engineering and training reference

**Audience:** OT security engineers, control engineers, SOC analysts, incident responders, industrial network architects, trainers, researchers, system integrators, auditors and critical infrastructure operators.

> **Safety and authorization boundary:** Every hands-on activity in this playbook is intended for an isolated lab, synthetic dataset, hardware-in-the-loop test station, or explicitly approved non-production environment. Do not scan, fuzz, exploit, reprogram, disrupt, or inject traffic into a live plant, production network, safety instrumented system, utility, pipeline, building control system or third-party environment. A lab exercise is not authorization for production testing. Hardware-connected experiments require electrical, process, machinery and safety review, appropriate isolation, competent supervision and an approved method statement.

---

# 1. Purpose

This playbook defines how to design, build, operate and assess practical OT cybersecurity learning and validation environments. It connects industrial process understanding with network architecture, control systems, defensive monitoring, incident response, safety and governance.

A useful OT lab must do more than provide a vulnerable web interface or a packet capture. It should model a process, its instrumentation, controller logic, operator interface, engineering workflow, communications, safety constraints and operational consequences.

The objective is to build reproducible environments where learners can:
- Understand the physical process represented by a control system.
- Identify PLC, RTU, HMI, SCADA, historian and engineering workstation roles.
- Observe industrial protocols and normal communication patterns.
- Design and validate defensive controls.
- Investigate synthetic incidents and evidence.
- Test detection content without touching production assets.
- Practice recovery, change management and safety-aware decision-making.
- Map technical findings to risk, standards and operational outcomes.

# 2. Learning and engineering outcomes

A completed lab program should produce evidence of:
1. Correct process and system-under-test definition.
2. Network and control architecture.
3. Asset inventory and protocol map.
4. Baseline operating behavior.
5. Threat and risk scenario.
6. Approved lab safety and isolation controls.
7. Reproducible exercise steps.
8. Expected and observed results.
9. Detection and response evidence.
10. Recovery or rollback evidence.
11. Lessons learned and limitations.
12. Mapping to relevant security objectives and controls.

# 3. Lab design principles

## 3.1 Isolation by design

- Separate lab networks from enterprise and production networks.
- Use host-only or dedicated virtual networks where possible.
- Do not bridge an exercise network to a production VLAN.
- Disable unnecessary internet access.
- Use synthetic credentials, addresses, process data and certificates.
- Restrict management access to designated administrators.
- Capture and document all permitted inter-zone flows.
- Snapshot virtual machines before exercises.
- Define reset and destruction procedures.
- Store packet captures and logs in a controlled location.
- Never use real customer, plant or employee data without authorization.

## 3.2 Fidelity levels

| Level | Environment | Use | Limitations |
|---|---|---|---|
| L0 | Diagram, tabletop and synthetic logs | Governance, architecture and incident decisions | No live protocol behavior |
| L1 | Protocol simulator and synthetic PCAP | Protocol understanding and detection content | Does not reproduce physical process timing |
| L2 | Virtual PLC, HMI and process simulator | Logic, HMI and network exercises | Vendor-specific behavior may be incomplete |
| L3 | Integrated virtual plant and security stack | Multi-system scenarios and SOC validation | Simulation assumptions must be documented |
| L4 | Hardware-in-the-loop test station | Device compatibility and signal-level validation | Requires specialist facility and safety controls |
| L5 | Authorized replica or pre-production testbed | Change validation and high-fidelity testing | Requires formal ownership, approval and operational governance |

A higher fidelity level is not automatically safer or more accurate. State exactly what the environment models and what it omits.

# 4. Reference lab architecture

\`\`\`mermaid
flowchart TB
  subgraph LAB["Isolated OT cyber range"]
    subgraph CELL["Process cell"]
      SIM["Process simulator"]
      PLC["Virtual PLC / controller"]
      HMI["HMI / SCADA"]
      HIST["Historian / data service"]
      ENG["Engineering workstation"]
      SIM <-->|"Synthetic I/O"| PLC
      PLC <-->|"Control protocol"| HMI
      HMI --> HIST
      ENG --> PLC
    end
    subgraph MON["Security monitoring zone"]
      TAP["Virtual mirror / packet capture"]
      IDS["IDS / protocol analytics"]
      SIEM["Lab SIEM"]
      CASE["Case management"]
      TAP --> IDS --> SIEM --> CASE
    end
    subgraph RANGE["Exercise control zone"]
      ORCH["Scenario orchestrator"]
      DATA["Synthetic telemetry and evidence"]
      RESET["Snapshot and reset controller"]
      ORCH --> DATA
      ORCH --> RESET
    end
  end
  INSTR["Instructor / lab operator"] --> ORCH
  ANALYST["Learner / analyst"] --> CASE
\`\`\`

This is a logical training architecture. Actual network interfaces, virtual switches, routes, container networks and host controls must be explicitly documented. The scenario orchestrator must not have a route to production control assets.

## 4.1 Required zones

| Zone | Purpose | Example components | Access rule |
|---|---|---|---|
| Lab management | Manage virtual infrastructure | Hypervisor, orchestration | Administrator only |
| Process simulation | Model physical process | Simulator, sensor/actuator model | Lab-only flows |
| Control | Execute controller logic | PLC runtime or simulator | Explicitly scoped peers |
| Supervisory | Operator monitoring | HMI, SCADA, historian | Required process flows only |
| Engineering | Authorized programming and maintenance | Engineering workstation | Time-bound lab access |
| Monitoring | Observe and analyze traffic | IDS, packet capture, SIEM | Read-only collection preferred |
| Exercise delivery | Instructions and scoring | LMS, CTF, case portal | No direct control-plane access |

# 5. Build strategy and technology choices

Select tools according to learning outcomes, licensing, platform support, protocol fidelity, maintainability and instructor capability. Do not imply that a simulator is a certified replacement for a vendor controller or plant digital twin.

## 5.1 Representative platforms

| Platform / project | Publicly described purpose | Potential lab role | Validation required |
|---|---|---|---|
| OpenPLC | Open-source PLC runtime and tooling | Controller logic education and protocol integration | Runtime, driver, protocol and version compatibility |
| Factory I/O | 3D factory simulation for automation training | Process visualization and I/O-driven exercises | License, supported interfaces and simulation fidelity |
| FUXA | Web-based SCADA/HMI project | Operator interface and visualization exercises | Project maintenance, supported drivers and security posture |
| Scada-LTS | Open-source SCADA software | Supervisory monitoring exercises | Version status, deployment and protocol support |
| Node-RED | Flow-based application development | Synthetic telemetry, integration and orchestration | Secure configuration; do not expose editor broadly |
| Wireshark | Packet analysis | Offline protocol inspection | Use lab captures only |
| Zeek | Network security monitoring | Metadata and event generation | Validate protocol analyzers and logs |
| Suricata | Network IDS/IPS | Signature and protocol detection exercises | Use passive lab mode unless explicitly testing an isolated inline setup |
| Security Onion | Integrated security monitoring platform | SOC and network visibility lab | Sizing, version and sensor architecture |
| MITRE ATT&CK for ICS | Industrial adversary behavior knowledge base | Scenario and detection mapping | Technique applicability and evidence quality |
| C-DAC OT Security Test Station | Sandboxed OT security test environment with process simulation and test capabilities | Reference for higher-fidelity test-station design | Access, current availability and facility requirements |

Official resources:
- OpenPLC: https://openplcproject.com/
- Factory I/O: https://factoryio.com/
- FUXA: https://github.com/frangoteam/FUXA
- Scada-LTS: https://github.com/SCADA-LTS/Scada-LTS
- Node-RED: https://nodered.org/docs/
- Wireshark: https://www.wireshark.org/docs/
- Zeek: https://docs.zeek.org/
- Suricata: https://docs.suricata.io/
- Security Onion: https://docs.securityonion.net/
- MITRE ATT&CK for ICS: https://attack.mitre.org/matrices/ics/

C-DAC describes an OT Security Test Station with plant process simulation, signal generation, security analysis and a sandboxed virtualized environment. This is an example of a test-station approach, not a claim that the same capabilities are available as a downloadable software package. https://www.cdac.gov.in/index.aspx?id=product_details&productId=IndustrialControlSystemSecurityTestBed%28ICSSTB%29

## 5.2 Platform selection matrix

Evaluate each candidate against:
- Supported operating systems and hypervisors.
- CPU, memory, storage and network requirements.
- Licensing and permitted educational/commercial use.
- Maintenance activity and release history.
- Protocol support and implementation limits.
- Ability to export logs and packet captures.
- API and automation support.
- Authentication, authorization and audit.
- Secure defaults and update process.
- Documentation and instructor support.
- Reproducibility and reset capability.
- Known vulnerabilities and dependency exposure.

Do not select a platform solely because it is free or popular.

# 6. Process model catalogue

A process simulator should represent meaningful process variables and control objectives. Examples include:
- Tank level, inlet/outlet flow and pump state.
- Pressure, compressor state, valve position and alarms.
- Conveyor speed, motor state, interlocks and product count.
- Boiler temperature, pressure and permissive states.
- Water treatment stages, chemical dosing and pump operation.
- Substation measurement and breaker status as a simplified educational model.
- Building HVAC temperature, fan, damper and chiller status.
- Renewable energy generation and inverter telemetry as a simplified model.

For every process model document:
- Process purpose and boundary.
- Input and output variables.
- Units, ranges and engineering assumptions.
- Normal operating envelope.
- Alarm thresholds and rationale.
- Interlocks and permissives represented.
- Failure states and safe-state assumptions.
- Sampling and update rates.
- Model limitations.
- Responsible process engineer or instructor.

A simulated interlock is not a safety-rated function. Do not describe a teaching model as a validated SIS or safety instrumented function.

# 7. Industrial protocol lab catalogue

Build protocol exercises using simulators, synthetic traffic and controlled virtual networks. Protocol support varies by product and implementation.

| Protocol | Common learning focus | Lab evidence |
|---|---|---|
| Modbus TCP | Client/server exchanges, function codes, register model | PCAP, request/response explanation, allowlist |
| Modbus RTU | Serial framing, addressing and gateway behavior | Synthetic serial trace and gateway diagram |
| OPC UA | Client/server, certificates, security modes and user identity | Trust configuration and connection evidence |
| EtherNet/IP | CIP concepts, device discovery and industrial communication | Protocol map and traffic analysis |
| PROFINET | Industrial Ethernet architecture and device relationships | Network topology and engineering context |
| Siemens S7 communication | Controller engineering and data access concepts | Lab-only packet analysis and detection notes |
| DNP3 | Master/outstation concepts and utility telemetry | Synthetic event and protocol observation |
| IEC 60870-5-104 | Telecontrol communication and command/monitoring concepts | Synthetic session analysis |
| IEC 61850 | Substation automation concepts, MMS and GOOSE overview | Logical architecture and traffic identification |
| BACnet | Building automation services and device communication | HVAC simulation and network policy |
| MQTT | IIoT publish/subscribe and broker security | Topic ACL and certificate exercise |
| HART / WirelessHART | Instrumentation and field communication concepts | Architecture and security review |

Do not assume that protocol presence proves a particular control function or device role. Validate context against the process design and asset owner.

# 8. Lab lifecycle and quality workflow

\`\`\`mermaid
flowchart TD
  A["Define learning or validation objective"] --> B["Select process and fidelity level"]
  B --> C["Document scope, threat model and safety boundary"]
  C --> D["Build isolated topology"]
  D --> E["Baseline normal process and traffic"]
  E --> F["Create scenario and synthetic evidence"]
  F --> G["Run instructor validation"]
  G --> H{"Expected behavior reproducible?"}
  H -->|No| I["Fix model, data or instructions"]
  I --> G
  H -->|Yes| J["Release controlled exercise"]
  J --> K["Learner execution and evidence capture"]
  K --> L["Score, debrief and reset"]
  L --> M["Review content, dependencies and version"]
\`\`\`

## 8.1 Lab release gate

A lab must not be published until:
- Network isolation is tested.
- Scope and authorization are clear.
- Instructions are reproducible.
- Expected output is documented.
- Synthetic data is identified as synthetic.
- Safety and operational impacts are explained.
- Reset and cleanup work.
- Tool versions and licenses are recorded.
- References and mappings are reviewed.
- Instructor has completed a dry run.

# 9. Scenario engineering template

Every scenario must include:

| Field | Required content |
|---|---|
| Scenario ID | Stable identifier and version |
| Title | Clear operational scenario |
| Sector | Oil and gas, power, water, manufacturing, transport, buildings, etc. |
| Process | What the simulated process does |
| Environment | Components, topology and fidelity level |
| Learning objectives | Observable skills |
| Preconditions | Required accounts, snapshots and baseline |
| Threat model | Actor capability and access assumptions |
| Initial conditions | Synthetic process and network state |
| Exercise injects | Timed events or evidence supplied |
| Expected observations | Logs, alarms and process behavior |
| Defensive tasks | Investigate, validate, contain in lab, recover |
| Safety boundary | Explicit prohibited actions |
| Success criteria | Measurable outcomes |
| Evidence | PCAP, logs, screenshots, timeline, report |
| Reset | Exact restoration procedure |
| Mapping | ATT&CK for ICS, relevant standards and controls |
| Limitations | What the scenario does not model |

# 10. Practical lab programme

All exercises below use isolated simulated systems and synthetic data.

## Foundation track

### LAB-001: OT environment orientation
- Objective: Identify process, control, supervisory and enterprise boundaries.
- Build: Reference architecture with simulated assets.
- Tasks: Classify PLC, RTU, HMI, historian, engineering station, firewall and sensor.
- Evidence: Asset inventory and zone diagram.
- Pass criteria: Correctly identify system roles and trust boundaries.

### LAB-002: Purdue and zones-and-conduits mapping
- Objective: Translate a process diagram into security zones and communication conduits.
- Tasks: Define system-under-consideration boundary, flows, dependencies and trust assumptions.
- Evidence: Architecture diagram and flow register.
- Pass criteria: Every required flow has an owner and purpose.

### LAB-003: Asset inventory and confidence
- Objective: Reconcile synthetic passive observations with an engineering asset register.
- Tasks: Identify duplicates, stale records and unknown devices.
- Evidence: Reconciled inventory with source and confidence.
- Pass criteria: Unknowns and visibility gaps are explicit.

## Controller and process track

### LAB-004: Virtual PLC logic fundamentals
- Objective: Understand controller scan cycle, inputs, outputs, timers and state.
- Build: OpenPLC or equivalent simulator and synthetic I/O.
- Tasks: Review a benign sample program, trace state changes and document expected outputs.
- Evidence: Logic explanation and I/O map.
- Pass criteria: Explain process behavior without claiming safety certification.

### LAB-005: Tank level and pump process
- Objective: Connect a process model, controller and HMI.
- Build: Tank model, simulated level input, pump and valve outputs.
- Tasks: Observe normal operation, alarm states and recovery.
- Evidence: Process trend and alarm matrix.
- Pass criteria: Correctly explain process states and model assumptions.

### LAB-006: Conveyor and manufacturing cell
- Objective: Understand motor, sensor, interlock and operator workflow.
- Build: Factory simulation or equivalent model.
- Tasks: Map sensors, actuators, controller and operator station.
- Evidence: Asset and communication diagram.
- Pass criteria: Explain dependencies and safe operating assumptions.

### LAB-007: Water and wastewater process model
- Objective: Model treatment stages and remote telemetry.
- Build: Synthetic tanks, pumps, level and quality values.
- Tasks: Identify remote site dependencies and monitoring gaps.
- Evidence: Process flow, telemetry and incident worksheet.
- Pass criteria: Identify operational consequence without asserting real plant design.

## Protocol and network track

### LAB-008: Modbus TCP packet analysis
- Objective: Understand synthetic Modbus TCP exchanges.
- Tasks: Inspect provided PCAP offline, identify endpoints and explain request/response fields.
- Evidence: Annotated packet analysis.
- Pass criteria: Correct interpretation of the supplied trace.

### LAB-009: OPC UA trust and certificate review
- Objective: Understand endpoint security configuration.
- Tasks: Review a lab certificate trust list, security policy and user identity settings.
- Evidence: Configuration checklist and trust diagram.
- Pass criteria: Identify misconfiguration in the supplied lab only.

### LAB-010: Industrial network segmentation
- Objective: Design allowlisted communication between simulated zones.
- Tasks: Create a flow matrix and review hypothetical firewall rules.
- Evidence: Approved-rule proposal and test plan.
- Pass criteria: No unexplained broad access; each flow has an owner.

### LAB-011: Passive network monitoring
- Objective: Validate sensor visibility and limitations.
- Tasks: Compare synthetic expected flows with a supplied packet capture and sensor output.
- Evidence: Coverage matrix and blind-spot register.
- Pass criteria: Distinguish observed traffic from unobserved traffic.

## Detection and response track

### LAB-012: OT SOC baseline and anomaly triage
- Objective: Establish normal communication context and investigate synthetic anomalies.
- Tasks: Review baseline, asset criticality, time window and alert evidence.
- Evidence: Triage record with confidence and uncertainty.
- Pass criteria: Findings are evidence-based and process-aware.

### LAB-013: ATT&CK for ICS mapping
- Objective: Map a synthetic scenario to relevant ATT&CK for ICS techniques.
- Tasks: Select only techniques supported by scenario evidence and map defensive opportunities.
- Evidence: Technique mapping with source references.
- Pass criteria: No unsupported technique or attribution claims.

### LAB-014: Incident response tabletop
- Objective: Coordinate SOC, plant operations, engineering, safety and management.
- Injects: Unusual remote access, loss of telemetry and suspected engineering change.
- Tasks: Establish facts, preserve evidence, assess process state and obtain authorized decisions.
- Evidence: Timeline, decision log and communications record.
- Pass criteria: No unapproved disruptive action; escalation follows defined authority.

### LAB-015: Backup and recovery validation
- Objective: Validate recovery evidence for a simulated engineering project and server.
- Tasks: Restore in an isolated environment, verify integrity and compare to approved baseline.
- Evidence: Restore test report.
- Pass criteria: Recovery is demonstrated, not inferred from backup job status.

## Advanced engineering track

### LAB-016: Sensor failure and monitoring blind spot
- Objective: Understand monitoring dependency and data loss.
- Tasks: Review synthetic sensor-health events and missing telemetry.
- Evidence: Monitoring availability and response procedure.
- Pass criteria: SOC recognizes loss of visibility as a condition requiring investigation.

### LAB-017: Supplier remote access governance
- Objective: Design a controlled maintenance workflow.
- Tasks: Review identity, MFA, approval, jump access, session logs and expiry.
- Evidence: Remote access control matrix.
- Pass criteria: Access is named, scoped, approved, logged and revocable.

### LAB-018: Vulnerability applicability and prioritization
- Objective: Assess a synthetic vendor advisory against a simulated asset inventory.
- Tasks: Verify product/version match, exposure, process criticality and vendor mitigation.
- Evidence: Applicability and risk record.
- Pass criteria: No unsupported CVE-to-asset mapping.

### LAB-019: AI-assisted alert enrichment
- Objective: Use an AI assistant to summarize synthetic alerts with citations and uncertainty.
- Tasks: Provide controlled evidence, test for hallucination and prompt injection, require analyst verification.
- Evidence: Original alert, AI draft, corrections and approval record.
- Pass criteria: No autonomous production action; every claim traceable to evidence.

### LAB-020: Integrated industrial cyber range
- Objective: Run an end-to-end synthetic incident across process, network, SOC and governance.
- Tasks: Detect, investigate, coordinate, recover and conduct lessons learned.
- Evidence: Incident report, process impact analysis, control gaps and improvement plan.
- Pass criteria: Evidence-based response, approved decisions, validated recovery and documented limitations.

# 11. MITRE ATT&CK for ICS scenario mapping

Use ATT&CK for ICS as a knowledge base for describing adversary behavior, not as proof that an event occurred. Map a technique only when the scenario contains evidence supporting it.

For every mapping retain:
- Technique ID and name.
- ATT&CK version or retrieval date.
- Scenario step and evidence.
- Preconditions and assumptions.
- Relevant assets and process function.
- Detection opportunity.
- Preventive or mitigative controls.
- Known visibility limitations.
- Analyst confidence.

Official matrix: https://attack.mitre.org/matrices/ics/

MITRE's adversary emulation resources explain how public threat reporting can be translated into behavior-oriented defensive testing. Adapt any emulation to an isolated range and avoid reproducing harmful actions against real systems. https://attack.mitre.org/resources/adversary-emulation-plans/

# 12. Sector scenario catalogue

| Sector | Simulated process | Security learning objective |
|---|---|---|
| Upstream oil and gas | Well pad telemetry and remote pump | Remote access, RTU visibility and intermittent connectivity |
| Midstream pipeline | Pressure and flow monitoring | Telemetry integrity, remote site segmentation and escalation |
| Refinery | Simplified process unit | DCS dependencies, engineering access and change governance |
| LNG | Utility and process support model | Multi-system dependencies and recovery coordination |
| Power generation | Turbine auxiliary and generator monitoring model | Control network visibility and engineering workstation governance |
| Substation | IED and breaker status simulation | IEC 61850 concepts, event monitoring and configuration integrity |
| Solar and wind | Inverter and plant monitoring model | IIoT, remote operations and vendor access |
| Water treatment | Tank, pump and treatment stages | Process-aware incident triage and remote telemetry |
| Manufacturing | Conveyor, robot cell and packaging line | PLC/HMI dependencies, availability and production impact |
| Mining | Conveyor and ventilation monitoring model | Wireless/edge visibility and remote site resilience |
| Port | Gate, crane and terminal support model | IT/OT boundaries and supplier access |
| Airport | Baggage handling and facility automation model | Availability, system dependencies and coordinated response |
| Rail | Signalling support and operations telemetry model | Safety boundary, change governance and evidence handling |
| Building automation | HVAC, access and energy management | BACnet concepts, identity and network segmentation |
| Data centre facilities | Cooling, power and environmental monitoring | Availability, telemetry integrity and recovery |

These are educational abstractions, not operational design templates. Do not reproduce safety-critical logic or claim that a simplified model represents a certified system.

# 13. Digital twins: scope and assurance

A digital twin may represent geometry, process behavior, equipment state, telemetry, maintenance history or a combination. A 3D visualization alone is not necessarily a digital twin.

Record:
- Intended decision or engineering use.
- Physical system boundary.
- Model type and fidelity.
- Data sources and update frequency.
- Calibration and validation evidence.
- Model uncertainty.
- Assumptions and exclusions.
- Cybersecurity controls for data and interfaces.
- Ownership and lifecycle.
- Change synchronization process.

## 13.1 Twin categories

| Category | Representation | Typical use |
|---|---|---|
| Asset twin | Individual equipment | Lifecycle and maintenance context |
| Process twin | Process variables and behavior | Operating scenario analysis |
| System twin | Interconnected control and support systems | Dependency and architecture analysis |
| Network twin | Communication topology and flows | Segmentation and monitoring design |
| Security twin | Asset, exposure and control context | Risk and detection analysis |
| Training twin | Simplified process and operator interface | Education and scenario exercises |

## 13.2 Twin data security

- Authenticate data producers and consumers.
- Protect APIs and message brokers.
- Validate data provenance and timestamps.
- Separate simulation from live control paths.
- Restrict write-back capability.
- Monitor model drift and stale data.
- Protect engineering and process models.
- Record model and configuration versions.
- Test loss-of-connectivity behavior.
- Review cloud, vendor and cross-border data flows.

# 14. Purple-team and defensive validation

Purple-team exercises should validate defensive hypotheses in an isolated environment. The aim is to improve telemetry, detection, response and recovery, not to maximize disruption.

A safe exercise plan includes:
- Written scope and authorization.
- Asset and network boundary.
- Scenario objectives and prohibited actions.
- Synthetic or lab-only indicators.
- Approved test actions.
- Expected telemetry.
- Detection owner and observer.
- Stop conditions.
- Evidence collection.
- Reset and recovery.
- Lessons learned and control changes.

# 15. Scoring and competency model

Assess observable skills rather than tool familiarity alone.

| Competency | Beginner | Practitioner | Advanced |
|---|---|---|---|
| Process understanding | Identifies basic process elements | Explains dependencies and operating states | Evaluates model fidelity and consequence |
| Asset visibility | Reads an inventory | Reconciles multiple sources | Quantifies confidence and blind spots |
| Protocol analysis | Identifies basic endpoints | Explains supplied transactions | Builds validated detection and limitations |
| Architecture | Identifies zones | Designs flows and boundaries | Evaluates complex dependencies and failure modes |
| Detection | Reviews alerts | Correlates process and network context | Validates analytics and detection coverage |
| Incident response | Follows a playbook | Coordinates technical triage | Leads cross-functional decisions and recovery |
| Governance | Recognizes approval needs | Produces evidence and change records | Integrates risk, assurance and lifecycle |

Suggested scoring:
- 0: Not attempted.
- 1: Attempted with substantial guidance.
- 2: Completed with minor errors.
- 3: Independently completed with evidence.
- 4: Explains limitations, validates results and improves the method.

Define pass thresholds per course and do not treat a score as a professional certification.

# 16. Evidence pack and reporting template

Every exercise should produce a consistent evidence pack:
1. Exercise ID, version and date.
2. Learner and instructor.
3. Lab architecture and fidelity level.
4. Asset and software versions.
5. Authorization and safety statement.
6. Initial state and scenario injects.
7. Steps performed.
8. Raw logs and packet capture references.
9. Screenshots with timestamps where useful.
10. Observations and analysis.
11. Expected versus actual behavior.
12. Detection and response result.
13. Recovery and reset evidence.
14. Standards or technique mapping with caveats.
15. Limitations and improvement actions.

Preserve original evidence separately from analyst notes. Hash exported evidence where integrity assurance is required and record collection method and custody.

# 17. Lab operations and maintenance

Maintain:
- Lab owner and instructor.
- Asset and VM inventory.
- Software bill of materials where available.
- Image and snapshot versions.
- License and usage restrictions.
- Network isolation test results.
- Credential management.
- Backup and restore.
- Vulnerability and patch process.
- Change history.
- Student access and expiry.
- Data retention and deletion.
- Incident and misuse procedure.
- Annual content review.

Do not leave default credentials, exposed management interfaces or public cloud services accessible after an exercise.

# 18. Infrastructure sizing and deployment patterns

Sizing depends on simulator fidelity, number of concurrent learners, packet capture volume, retention and endpoint count. Do not use a universal hardware specification.

Estimate:
- Concurrent learners and isolated lab instances.
- vCPU and memory per VM/container.
- Storage for images, snapshots, logs and PCAP.
- Network throughput and packet capture rate.
- Backup and restore time.
- GPU requirements only where a workload genuinely needs them.
- Hypervisor and license constraints.
- Instructor and support capacity.

Deployment options:
- Single workstation for foundational exercises.
- Dedicated virtualization server for class labs.
- Isolated on-premises cyber range.
- Cloud-hosted disposable labs with strict network isolation.
- Hardware-in-the-loop specialist test station.
- Hybrid delivery with central LMS and isolated execution environment.

Cloud deployment requires region, residency, access, egress, secrets, tenant isolation, logging and deletion review. Never expose a simulated controller management interface directly to the public internet.

# 19. AI agents for lab orchestration and instruction

AI can assist with exercise creation, synthetic evidence generation, hint delivery, rubric-based feedback and report drafting. It must not have unrestricted access to hypervisors, networks or control devices.

\`\`\`mermaid
flowchart TD
  AUTHOR["Instructor defines approved scenario"] --> VALIDATE["Scenario schema and safety validator"]
  VALIDATE --> ORCH["Lab orchestration service"]
  ORCH --> ENV["Disposable isolated lab"]
  ENV --> TELEMETRY["Synthetic logs and exercise events"]
  TELEMETRY --> TUTOR["AI tutor and evidence explainer"]
  TELEMETRY --> SCORE["Rubric-based scoring assistant"]
  TUTOR --> LEARNER["Learner"]
  SCORE --> REVIEW["Instructor review"]
  LEARNER --> SUBMIT["Evidence submission"]
  SUBMIT --> REVIEW
  REVIEW --> RESET["Authorized reset service"]
\`\`

Agent controls:
- Scenario allowlist and signed lab definitions.
- No production network route.
- No production credentials.
- Least-privilege orchestration API.
- Human approval for environment creation and destructive reset.
- Per-learner tenant isolation.
- Resource and time quotas.
- Prompt-injection handling for uploaded evidence.
- Source and rubric citations.
- Human-reviewed scores.
- Full audit trail.
- Kill switch and cleanup process.

# 20. Standards and framework mapping

This playbook supports educational and validation activities. It does not claim that completing a lab demonstrates organizational compliance or certification.

| Reference | Potential lab relationship | Mapping limitation |
|---|---|---|
| NIST SP 800-82 Rev. 3 | OT architecture, risk, safeguards and monitoring | Guidance, not a lab certification scheme |
| NIST SP 800-82 Rev. 4 Initial Public Draft | Emerging guidance and expanded sector coverage | Draft only; do not treat as final requirement |
| ISA/IEC 62443-2-1 | Asset owner security program concepts | Lab does not demonstrate a complete security program |
| ISA/IEC 62443-2-4 | Service provider practice concepts | Training exercise is not provider conformity evidence |
| ISA/IEC 62443-3-2 | System boundary, zones, conduits and risk | Lab scope is not a site risk assessment |
| ISA/IEC 62443-3-3 | System security requirement concepts | Simulator does not establish system security level |
| ISA/IEC 62443-4-1 | Secure product development concepts | Not a supplier lifecycle audit |
| ISA/IEC 62443-4-2 | Component capability concepts | Simulator is not a certified component |
| MITRE ATT&CK for ICS | Behavior and detection mapping | Technique mapping requires evidence |
| NIST CSF 2.0 | Governance and security outcome discussion | A training result is not an organizational profile |

For formal mapping, preserve standard edition, clause identifier, exact applicability, evidence requirement, owner and assessor decision. Consult licensed standards and the authoritative publisher catalogue.

# 21. Legal, ethical and safety requirements

- Obtain written authorization for all testing.
- Use only lab-owned or explicitly approved assets.
- Follow applicable laws, contracts and acceptable-use requirements.
- Respect software licenses and intellectual property.
- Do not use real operational credentials or secrets.
- Do not connect a lab to production without formal approval and engineering design.
- Do not reproduce destructive payloads or uncontrolled denial-of-service scenarios.
- Do not interact with safety systems or process actuators outside approved specialist facilities.
- Stop an exercise if isolation, scope or process safety is uncertain.
- Report accidental exposure or unintended connectivity immediately.

# 22. References and further reading

1. **NIST SP 800-82 Rev. 3, Guide to Operational Technology Security, September 2023.** Final publication and baseline OT security guidance. https://csrc.nist.gov/pubs/sp/800/82/r3/final
2. **NIST SP 800-82 Rev. 4 Initial Public Draft, September 21, 2026.** Draft publication; comment deadline November 30, 2026. https://csrc.nist.gov/pubs/sp/800/82/r4/ipd
3. **NISTIR 8089, An Industrial Control System Cybersecurity Performance Testbed.** Testbed approach and performance measurement context. https://doi.org/10.6028/NIST.IR.8089
4. **C-DAC OT Security Test Station.** Process simulation, signal generation, security analysis and sandboxed test environment description. https://www.cdac.gov.in/index.aspx?id=product_details&productId=IndustrialControlSystemSecurityTestBed%28ICSSTB%29
5. **C-DAC Critical Infrastructure Security Training Kit.** Simulated SCADA training environment and competency-based exercises. https://www.cdac.in/index.aspx?id=product_details&productId=CriticalInfrastructureSecurityTrainingKit
6. **MITRE ATT&CK for ICS.** https://attack.mitre.org/matrices/ics/
7. **MITRE Adversary Emulation Plans.** https://attack.mitre.org/resources/adversary-emulation-plans/
8. **UWE Cyber Physical Systems Security interactive simulation project.** Educational use of Factory I/O, OpenPLC and ScadaBR. https://uwe-cyber.github.io/cpss/
9. **OpenPLC documentation and project resources.** https://openplcproject.com/
10. **Factory I/O.** https://factoryio.com/
11. **Zeek documentation.** https://docs.zeek.org/
12. **Suricata documentation.** https://docs.suricata.io/

# 23. Revision history

| Version | Date | Change | Status |
|---|---|---|---|
| 1.0 | 2026-11-17 | Initial labs, digital twin and industrial simulation playbook | Engineering reference |

# 24. Expansion backlog

1. Reproducible build guides for each selected lab platform and version.
2. Detailed isolated network diagrams and firewall flow matrices.
3. Synthetic PCAP library with provenance and expected analysis.
4. Process model specifications and instructor answer keys.
5. Per-lab scoring rubrics and evidence templates.
6. Container and VM image hardening baseline.
7. Sector-specific scenario packs.
8. Digital twin validation and model assurance worksheet.
9. AI agent threat model and orchestration API security design.
10. Lab content CI validation, dependency scanning and release signing.

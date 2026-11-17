# OT and ICS Foundations

## What is operational technology?

Operational technology comprises programmable systems and devices that interact with the physical environment, or manage devices that interact with the physical environment. They detect or cause changes through monitoring and control of devices, processes, and events.

Examples include industrial controllers, supervisory systems, building management systems, process instrumentation, power automation, and physical access or environmental control systems.

## OT, IT, and cyber-physical systems

Information technology commonly supports information processing, business applications, and enterprise services. OT supports or directly influences physical processes. The distinction is useful but not absolute: modern industrial environments depend on identity services, virtualization, cloud platforms, data pipelines, remote access, and enterprise systems.

Cyber-physical systems combine computational elements with sensing, communication, and physical actuation. Their cybersecurity must account for both digital and physical consequences.

## Core system types

- **PLC:** Executes control logic for machines and processes.
- **RTU:** Collects telemetry and supports remote monitoring or control, often across geographically distributed sites.
- **DCS:** Provides distributed process control, operator interfaces, and supervisory functions.
- **SCADA:** Provides supervisory monitoring and control across distributed assets.
- **HMI:** Presents process information and operator controls.
- **SIS:** Implements safety instrumented functions to achieve or maintain a safe state.
- **IED:** Performs protection, control, and automation functions, especially in power systems.
- **Historian:** Stores time-series process data for operations, engineering, and analysis.

## OT security objectives

OT security must protect:
- Safety of people and the environment
- Availability and continuity of physical processes
- Integrity of control logic, configurations, measurements, and commands
- Visibility and operator decision-making
- Confidentiality of sensitive engineering and operational information
- Recoverability and resilience

The priority and trade-offs depend on the process and hazard context. Availability is often critical, but integrity and safety can be equally or more consequential.

## Why OT differs from typical IT

- Long equipment lifecycles and legacy platforms
- Vendor-specific protocols and engineering tools
- Real-time and deterministic communication requirements
- High cost and risk of downtime
- Limited patch windows and constrained maintenance access
- Safety and environmental consequences
- Physical dependencies and manual fallback procedures
- Fragile devices and risk from active scanning or changes

## Common architecture elements

An industrial environment may include field devices, controllers, supervisory systems, operations management, an industrial DMZ, enterprise services, remote sites, vendors, and cloud or IIoT platforms. The actual architecture depends on process, scale, engineering, and risk.

## Security lifecycle

Security must be considered from procurement and design through integration, commissioning, operations, maintenance, incident response, recovery, replacement, and decommissioning.

## Essential questions for any OT assessment

1. What physical process is being controlled or monitored?
2. What happens if the asset is unavailable, inaccurate, or manipulated?
3. Who owns the asset and approves changes?
4. What systems and services does it depend on?
5. Which zones and conduits can reach it?
6. Which engineering and remote access paths exist?
7. How are configurations backed up and restored?
8. How are changes detected and validated?
9. What are the safe operating and recovery procedures?
10. Which standards and regulations actually apply?

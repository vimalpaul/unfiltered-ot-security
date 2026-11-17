# OT Asset Inventory and Criticality

## Objective

Establish a reliable, maintained view of the assets and dependencies required to operate, monitor, protect, and recover industrial processes.

## Asset classes

Include, where present:
- Sensors, transmitters, analyzers, actuators, valves, drives, and motor control equipment
- PLCs, PACs, RTUs, remote I/O, controllers, and embedded devices
- DCS controllers, operator stations, application servers, and engineering stations
- SCADA masters, front-end processors, telemetry gateways, and remote site equipment
- HMI panels, historians, alarm servers, batch systems, and manufacturing execution systems
- SIS controllers, safety instrumented functions, fire and gas systems, and protection relays
- Industrial switches, routers, firewalls, serial gateways, wireless access points, and time sources
- Virtualization hosts, hypervisors, storage, backup systems, and OT support infrastructure
- Remote access platforms, identity services, jump hosts, and vendor support appliances
- IIoT gateways, edge platforms, cloud connectors, and data brokers

## Minimum asset record

| Field | Purpose |
|---|---|
| Asset ID | Stable unique identifier |
| Site and process | Physical and operational context |
| Zone and conduit | Network security context |
| Asset type and function | What it does in the process |
| Manufacturer, model, version | Product identity |
| Firmware and software | Exact version where known |
| Network identity | Approved addresses, MAC, hostname, protocol |
| Owner and support party | Accountability |
| Criticality | Consequence-based rating with rationale |
| Safety relationship | Safety function, dependency, or no known relationship |
| Dependencies | Power, network, identity, time, server, vendor services |
| Exposure | Reachability and remote access paths |
| Lifecycle | Supported, end-of-support, spare, retired |
| Backup and recovery | Method, last test, responsible party |
| Evidence and confidence | Source and accuracy of the record |
| Last verified | Actual date and verification method |

Do not publish sensitive facility-specific inventory data in a public repository. Use synthetic examples.

## Criticality assessment

Assess consequence, not just device price or IT data sensitivity. Consider:
- Personnel safety and hazardous process consequences
- Environmental release or damage
- Loss of control or visibility
- Essential service interruption
- Equipment damage and repair lead time
- Product quality and batch integrity
- Recovery time and spare availability
- Dependencies and common points of failure

A criticality rating must have documented criteria, accountable owner, and review date.

## Discovery methods

Prefer approved sources such as engineering records, configuration management databases, procurement records, network diagrams, switch and firewall configurations, passive network monitoring, vendor tools, and operator validation.

Active discovery can affect fragile devices or networks. Require authorization, scope, rate limits, maintenance planning, vendor guidance, and operational approval. Never assume that a ping, port scan, protocol query, or inventory agent is harmless.

## Lifecycle governance

Reconcile the inventory after commissioning, maintenance, engineering changes, vendor access, incidents, replacement, and decommissioning. Preserve configuration baselines and secure disposal evidence. Record unknown assets as investigation items rather than silently excluding them.

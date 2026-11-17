# Industrial Sectors and Use Cases

## Sector model

The same technology can create different risks depending on process, safety function, operating model, and consequences. Sector pages must describe process context before prescribing security controls.

## Oil and gas

### Upstream
Exploration, drilling, well control, offshore platforms, onshore production, gathering systems, remote telemetry, and production facilities.

Key OT assets may include PLCs, RTUs, DCS, wellhead controllers, safety systems, compressor controls, telemetry, and engineering workstations.

Security themes: remote field access, satellite and radio links, contractor access, legacy devices, process safety, availability, environmental consequence, and loss of communications.

### Midstream
Pipelines, terminals, storage, compressor and pump stations, metering, leak detection, and pipeline SCADA.

Security themes: geographically distributed sites, telemetry integrity, remote operations, communications resilience, unauthorized setpoint changes, and safe degraded operation.

### Downstream
Refineries, petrochemical plants, LNG facilities, gas processing, and terminals.

Security themes: complex DCS environments, SIS independence, engineering change control, vendor maintenance, historian and MES connectivity, and high-consequence process disruption.

## Power and energy

Generation, transmission, distribution, substations, protection and control, renewable generation, battery storage, and grid operations.

Security themes: protection relay integrity, substation automation, time synchronization, IEC 61850 engineering, remote access, control center resilience, and coordinated IT/OT response.

## Water and wastewater

Intake, treatment, chemical dosing, pumping, storage, distribution, wastewater treatment, and telemetry.

Security themes: public health and environmental consequence, remote pump stations, chemical process integrity, legacy PLCs, cellular telemetry, and safe manual operation.

## Manufacturing

Discrete and process manufacturing, robotics, packaging, assembly, MES, quality systems, and industrial edge platforms.

Security themes: production availability, recipe and batch integrity, engineering workstations, vendor support, removable media, and IT/OT data exchange.

## Mining and metals

Open-pit and underground operations, conveyors, crushers, ventilation, dewatering, fleet management, processing plants, and smelters.

Security themes: remote and harsh environments, autonomous equipment, safety systems, wireless coverage, and supply chain dependency.

## Transportation and logistics

Rail, metro, airports, ports, maritime, tunnels, traffic systems, baggage handling, and logistics automation.

Security themes: operational continuity, passenger and worker safety, signaling or navigation integrity, third-party access, and distributed control systems.

## Buildings and campuses

Building management systems, HVAC, elevators, access control, fire and life-safety systems, energy management, and data center facilities.

Security themes: converged IT and facility networks, internet-connected controllers, shared vendors, physical security dependencies, and life-safety system separation.

## Required sector use-case format

Each use case should include:
1. Sector and process overview
2. Representative process flow
3. Reference architecture and trust boundaries
4. Asset inventory and criticality
5. Safety, environmental, and business consequences
6. Threat scenarios and attack paths
7. Preventive and detective controls
8. Operational response and recovery
9. Relevant standards and jurisdiction-specific requirements
10. Assumptions, limitations, and sources

All architectures must be labeled illustrative unless based on a cited public reference. Never publish sensitive facility details.

# Oil, Gas, LNG, and Petrochemical OT Security

## Scope

This reference covers upstream, midstream, downstream, LNG, gas processing, terminals, and petrochemical facilities. Site-specific process hazard analysis and engineering authority remain controlling.

## Process and asset landscape

### Upstream
- Drilling and well control systems
- Wellhead and production control
- Offshore platform control networks
- Remote telemetry and unmanned facilities
- Compressor and pumping systems
- Safety and fire-and-gas systems

### Midstream
- Pipeline SCADA and leak detection
- Compressor and pump stations
- Metering and custody transfer
- Storage terminals and tank farms
- Remote communications and telemetry

### Downstream and LNG
- Refinery and gas processing DCS
- LNG liquefaction and regasification
- Loading and unloading systems
- Tank gauging and terminal automation
- SIS, burner management, and fire-and-gas systems
- Historian, laboratory, maintenance, and production systems

## Representative architecture

A typical conceptual flow may include field instruments and actuators connected to controllers, area control and operator systems, site supervisory services, an industrial DMZ, and approved enterprise services. Remote facilities may communicate through radio, cellular, satellite, microwave, or leased links. Actual designs vary widely.

## High-priority threat scenarios

- Compromise of a vendor remote access account
- Engineering workstation compromise followed by unauthorized project change
- Loss of SCADA visibility across remote pipeline sites
- Manipulation of process measurements or setpoints
- Ransomware affecting supporting Windows infrastructure
- Compromise of historian or data exchange services
- Unauthorized access between business and control zones
- Loss of communications to remote assets
- Compromise of safety-related engineering or support paths

These are scenarios for risk analysis, not claims about a specific facility or incident.

## Security requirements to evaluate

- Complete asset and communications inventory
- Segmentation between corporate, DMZ, control, remote site, and safety-related environments
- Strong vendor and contractor access governance
- Engineering change control and controller logic backup
- Passive monitoring of critical conduits
- Secure time synchronization
- Offline recovery capability
- Resilient communications and documented loss-of-link behavior
- Product lifecycle and spare-parts strategy
- Coordination between cybersecurity, process safety, operations, and engineering

## Operational constraints

A control network action can affect production, pressure, temperature, flow, rotating equipment, emissions, and safety functions. Active scanning, packet injection, controller downloads, or network isolation must be subject to site authorization, process safety review, vendor guidance, and approved test plans.

## Use-case template

For each facility type, document process description, simplified PFD/P&ID context, asset classes, zones and conduits, dependencies, threat scenarios, safety and environmental consequences, preventive and detective controls, response and recovery, applicable standards, jurisdiction-specific requirements, and sources.

## Relevant reference families

- IEC 62443 series
- NIST SP 800-82
- MITRE ATT&CK for ICS
- Applicable national critical infrastructure and energy-sector requirements
- Vendor security advisories for deployed equipment

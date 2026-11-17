# Power Generation, Grid, and Substation OT Security

## Scope

Generation, transmission, distribution, substations, control centers, renewables, battery energy storage, and distributed energy resources.

## System landscape

- Plant DCS and turbine or generator control
- Energy management and distribution management systems
- SCADA masters and remote terminal units
- Substation automation and protection IEDs
- IEC 61850 station and process bus environments
- Protection relays and engineering tools
- Time synchronization and phasor measurement systems
- Renewable plant controllers and inverter systems
- Battery energy storage management and safety systems
- Telecom, microwave, fiber, and remote access infrastructure

## Security objectives

Preserve safe and reliable generation and grid operation, protection coordination, command authenticity, visibility, time integrity, and recovery capability.

## Threat scenarios

- Unauthorized relay settings or protection configuration changes
- Compromise of substation engineering workstation
- Loss of SCADA visibility or remote control
- Unauthorized GOOSE or MMS traffic within a substation network
- Compromise of time synchronization source
- Remote access abuse by contractor or supplier
- Malware affecting control center support systems
- Supply chain compromise of firmware or engineering software
- Coordinated disruption across distributed energy assets

## Defensive engineering

- Maintain authoritative asset, firmware, settings, and network inventories.
- Separate enterprise, control center, substation, protection, and vendor access paths based on risk.
- Protect engineering access and settings files.
- Monitor approved communication patterns and unexpected changes.
- Maintain verified backups of relay settings, controller logic, and system configurations.
- Validate time sources and monitor loss or drift.
- Coordinate cybersecurity changes with grid operations and protection engineering.
- Test recovery and local fallback procedures.

## Protocol considerations

IEC 61850 deployments may use MMS, GOOSE, and sampled values, with different timing and availability characteristics. Security controls and monitoring must be compatible with the engineering design and latency requirements. Do not inject test traffic into production protection networks without formal authorization and a validated test plan.

## Incident response priorities

Coordinate with system operators and protection engineers. Evaluate grid stability, protection coordination, essential service impact, and safe operating states before containment. A cyber alert does not automatically justify blocking traffic or isolating a relay.

## Reference families

IEC 61850, IEC 62351 where applicable, IEC 62443, NIST SP 800-82, relevant national grid codes, energy regulator requirements, and equipment vendor advisories.

# Safe OT Lab Engineering

## Purpose

Establish isolated, repeatable learning and validation environments without exposing production processes or third-party systems.

## Lab tiers

1. Protocol-only simulation using synthetic packet captures and protocol emulators.
2. Virtualized PLC, HMI, historian, and SCADA simulation.
3. Dedicated hardware test bench with non-production controllers.
4. Digital twin or process simulator connected only to the isolated lab network.
5. Purple-team exercise using pre-approved scenarios and synthetic telemetry.

## Isolation requirements

- Separate lab networks from corporate and production OT.
- No bridged or routed path to live industrial assets by default.
- Use synthetic identities, credentials, and process data.
- Disable unnecessary external access.
- Control snapshots, backups, and reset procedures.
- Log lab changes and preserve exercise evidence.
- Clearly label simulated devices and data.
- Ensure cloud lab environments do not expose management interfaces publicly.

## Exercise design

Each exercise should define learning objectives, prerequisites, architecture, asset list, safe starting state, scenario, permitted actions, prohibited actions, expected observations, defensive learning outcomes, reset procedure, and evaluation rubric.

## Scenario catalogue

- Passive discovery of synthetic OT traffic
- Modbus function and communication analysis using capture files
- OPC UA certificate and trust configuration review
- Industrial DMZ rule review
- Engineering workstation hardening
- PLC project integrity and backup validation
- Remote access approval workflow
- OT alert triage using synthetic logs
- Incident timeline and recovery planning
- ATT&CK for ICS technique mapping

## Prohibited lab-to-production behavior

Do not reuse lab targets, credentials, payloads, scripts, or scanning profiles against production systems without separate written authorization and site-specific approval. Lab success does not prove a technique is safe or applicable to a real vendor deployment.

## Exercise report

Record environment version, tool versions, test data origin, actions performed, expected and actual results, limitations, safety controls, cleanup, and reviewer.

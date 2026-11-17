# OT SOC and Detection Engineering

## Mission

Detect malicious, unauthorized, unsafe, or anomalous activity while preserving process visibility, availability, and engineering safety.

## Telemetry sources

- Passive network sensors and approved packet captures
- Firewall, router, switch, and industrial DMZ logs
- Remote access and jump-host session records
- Windows and Linux engineering workstation logs
- HMI, SCADA, DCS, historian, and application audit logs
- Identity, authentication, and privileged access records
- Endpoint protection and application control events where supported
- PLC logic change and controller diagnostic records where available
- Physical access and maintenance records
- Time synchronization and backup systems

## Detection engineering lifecycle

1. Define the process and threat scenario.
2. Identify the relevant assets and expected communication baseline.
3. Confirm telemetry exists and is reliable.
4. Write a detection hypothesis and analytic logic.
5. Identify false positives and benign engineering activity.
6. Test against representative lab or replay data.
7. Define severity, triage questions, and escalation owner.
8. Document response actions and prohibited actions.
9. Deploy through change control.
10. Measure quality and review after incidents or system changes.

## High-value detection themes

- New or unexpected asset on a control network
- New conduit or unexpected cross-zone communication
- Remote access outside approved windows
- Shared or unusual privileged account use
- Engineering workstation execution anomalies
- PLC project download or logic change
- Unexpected mode, setpoint, or configuration changes
- Unauthorized removable media activity
- Unusual protocol function or service usage
- Loss of historian, sensor, or monitoring visibility
- Time synchronization anomalies
- Backup deletion or integrity failure
- SIS boundary or safety-system access anomalies

## Alert triage

For every alert, establish:
- What asset and process are involved?
- Is the activity expected and approved?
- Is there a current maintenance or engineering change?
- Is the event isolated or part of a broader sequence?
- What is the potential process, safety, environmental, and business impact?
- Which engineering or operations authority must be consulted?
- What evidence can be collected without disrupting the process?

## Response guardrails

SOC analysts must not automatically isolate, reboot, block, scan, or modify industrial assets based solely on an alert. Response actions must follow pre-approved playbooks and decision authority. Coordinate with control room, operations, engineering, safety, and incident command.

## Metrics

Track asset visibility, critical conduit coverage, telemetry health, detection validation, triage time, false-positive rate, playbook exercise results, unresolved high-risk exposures, and recovery readiness. Metrics should not incentivize unsafe automation or indiscriminate alert volume.

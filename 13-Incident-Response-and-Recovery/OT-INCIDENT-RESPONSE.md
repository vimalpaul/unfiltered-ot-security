# OT Incident Response and Recovery

## Purpose

Provide an OT-aware incident response model that coordinates cybersecurity with operations, engineering, process safety, environmental, and business continuity functions.

## Governing principles

- Protect people and the environment first.
- Preserve safe process operation and essential services.
- Follow site emergency, process safety, and operational procedures.
- Do not assume that IT containment actions are safe for OT.
- Maintain clear decision authority and communications.
- Preserve evidence where feasible without delaying safety actions.

## Preparation

Maintain:
- OT asset and dependency inventories
- Current network and process diagrams
- Contact and escalation lists
- Vendor support and emergency access arrangements
- Approved isolation and degraded-operation procedures
- Offline and tested backups of engineering configurations
- Golden images and recovery media where appropriate
- Spare parts and replacement controller strategy
- Time synchronization and logging arrangements
- Exercise plans and lessons learned

## Incident phases

### 1. Detect and report
Validate the alert using trusted telemetry and consult operations. Record time, source, affected systems, observed behavior, and confidence.

### 2. Triage and classify
Determine whether the event affects confidentiality, integrity, availability, process control, safety, environment, or essential service delivery. Identify affected zones and dependencies.

### 3. Escalate and coordinate
Activate the incident structure. Include operations, control engineering, process safety, cybersecurity, IT, legal, communications, vendor, and regulator contacts as appropriate.

### 4. Contain safely
Use pre-approved actions. Options may include restricting remote access, disabling compromised accounts, blocking a conduit, or moving to a safe operating mode, but only after engineering and operational impact assessment and approval by the designated authority.

### 5. Eradicate and recover
Restore from known-good backups, validate controller logic and configurations, verify device integrity, and recover in a controlled sequence. Confirm process behavior and safety functions with qualified personnel.

### 6. Learn and improve
Preserve timeline and evidence, identify root causes and contributing conditions, update detections and controls, and track corrective actions.

## Scenario playbooks to develop

- Ransomware affecting enterprise services connected to OT
- Compromised engineering workstation
- Unauthorized PLC logic or parameter change
- Loss of SCADA visibility
- Vendor remote access compromise
- OT network segmentation failure
- Malware on removable media
- Compromised historian or data broker
- Substation or remote site communications disruption
- Suspected SIS compromise

## Decision authority

The site emergency plan, process safety procedures, and incident command model determine who can order operational changes. Cybersecurity staff should not independently direct process shutdown, safety bypass, controller isolation, or restart unless explicitly authorized and competent under site procedures.

## Recovery validation

Verify asset identity, firmware and configuration, logic integrity, communications, alarms, interlocks, time synchronization, backups, monitoring, remote access, and operator visibility. Document residual risk and formal handover to operations.

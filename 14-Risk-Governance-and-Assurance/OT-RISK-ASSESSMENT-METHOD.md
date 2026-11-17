# OT Cybersecurity Risk Assessment Method

## Purpose

Provide a repeatable method to assess cyber risk in industrial environments while explicitly considering safety, process, environmental, and availability consequences.

## Assessment unit

Assess a defined process, system, zone, conduit, asset group, or service. Avoid scoring an entire plant as one undifferentiated object.

## Inputs

- Process description and operating modes
- Asset and dependency inventory
- Network and data-flow diagrams
- Safety and hazard studies as authorized
- Threat and vulnerability information
- Vendor support and lifecycle data
- Existing safeguards and operating procedures
- Business, environmental, and service impact criteria
- Legal, regulatory, and contractual requirements

## Workflow

1. Establish scope, boundaries, assumptions, and stakeholders.
2. Identify process functions and critical services.
3. Identify assets, dependencies, and trust boundaries.
4. Identify threat scenarios and failure modes.
5. Identify vulnerabilities, exposure, and threat capability.
6. Analyze consequences across safety, environment, operations, quality, finance, and reputation.
7. Evaluate existing safeguards and their independence.
8. Estimate likelihood using a documented method and evidence.
9. Determine inherent and residual risk.
10. Assign risk owner and treatment decision.
11. Define actions, due dates, evidence, and review triggers.

## Consequence dimensions

Do not collapse all impact into a generic data confidentiality score. Consider:
- Personnel safety
- Process safety and loss of control
- Environmental release or damage
- Essential service disruption
- Equipment damage
- Product quality and batch integrity
- Operational downtime and recovery duration
- Financial and contractual impact
- Regulatory and legal consequences

## Treatment options

Avoid, reduce, transfer, or accept risk. Acceptance must be made by an authorized risk owner and must include rationale, compensating safeguards, residual risk, expiry or review date, and escalation criteria.

## Risk register fields

Risk ID, process, asset or zone, scenario, threat source, vulnerability, existing safeguards, consequence analysis, likelihood rationale, inherent rating, residual rating, treatment, owner, action, due date, evidence, approval, and review date.

## Important limitations

A numeric score does not replace engineering judgment, hazard analysis, safety lifecycle obligations, or regulator requirements. Do not use CVSS as the sole OT risk score. Do not treat the presence of a control as evidence that it is effective.

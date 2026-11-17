# OT Security Assessment Methodology

## Purpose

Define a safe, risk-based structure for authorized OT security assessments. Scope and test depth must be agreed with the asset owner and engineering authority.

## Assessment phases

### 1. Authorization and planning
Confirm written authorization, business purpose, assets, sites, dates, contacts, prohibited actions, escalation path, and stop-work criteria.

### 2. Safety and operational review
Review process context, operating modes, maintenance windows, safety constraints, environmental concerns, and impact of loss of communications or device performance.

### 3. Architecture and documentation review
Review network diagrams, zones, conduits, asset inventory, remote access paths, data flows, supplier access, and dependencies.

### 4. Passive discovery and observation
Use approved records and passive methods to identify assets, protocols, communications, and unexpected paths. Validate observations with engineering.

### 5. Configuration and control review
Review firewall rules, remote access, identity, engineering workstation hardening, backup, logging, patch governance, change management, and supplier controls.

### 6. Vulnerability and exposure analysis
Correlate exact product versions and configurations with vendor advisories and trusted vulnerability sources. Avoid assumptions from banner-only identification.

### 7. Controlled validation
Any active test requires separate approval, documented method, vendor compatibility review, safety assessment, rollback plan, and test window. Prefer a lab or staging environment.

### 8. Reporting and remediation planning
Describe evidence, affected assets, exploit prerequisites, process consequence, safety impact, existing safeguards, uncertainty, recommendations, and accountable owner.

### 9. Retest and closure
Verify remediation through approved methods and record residual risk.

## Assessment dimensions

- Asset visibility and ownership
- Architecture, segmentation, and conduits
- Identity and remote access
- Secure configuration and engineering change
- Vulnerability and patch lifecycle
- Endpoint and removable media controls
- Monitoring and detection
- Backup, restoration, and resilience
- Supplier and product lifecycle
- Incident response and recovery
- Governance, risk, and regulatory applicability

## Rules of engagement

Never perform uncontrolled scanning, fuzzing, exploitation, protocol writes, controller downloads, reboot, isolation, or configuration changes on production OT. Written authorization alone is not enough; the activity must also be technically safe, approved by responsible engineering and operations personnel, and consistent with site procedures.

## Deliverables

- Scope and rules of engagement
- Architecture and asset observations
- Evidence register
- Risk-ranked findings
- Standards and control mapping with limitations
- Remediation plan and owners
- Executive summary
- Retest evidence and residual risk

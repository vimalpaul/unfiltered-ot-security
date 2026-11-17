# OT Threat Intelligence Model

## Purpose

Organize intelligence about threats to industrial environments in a way that supports engineering decisions, detection, response, and risk management.

## Intelligence categories

- Threat actors and motivations
- Campaigns and intrusion sets
- Malware and tooling
- Initial access and remote access abuse
- IT-to-OT movement
- Engineering workstation compromise
- Manipulation of control logic, parameters, or process views
- Disruption, denial of view, denial of control, and destructive effects
- Supply chain and product compromise
- Exploitation of internet-exposed industrial services
- Insider and contractor risk
- Physical and cyber-physical convergence

## Required intelligence record

- Record identifier and title
- Publication and last-updated dates
- Publisher and source type
- Confidence and evidence quality
- Affected sector and geography, if supported
- Affected products and versions, if supported
- Observed techniques and ATT&CK for ICS references
- Initial access and prerequisites
- OT impact and process consequence
- Detection opportunities
- Mitigations and recovery considerations
- Attribution caveats
- Primary source links

## Analysis principles

Attribution is uncertain and should be stated with confidence and source basis. Do not equate malware capability with observed use. Distinguish confirmed incident facts from analyst inference. A technique mapping is a classification aid, not proof that a particular actor used the technique in every incident.

## Threat-informed defensive workflow

1. Define the process and assets to protect.
2. Identify relevant threat scenarios.
3. Map scenarios to ATT&CK for ICS techniques where appropriate.
4. Identify telemetry available at each zone and conduit.
5. Develop detections with false-positive and operational impact analysis.
6. Validate using safe simulations or replayed data.
7. Define response actions and decision authority.
8. Review after incidents, exercises, and material intelligence changes.

## Authoritative starting points

- MITRE ATT&CK for ICS: https://attack.mitre.org/matrices/ics/
- CISA Industrial Control Systems advisories: https://www.cisa.gov/news-events/cybersecurity-advisories
- CISA ICS recommended practices: https://www.cisa.gov/resources-tools/resources/ics-recommended-practices
- National CERT and regulator advisories relevant to each jurisdiction

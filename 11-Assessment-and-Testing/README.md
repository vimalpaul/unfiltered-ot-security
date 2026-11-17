# OT Security Assessment and Testing

This section provides the authorized assessment lifecycle, evidence standards, safe validation boundaries, technical review domains, reporting and assurance practices for OT/ICS environments.

## Core methodology

- [OT Security Assessment Methodology](OT-ASSESSMENT-METHODOLOGY.md)
- [OT Security Assessment, Audit and Testing Playbook](OT-SECURITY-ASSESSMENT-AUDIT-AND-TESTING-PLAYBOOK.md)

## Assessment principles

- Written authorization, precise scope and rules of engagement are mandatory.
- Authorization does not replace technical safety review or asset-owner approval.
- Understand process behavior, safety dependencies and operational constraints first.
- Prefer documentary review, passive observation and isolated replicas.
- Separate vulnerability assessment, configuration review and penetration testing.
- Never perform uncontrolled scanning, fuzzing, exploitation, protocol writes or controller changes on production OT.
- Validate product identity and version against authoritative vendor advisories.
- Map observations to exact control identifiers and preserve mapping limitations.
- Tie technical findings to process consequence and evidence.
- Require human review of AI-assisted analysis and reports.

## Planned specialist references

- Asset-family assessment worksheets for PLC, RTU, DCS, SCADA, HMI, SIS and IED.
- Passive protocol assessment guides.
- Vendor-specific safe assessment constraints.
- IEC 62443 audit evidence catalogue.
- Sector-specific assessment scenarios.
- Synthetic PCAP, log and tabletop exercise packs.
- Assessment maturity and quality assurance model.
- Jurisdiction-specific regulatory audit crosswalks.

# Standards and Frameworks

## Purpose

Catalogue the standards, frameworks, guidance, and technical models relevant to OT and industrial cybersecurity. This directory distinguishes source documents from project summaries and crosswalks.

## Core reference catalogue

| Reference | Primary focus | Use in this repository |
|---|---|---|
| IEC 62443 series | Security of industrial automation and control systems | Asset owner program, risk assessment, system requirements, component requirements, service providers |
| NIST SP 800-82 Rev. 3 | OT security guidance | OT architecture, threats, safeguards, operational constraints |
| NIST SP 800-82 Rev. 4 Initial Public Draft | Proposed update to OT guidance | Track as draft only until finalized |
| NIST Cybersecurity Framework 2.0 | Cybersecurity risk outcomes | Governance and enterprise-to-OT alignment |
| MITRE ATT&CK for ICS | Adversary tactics and techniques | Threat-informed detection and response |
| ISO/IEC 27001 | Information security management systems | Enterprise governance interfaces |
| ISO/IEC 27002 | Information security controls | Control design reference |
| ISO/IEC 27019 | Information security for energy utility process control | Energy-sector reference where applicable |
| ISO 22301 | Business continuity management | Continuity and recovery governance |
| IEC 61508 | Functional safety of E/E/PE safety-related systems | Safety lifecycle context |
| IEC 61511 | Functional safety for process industry SIS | SIS lifecycle and safety/security coordination |
| ISA-TR84.00.09 | Security considerations for SIS | Safety and security interface, subject to licensed source |
| CIS Controls | Prioritized cybersecurity safeguards | Supporting enterprise practices, tailored to OT |
| OWASP OT Top 10 | OT risk themes and mappings | Awareness and supplementary risk taxonomy |

## IEC 62443 family overview

The series contains multiple parts addressing general concepts, policies and procedures, system security requirements, component requirements, and lifecycle roles. The exact edition, amendment, publication status, and applicability must be verified against the IEC catalogue before a project cites a specific requirement.

Commonly referenced parts include:
- IEC 62443-1-1: terminology, concepts, and models
- IEC 62443-2-1: security program requirements for asset owners
- IEC 62443-2-4: security program requirements for IACS service providers
- IEC 62443-2-3: patch management in the IACS environment
- IEC 62443-3-2: security risk assessment for system design
- IEC 62443-3-3: system security requirements and security levels
- IEC 62443-4-1: secure product development lifecycle
- IEC 62443-4-2: technical security requirements for IACS components

This summary is not a substitute for the licensed standards. Do not reproduce protected requirement text.

## Mapping principles

- Preserve the original source identifier.
- Record edition and amendment.
- State whether the mapping is direct, partial, supporting, or not demonstrated.
- Explain rationale and scope.
- Do not infer equivalence from similar wording.
- Record evidence needed to demonstrate implementation.
- Keep safety and availability requirements visible.

## Official and authoritative starting points

- NIST SP 800-82 Rev. 3: https://csrc.nist.gov/pubs/sp/800/82/r3/final
- NIST SP 800-82 Rev. 4 initial public draft: https://csrc.nist.gov/pubs/sp/800/82/r4/ipd
- NIST CSF: https://www.nist.gov/cyberframework
- MITRE ATT&CK for ICS: https://attack.mitre.org/matrices/ics/
- IEC 62443 overview: https://www.iec.ch/
- ISO standards catalogue: https://www.iso.org/standards.html
- OWASP OT Top 10: https://ot.owasp.org/

## Currency note

At the time this entry was researched, NIST identifies SP 800-82 Rev. 3 as the final published revision and has published a Rev. 4 Initial Public Draft dated 21 September 2026 with comments due 30 November 2026. The draft must not be represented as a final standard or final NIST publication.

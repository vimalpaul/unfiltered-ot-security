---
title: "IEC 62443 Series: Practical Implementation Guide"
document_id: "UOTS-05-IEC62443-GUIDE"
status: "Research baseline — verify licensed edition and applicability before use"
version: "1.1"
owner: "Unfiltered OT Security"
created: "2026-11-17"
last_reviewed: "2026-11-27"
review_due: "2027-02-27"
scope: "ISA/IEC 62443 series orientation and implementation workflow"
classification: "Public"
---

# IEC 62443 Series: Practical Implementation Guide

## Purpose

Provide an orientation to the ISA/IEC 62443 family and how its parts relate to asset owners, integrators, service providers, and product suppliers. This is an explanatory guide, not a substitute for licensed standards.

## Stakeholder model

- **Asset owner:** Owns the industrial operation and risk, establishes the security program, defines requirements, and governs operation and maintenance.
- **Integrator and service provider:** Designs, integrates, configures, commissions, and maintains the automation solution within agreed responsibilities.
- **Product supplier:** Develops and supports industrial hardware and software and manages product security through its lifecycle.

Security is a shared responsibility. Contractual and operational boundaries must be explicit.

## Main parts and practical use

| Part | Main subject | Typical project use |
|---|---|---|
| IEC 62443-1-1 | Terminology, concepts, and models | Establish common vocabulary and foundational models |
| IEC 62443-2-1 | Asset owner IACS security program requirements; ANSI/ISA-62443-2-1-2024 is listed by ISA | Establish and maintain an OT security program |
| IEC 62443-2-2 | IACS security protection scheme technical report; ISA-TR62443-2-2-2025 is listed by ISA | Understand and organize the protection scheme across IACS operations |\n| IEC 62443-2-3 | Patch management in the IACS environment | Govern patch evaluation, testing, and deployment |
| IEC 62443-2-4 | Security program requirements for IACS service providers | Specify and assess integrator and maintenance provider practices |
| IEC 62443-3-2 | Security risk assessment for system design | Define system under consideration, zones, conduits, risk, and target security levels |
| IEC 62443-3-3 | System security requirements and security levels | Define system-level technical requirements |
| IEC 62443-4-1 | Secure product development lifecycle requirements | Assess supplier secure development lifecycle |
| IEC 62443-4-2 | Technical security requirements for IACS components | Evaluate component security capabilities |

The series is not published as one synchronized edition. The ISA catalogue currently lists ANSI/ISA-62443-2-1-2024 and ISA-TR62443-2-2-2025 alongside earlier publications for other parts. The IEC and ISA identifiers and publication states must be checked part by part. A technical report is not automatically a normative requirements standard. The exact current edition, corrigenda, amendments, national adoption and publication status must be verified against the IEC or ISA catalogue before citing a requirement.

## A practical implementation sequence

1. Establish governance, roles, policy, risk appetite, and management sponsorship.
2. Define the industrial scope and system boundaries.
3. Inventory assets, dependencies, process functions, and external connections.
4. Conduct a risk assessment for the system under consideration.
5. Partition the system into zones and conduits based on risk and security requirements.
6. Define target security levels with documented rationale.
7. Derive system and component requirements.
8. Specify integrator, supplier, and service provider responsibilities.
9. Implement technical and procedural safeguards.
10. Verify design, configuration, and operational evidence.
11. Operate vulnerability, patch, incident, backup, and change management processes.
12. Reassess after material changes and on a defined review cycle.

## Security levels

Security levels are risk-based concepts within the series. Do not assign a target level by guesswork or treat a product certificate as proof that an entire site or system achieves that level. Document the threat assumptions, system boundary, capability requirements, and verification evidence.

## Mapping and audit evidence

A project crosswalk should retain the source clause identifier and edition, describe the control objective in original wording, map to local policies and technical safeguards, identify evidence, explain gaps, and record accountable owners. Do not reproduce licensed normative text.

## Edition and status verification

ISA's published series page lists, among other entries, ANSI/ISA-62443-2-1-2024, ANSI/ISA-62443-3-2-2020, ISA-62443-3-3-2013, ANSI/ISA-62443-2-4-2018 / IEC 62443-2-4:2015+AMD1:2017, ANSI/ISA-62443-4-1-2018, and ANSI/ISA-62443-4-2-2018. ISA and IEC editions, publication status, and national adoption can differ. Check the official catalogue at the time of use.

## Supplier and product lifecycle boundary

IEC 62443-4-1 addresses secure product development lifecycle processes for product developers and maintainers. It is not a generic operator or integrator certification checklist. Asset owners and integrators should translate product security expectations into procurement, acceptance, vulnerability disclosure, patch support, end-of-life and contractual requirements, while assessing the supplier's evidence within the actual product and service scope.

IEC 62443-4-2 addresses technical security requirements for IACS components. Component capability evidence does not, by itself, demonstrate that the deployed system or site is securely architected, configured, integrated or operated.

## Copyright and AI handling

ISA's 62443 series page contains an explicit warning against entering ISA intellectual property into AI tools or creating derivatives from ISA intellectual property without permission. Do not upload licensed ISA/IEC standards text or use it to prompt an AI system unless the applicable licence and written permissions expressly permit that use. This guide uses bibliographic metadata and original explanatory summaries only.

## Review note — 2026-11-27

The edition references above were checked against the ISA series catalogue on this date. Recheck the publisher catalogue before procurement, contractual specification, assessment or audit. The catalogue is dynamic and this page is an orientation aid, not an edition register.

## Sources

- ISA, ISA/IEC 62443 Series of Standards: https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
- IEC catalogue: https://www.iec.ch/

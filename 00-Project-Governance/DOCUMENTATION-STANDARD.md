# Documentation and Evidence Standard

## 1. Purpose

Set a consistent quality bar for technical, regulatory, operational, and research documents.

## 2. Metadata block

Use this block at the top of substantial documents:

```yaml
title: "Document title"
document_id: "UOTS-DOMAIN-001"
status: "Draft"
version: "0.1"
owner: "Unfiltered OT Security"
created: "YYYY-MM-DD"
last_reviewed: "YYYY-MM-DD"
review_due: "YYYY-MM-DD"
scope: "Systems, process, sector, and jurisdiction"
classification: "Public"
sources:
  - "Canonical source URL"
```

Do not invent review dates or claim verification that has not occurred. Use the actual date when editing.

## 3. Required sections

1. Executive summary
2. Purpose and scope
3. Audience and prerequisites
4. Definitions and abbreviations
5. System and process context
6. Architecture, assets, interfaces, and trust boundaries
7. Threats, vulnerabilities, failure modes, and consequences
8. Security requirements and recommended controls
9. Implementation and operational considerations
10. Monitoring, response, and recovery
11. Verification and evidence
12. Standards and regulatory references
13. Assumptions, limitations, and open questions
14. Revision history

Not every section applies to every short reference page. Explain omissions where they matter.

## 4. Source hierarchy

1. Official law, regulator, standards body, national CERT, or government publication.
2. Official vendor product documentation and security advisories.
3. Recognized technical organizations and established research institutions.
4. Peer-reviewed publications and conference research.
5. Reputable industry analysis.
6. Community material, clearly labeled as practitioner experience and independently checked.

## 5. Source records

Capture publisher, exact title, version or edition, publication date, update date, canonical URL, access date, jurisdiction, source type, and claims supported. Prefer stable landing pages over transient download links.

## 6. Regulatory language

Use precise labels: law, regulation, regulator-issued control, mandatory standard, contractual requirement, voluntary standard, framework, guidance, or good practice. Record applicability conditions, regulated entity types, sector, territory, effective date, superseded status, and official source.

Never infer applicability from a country's name alone. Do not claim a control is legally mandatory unless the primary source supports that statement.

## 7. Mapping discipline

A crosswalk is an analytical aid, not proof of equivalence. Preserve original control identifiers and wording through short descriptions, cite the source, explain mapping rationale, and use relationship labels such as direct, partial, supporting, or no demonstrated relationship. Record confidence and reviewer notes.

## 8. Technical accuracy

Separate observed facts, source statements, analysis, and recommendations. Explain protocol or product version assumptions. Identify whether guidance is passive, active, disruptive, vendor-supported, or lab-only. Avoid universal claims where implementations vary.

## 9. Safety and availability

Consider process safety, human safety, environmental impact, product quality, uptime, deterministic timing, fail-safe behavior, and recovery. State preconditions and approval requirements for any active test. Prefer passive and offline methods when practical.

## 10. Diagrams and examples

Use Mermaid for maintainable diagrams. Label trust boundaries, zones, conduits, data direction, security enforcement points, and safety-relevant dependencies. Clearly label illustrative architectures as examples, not universal designs.

## 11. Review lifecycle

Review when a standard is revised, regulator publishes an update, vendor advisory changes, a vulnerability status changes, or a technical claim becomes outdated. Record what changed and why.

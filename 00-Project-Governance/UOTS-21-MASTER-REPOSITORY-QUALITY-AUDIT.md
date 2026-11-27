# UOTS-21: Master Repository Quality Audit Report

**Document ID:** UOTS-21  
**Status:** Baseline audit in progress  
**Audit scope:** Repository structure, content inventory, document architecture, representative technical playbooks, governance controls and initial quality risks  
**Repository:** https://github.com/vimalpaul/unfiltered-ot-security  
**Branch inspected:** `main`  
**Audit baseline:** 2026-11-27  
**Prepared for:** Unfiltered OT Security project maintainers

---

## 1. Executive summary

This report establishes an evidence-based baseline for the repository quality audit. The repository was inspected directly through its GitHub default branch and recursive Git tree. The tree response was not truncated.

The inspected repository contains:

- 86 Git tree entries: 62 files and 24 directories.
- 60 Markdown files, one YAML workflow file and one extensionless file.
- Twenty-one numbered content areas, from `00-Project-Governance` through `20-Glossary-and-Indexes`.
- A dedicated `.github/workflows/markdown-link-check.yml` workflow.
- Root-level README, CONTRIBUTING, SECURITY and LICENSE documents.
- A source register under `references/`.

The repository already has substantial technical content. The major technical playbooks are generally large, structured documents with extensive headings, tables and Mermaid diagrams. The audit therefore should not treat the repository as an empty outline or replace its existing content wholesale.

The first significant quality observation is **uneven depth between the main playbooks and their supporting documents**. This is most visible in the industry-use-case area, where the central industry playbook is substantial while several individual sector documents are short scoping references. Similar supporting-document depth differences exist in standards, regulation, asset inventory, assessment, identity/remote access, tools, labs and AI governance.

This is a baseline report, not a final certification or a completed technical validation. No overall score is assigned at this stage. Technical correctness, current legal applicability, standards edition status, external-link reachability and detailed cross-chapter traceability still require dedicated review.

## 2. Audit objectives and boundaries

### 2.1 Objectives

1. Establish the actual repository structure and file inventory.
2. Identify where substantive playbooks exist and where only supporting references exist.
3. Assess document architecture, consistency and evidence practices.
4. Identify high-value audit work that should precede content expansion.
5. Define a repeatable chapter-by-chapter verification and remediation process.
6. Preserve existing content unless evidence supports a specific correction or enhancement.

### 2.2 Boundaries

This baseline review inspected the live repository tree and retrieved the root README, governance documents, selected supporting documents and the principal playbook files for structural metrics and heading outlines.

The following are **not yet complete**:

- Line-by-line technical validation of every claim in all 60 Markdown files.
- Exhaustive validation of every external URL and regulatory instrument.
- Full relative-link resolution across every Markdown file.
- Independent confirmation of every standards edition, amendment and legal commencement date.
- Operational testing of lab instructions, commands, detections or engineering procedures.
- Verification against licensed copies of IEC, ISO or other paid standards.

A document's length, heading count or diagram count is not proof of technical accuracy.

## 3. Repository inventory

### 3.1 Repository-level structure

| Area | Verified contents |
|---|---|
| `.github` | Markdown link-check workflow |
| `00-Project-Governance` | Charter, documentation standard, research methodology, content roadmap |
| `01-OT-Fundamentals` | OT/ICS foundations |
| `02-Industrial-Architecture` | Reference architecture, zones and conduits |
| `03-Industrial-Assets-and-Systems` | Asset technical reference and asset inventory/criticality support |
| `04-Industrial-Protocols-and-Networks` | Protocol security engineering |
| `05-Standards-and-Frameworks` | Main standards/compliance playbook, IEC 62443 guide, README |
| `06-Global-Regulatory-Mapping` | Global regulatory playbook, GCC register, mapping model, country template, README |
| `07-Industry-and-Use-Cases` | Industry engineering playbook and six sector references plus README |
| `08-Threat-Intelligence` | Threat landscape playbook, intelligence model, README |
| `09-Vulnerabilities-and-Advisories` | CVE intelligence playbook, vulnerability management reference, README |
| `10-OT-Security-Engineering` | Hardening/defensive architecture playbook, identity/remote access and supply-chain references, README |
| `11-Assessment-and-Testing` | Assessment playbook, assessment methodology, README |
| `12-Monitoring-and-Detection` | SOC/detection playbook, SOC reference |
| `13-Incident-Response-and-Recovery` | Incident response and recovery playbook |
| `14-Risk-Governance-and-Assurance` | Risk assessment and assurance playbook |
| `15-Tools-and-Technology` | Tools/technology playbook and tool categories |
| `16-Labs-and-Simulations` | Labs/digital-twin playbook and safe lab engineering reference |
| `17-AI-and-Agent-Workflows` | Agentic OT playbook, governance/reference architecture and use-case catalogue |
| `18-Templates-and-Reference-Materials` | Deliverables playbook and assessment/evidence template |
| `19-Research-and-Learning` | Research playbook and learning path |
| `20-Glossary-and-Indexes` | Master glossary/knowledge architecture and concise glossary |
| `references` | Source register |
| Root | README, CONTRIBUTING, SECURITY and LICENSE |

### 3.2 File counts by numbered area

Counts below are based on actual Markdown files in each directory, including README files where present.

| Area | Markdown files |
|---|---:|
| 00 Project Governance | 4 |
| 01 OT Fundamentals | 1 |
| 02 Industrial Architecture | 1 |
| 03 Industrial Assets and Systems | 2 |
| 04 Industrial Protocols and Networks | 1 |
| 05 Standards and Frameworks | 3 |
| 06 Global Regulatory Mapping | 5 |
| 07 Industry and Use Cases | 9 |
| 08 Threat Intelligence | 3 |
| 09 Vulnerabilities and Advisories | 3 |
| 10 OT Security Engineering | 4 |
| 11 Assessment and Testing | 3 |
| 12 Monitoring and Detection | 2 |
| 13 Incident Response and Recovery | 1 |
| 14 Risk Governance and Assurance | 1 |
| 15 Tools and Technology | 2 |
| 16 Labs and Simulations | 2 |
| 17 AI and Agent Workflows | 3 |
| 18 Templates and Reference Materials | 2 |
| 19 Research and Learning | 2 |
| 20 Glossary and Indexes | 2 |

### 3.3 Principal playbook structural baseline

The following metrics were obtained from the principal playbook files. They are structural indicators only, not quality scores.

| Chapter | Approx. lines | Headings | Markdown table lines | Mermaid blocks |
|---|---:|---:|---:|---:|
| 01 OT Fundamentals | 946 | 84 | 104 | 9 |
| 02 Industrial Architecture | 1,067 | 102 | 137 | 12 |
| 03 Industrial Assets | 1,127 | 99 | 126 | 17 |
| 04 Protocols and Networks | 1,265 | 129 | 213 | 14 |
| 05 Standards and Frameworks | 974 | 82 | 247 | 5 |
| 06 Global Regulations | 1,097 | 103 | 164 | 5 |
| 07 Industry Use Cases | 1,224 | 97 | 172 | 14 |
| 08 Threat Intelligence | 1,003 | 79 | 232 | 7 |
| 09 Vulnerability Management | 996 | 70 | 193 | 6 |
| 10 Security Engineering | 1,035 | 78 | 72 | 5 |
| 11 Assessment and Testing | 1,136 | 86 | 145 | 3 |
| 12 Monitoring and Detection | 1,017 | 75 | 146 | 5 |
| 13 Incident Response | 1,283 | 111 | 134 | 5 |
| 14 Risk Governance | 1,173 | 86 | 180 | 4 |
| 15 Tools and Technology | 961 | 65 | 115 | 5 |
| 16 Labs and Simulations | 715 | 58 | 113 | 3 |
| 17 AI and Agent Workflows | 969 | 63 | 164 | 4 |
| 18 Templates and Deliverables | 860 | 56 | 341 | 0 |
| 19 Research and Learning | 757 | 51 | 140 | 3 |
| 20 Glossary and Indexes | 761 | 34 | 466 | 0 |

## 4. Initial findings

### 4.1 Strengths observed

| ID | Observation | Evidence | Assessment |
|---|---|---|---|
| S-01 | Clear numbered information architecture | Twenty-one numbered areas from governance to glossary/indexes | Strong foundation for navigation and growth |
| S-02 | Substantial core technical playbooks | Multiple principal guides exceed 700 lines and contain detailed section structures | Good content depth baseline; claims still need validation |
| S-03 | Visual architecture is embedded in key technical guides | Mermaid diagrams present across fundamentals, architecture, assets, protocols, industry, assessment and other chapters | Useful for explaining relationships and workflows |
| S-04 | Governance standards exist | Charter, documentation standard, research methodology and roadmap are present | Provides a basis for consistent review |
| S-05 | Regulatory model separates concepts | Global playbook, country module template and control mapping model exist | Good architecture for jurisdiction-specific research |
| S-06 | Practical engineering outputs are considered | Templates and deliverables chapter includes extensive tabular material | Strong direction toward operational usability |
| S-07 | Safety is explicitly represented | Safe lab engineering and OT operational caution sections are present in the structure | Must be checked in detailed technical review |
| S-08 | Automated link checking is configured | Workflow file exists under `.github/workflows` | Configuration and actual run results remain to be verified |

### 4.2 Initial gaps and risks

| ID | Priority | Finding | Why it matters | Required verification or action |
|---|---|---|---|---|
| F-01 | High | Supporting documents are materially shorter than their parent playbooks in several domains | A title may imply a standalone implementation guide while the file is only a short overview | Define a minimum content contract for standalone sector and engineering modules |
| F-02 | High | Sector-specific depth is uneven | Oil/gas, power, water, manufacturing, mining, transport, building automation and data-centre topics need comparable operational treatment | Audit each sector against a common process, asset, architecture, threat, control, incident and evidence schema |
| F-03 | High | Standards edition and applicability verification is not yet demonstrated by this inventory | Outdated editions or incorrect applicability can create misleading compliance guidance | Build a dated standards register with publisher source, edition, amendment, status and verification date |
| F-04 | High | Country-level regulatory coverage requires evidence-led validation | A global title does not establish complete country, sector or operator coverage | Validate each instrument against primary regulator or government sources and record legal status |
| F-05 | High | Cross-chapter traceability is not yet measured | Controls, risks, assets, detections, response actions and evidence can become disconnected | Build a traceability matrix linking process consequence to asset, threat, control, detection, response and assurance evidence |
| F-06 | Medium | Source register is small relative to the number of external references in the main playbooks | A source register should make evidence reusable and auditable | Normalize references into source IDs and link claims or tables to those IDs |
| F-07 | Medium | Structural consistency varies across documents | Readers and contributors need predictable sections and metadata | Apply the documentation standard consistently and define justified exceptions |
| F-08 | Medium | Templates are primarily represented as Markdown in the current inventory | Some users need usable registers and deliverables in spreadsheet or document form | Prioritize native editable templates for asset inventory, risk, zones/conduits, vulnerability, audit, incident and supplier assurance |
| F-09 | Medium | AI and agent governance needs explicit operational boundaries and assurance evidence | AI-assisted recommendations must not become uncontrolled changes to live industrial processes | Verify human approval, read-only defaults, identity, audit logs, data handling, failure modes and emergency stop boundaries |
| F-10 | Medium | Link-check workflow presence is verified, but execution results are not | A configured workflow is not evidence that the current branch passes | Inspect workflow runs and resolve failures after the link audit |
| F-11 | Medium | Mermaid block count is not equivalent to diagram validity | Syntax errors or unclear trust boundaries can undermine technical diagrams | Render-check all diagrams and review semantic correctness |
| F-12 | Low | Root-level source and contributor navigation can be improved | New contributors need a clear route from the README to evidence and governance | Check README discoverability and ensure every chapter README/index is maintained where appropriate |

### 4.3 Sector-document depth observation

The following supporting documents were inspected by heading outline and file size:

| Sector reference | Approx. size | Initial interpretation |
|---|---:|---|
| Oil, Gas, LNG and Petrochemical | 3.5 KB | Focused sector reference; depth audit required |
| Power, Grid and Substation | 2.9 KB | Focused sector reference; depth audit required |
| Water and Wastewater | 2.4 KB | Focused sector reference; depth audit required |
| Manufacturing and Factory | 2.3 KB | Focused sector reference; depth audit required |
| Mining and Metals | 1.8 KB | Focused sector reference; depth audit required |
| Transportation, Ports, Airports and Rail | 1.8 KB | Focused sector reference; depth audit required |
| Building Automation and Data Centre Facilities | 1.7 KB | Focused sector reference; depth audit required |

These documents should not automatically be labelled defective because of size. The audit must first decide whether each is intended as a short sector profile or a complete sector playbook. If it is intended to be standalone, it should be expanded using a common engineering structure and cross-linked to the central industry playbook.

## 5. Audit scorecard

The project previously agreed to use the following weighted scorecard. Scores are deliberately **not assigned yet** because the initial pass was primarily inventory and structural inspection.

| Dimension | Weight | Evidence required before scoring |
|---|---:|---|
| Technical accuracy | 15 | Claim-level technical review, protocol/architecture validation and safe operational guidance |
| Technical depth | 15 | Complete workflows, implementation steps, examples, validation and failure handling |
| Standards mapping | 15 | Edition-aware requirement-to-control-to-evidence mapping |
| Real-world use cases | 10 | Sector-specific process, asset, consequence and operational scenarios |
| Engineering workflows | 10 | Repeatable procedures, roles, inputs, outputs, decision gates and acceptance criteria |
| Diagrams and architecture | 10 | Rendered, accurate and traceable diagrams |
| Security controls | 10 | Preventive, detective, responsive and recovery control coverage |
| References and evidence | 5 | Primary sources, citations, status, date and evidence quality |
| Deliverables | 5 | Usable, consistent and testable practitioner artefacts |
| Cross-chapter integration | 5 | Bidirectional links and end-to-end traceability |
| **Total** | **100** | |

### 5.1 Rating bands

| Score | Rating |
|---:|---|
| 90–100 | Excellent |
| 80–89 | Strong |
| 70–79 | Needs improvement |
| 50–69 | Major enhancement required |
| Below 50 | Fundamental rework required |

A score must be accompanied by evidence, specific gaps and remediation actions. A score must never be inferred from document length alone.

## 6. Required audit method for each chapter

Every chapter will be reviewed against the following evidence checklist:

1. **Purpose and audience:** Is the scope clear and appropriate?
2. **Technical model:** Are systems, components, interfaces and dependencies accurate?
3. **Industrial context:** Are process safety, availability, reliability and operational constraints represented?
4. **Threat model:** Are threat scenarios realistic and tied to assets and consequences?
5. **Controls:** Are preventive, detective, response and recovery controls actionable?
6. **Implementation:** Are prerequisites, owners, steps, decision gates and acceptance criteria stated?
7. **Validation:** Can a practitioner verify that the control or procedure works safely?
8. **Standards mapping:** Are mappings accurate, edition-aware and clearly labelled as direct or informative?
9. **Regulatory mapping:** Are jurisdiction, sector, entity scope, legal status and effective dates evidenced?
10. **Evidence:** Are records, logs, diagrams, approvals and test artefacts specified?
11. **Diagrams:** Are trust boundaries, data flows, safety boundaries and control points explicit?
12. **References:** Are primary sources discoverable and current?
13. **Cross-links:** Are related chapters and artefacts connected?
14. **Safety:** Are instructions bounded to authorized, controlled environments and do they avoid unsafe live-process testing?
15. **Maintainability:** Are version, owner, review date and change triggers defined where appropriate?

## 7. Remediation roadmap

| Sequence | Workstream | Main output | Exit criteria |
|---:|---|---|---|
| 1 | Repository integrity | Verified path/link inventory, Markdown and Mermaid checks | No unexplained broken internal links or malformed fences |
| 2 | Governance and evidence | Updated documentation, source and review controls | Every major claim class has a defined evidence approach |
| 3 | Standards validation | Standards register and requirement/control/evidence matrix | Edition, status and mapping limitations recorded |
| 4 | Regulatory validation | Jurisdiction and sector register | Primary source, applicability, legal status and review date recorded |
| 5 | Technical chapter review | Chapter-level findings and scores | Each chapter has evidence-backed findings and remediation |
| 6 | Industry engineering depth | Consistent sector modules | Sector workflows cover process, assets, threats, controls and response |
| 7 | Cross-chapter traceability | Master relationship matrix | Risk-to-control-to-detection-to-response-to-evidence chain is navigable |
| 8 | Practitioner deliverables | Editable registers, checklists and report templates | Artefacts are internally consistent and usable |
| 9 | AI and agent assurance | Agent architecture and control assurance model | Read-only default, human approval and auditability are explicit |
| 10 | Final assurance | Final audit report and release checklist | Findings closed or accepted with named rationale and review date |

## 8. Priority definitions

- **Critical:** A defect that could cause unsafe operational action, materially incorrect legal/compliance advice, or a serious security misunderstanding. Stop publication of the affected instruction until corrected.
- **High:** A material gap in technical accuracy, applicability, traceability or engineering completeness that undermines practitioner use.
- **Medium:** A gap that reduces consistency, evidence quality, maintainability or operational usefulness.
- **Low:** A navigation, editorial or presentation improvement with limited impact on technical correctness.

## 9. Initial repository integrity observations

- The recursive Git tree response was complete and reported `truncated: false`.
- The repository contains a Markdown link-check workflow. Its latest execution result was not inspected in this baseline.
- The root README contains chapter navigation and global/industry coverage sections.
- The governance directory contains a documentation standard and research/verification methodology.
- Full internal-link resolution, external-link reachability and Mermaid rendering remain open audit tasks.

No statement in this section should be interpreted as a successful CI result.

## 10. Next audit actions

The next work should proceed in this order:

1. Inspect the full documentation standard and research methodology against actual chapter practices.
2. Validate the source register and normalize the authoritative source inventory.
3. Review the standards and regulatory playbooks claim by claim, beginning with the highest-impact OT requirements.
4. Complete the sector-by-sector engineering depth assessment.
5. Build the cross-chapter traceability model.
6. Inspect CI workflow execution and perform repository-wide Markdown, link and Mermaid validation.
7. Assign chapter scores only after the relevant evidence has been collected.

## 11. Standards and framework validation — first pass (2026-11-27)

### 11.1 Official-source checks completed

The following publisher/issuer pages were checked during this pass:

| Reference | Verified metadata or status | Audit implication |
|---|---|---|
| ISA/IEC 62443 | ISA's catalogue lists ANSI/ISA-62443-2-1-2024 and ISA-TR62443-2-2-2025 alongside parts with earlier publication dates | Edition control must be part-specific; do not state a single year for the whole series |
| IEC 62443-3-2 | IEC 62443-3-2:2020 is listed as Edition 1.0 and covers the system under consideration, zones/conduits, risk assessment and target security levels | Use the exact part identifier and publication year |
| IEC 62443-3-3 | IEC 62443-3-3:2013 and its 2014 corrigendum are listed | Do not infer that all parts have been refreshed with the 2024/2025 publications |
| IEC 62443-4-1 | IEC 62443-4-1:2018 is listed as Edition 1.0; the IEC page also shows Edition 2.0 under development | Monitor the project; do not cite a forecast as a published edition |
| IEC 61508-1 | IEC 61508-1:2010 Edition 2 is listed, while a 2026 Edition 3 pre-release is also exposed by IEC | Treat pre-release material as non-final; validate each part's status individually |
| IEC 61511-1 | IEC 61511-1:2016+A1:2017 consolidated Edition 2.1 is listed for process-industry SIS | Explicitly map functional-safety scope and lifecycle dependencies |
| ISO/IEC 27001 | ISO/IEC 27001:2022 has published Amendment 1:2024 | Include applicable amendments in the controlled edition record |
| ISO/IEC 27002 | ISO/IEC 27002:2022 is published as information security control guidance | Do not confuse guidance with independently certifiable ISMS requirements |
| ISO/IEC 42001 | ISO/IEC 42001:2023 is published as an AI management system standard | Include in AI governance context, not as an OT control catalogue |
| NIST SP 800-82 | Rev. 4 Initial Public Draft was published 2026-09-21; comments due 2026-11-30 | Rev. 3 remains the final publication until NIST publishes a final Rev. 4 |

### 11.2 Material findings added

| ID | Priority | Finding | Disposition |
|---|---|---|---|
| F-13 | High | Standards chapter did not provide a consolidated edition watch for all standards specifically requested in the project quality plan | Added dated publisher-verified edition watch to UOTS-05-STANDARDS |
| F-14 | High | IEC 61508 and IEC 61511 functional-safety relationships were not adequately represented in the standards chapter's main reference model | Added explicit functional-safety boundary, lifecycle coordination warning and part-specific edition notes |
| F-15 | Medium | ISO/IEC 42001 was not explicitly integrated into the standards edition register | Added AI management system standard context and source record |
| F-16 | High | The standards documentation did not surface the ISA publisher's explicit restrictions concerning use of ISA intellectual property in AI tools | Added a copyright and AI handling warning; only public bibliographic metadata and original summaries are used |
| F-17 | Medium | IEC 62443 quick guide omitted the recently listed ISA-TR62443-2-2-2025 and did not distinguish a technical report from a normative requirements standard | Updated the quick guide and clarified part-specific edition handling |

### 11.3 Changes committed

- Updated `05-Standards-and-Frameworks/OT-STANDARDS-FRAMEWORKS-AND-COMPLIANCE-ENGINEERING.md` to version 1.1 with the dated standards watch, functional-safety boundary, NIST draft status and copyright/AI caution.
- Updated `05-Standards-and-Frameworks/IEC-62443-SERIES-IMPLEMENTATION-GUIDE.md` with edition-aware references, the 2024 and 2025 ISA catalogue entries, supplier/product scope clarification and AI/IP caution.
- Expanded `references/SOURCE-REGISTER.md` with official ISA, IEC, ISO and NIST metadata sources.

### 11.4 Primary sources consulted

- ISA/IEC 62443 series catalogue: https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
- IEC 62443-3-2:2020: https://webstore.iec.ch/en/publication/30727
- IEC 62443-3-3:2013: https://webstore.iec.ch/en/publication/7033
- IEC 62443-4-1:2018: https://webstore.iec.ch/en/publication/33615
- IEC 61508-1:2010: https://webstore.iec.ch/en/publication/5515
- IEC 61508-1 Edition 3 pre-release: https://webstore.iec.ch/en/publication/117296
- IEC 61511-1:2016+A1:2017: https://webstore.iec.ch/en/publication/61289
- ISO/IEC 27001:2022/Amd 1:2024: https://www.iso.org/standard/88435.html
- ISO/IEC 27002:2022: https://www.iso.org/standard/75652.html
- ISO/IEC 42001:2023: https://www.iso.org/standard/42001
- NIST SP 800-82 Rev. 4 Initial Public Draft: https://csrc.nist.gov/pubs/sp/800/82/r4/ipd

**Status:** This is a metadata and scope validation pass. It does not constitute clause-by-clause conformity assessment or a final standards mapping. The NIST Rev. 4 comment deadline is imminent and should be rechecked after 2026-11-30.

## 12. GCC regulatory source validation — first pass (2026-11-27)

### 12.1 Official-source checks completed

| Jurisdiction | Official source evidence | Safe statement | Open validation |
|---|---|---|---|
| Saudi Arabia | NCA's OTCC page identifies OTCC-1:2022, published 2 June 2022, as OT minimum cybersecurity requirements and an extension to ECC | An OT-specific national control publication exists | Confirm entity/facility applicability, control level, current methodology and assessment tool |
| UAE federal | UAE Government CIIP Policy page, updated 2 July 2026 | National CII governance and protection policy exists | Review full policy, CII designation, implementing instruments and entity-specific obligations |
| Dubai | DESC standards page identifies a DESC ICS Standard and states its scope includes Dubai government and semi-government entities operating critical infrastructure and/or OT | A Dubai-specific ICS/OT standard and scope statement exist | Obtain controlled standard, clause identifiers, current edition and exact entity applicability |
| Qatar | Q-CERT hosts the National ICS Security Standard v3.1 | An official-hosted ICS baseline document is identifiable | Current effective version, formal adoption, covered entities and assessment process remain unconfirmed |
| Bahrain | NCSC Baseline Cyber Security Controls page and PDF; CNI controls page | Baseline includes OT/IoT Domain 6; published PDF states mandatory application to public/private entities that are part of CNI; NCSC lists sector-specific CNI control resources | Confirm current controlled version, CNI designation, entity scope, sector-specific requirements and assessment mechanism |
| Kuwait | CITRA-hosted national cybersecurity strategy | Strategy is a research lead and national policy context | Current binding instruments, competent authority and OT-specific mandatory requirements remain unverified |
| Oman | No definitive current universally applicable OT control catalogue established in this pass | No positive claim is made | Continue primary-source research; do not invent a control set |

### 12.2 Material regulatory findings

| ID | Priority | Finding | Disposition |
|---|---|---|---|
| F-18 | High | The GCC register omitted Qatar's official-hosted National ICS Security Standard v3.1 as a distinct entry | Added the source with explicit current-status and applicability caveats |
| F-19 | High | Bahrain's baseline OT/IoT domain and CNI applicability were not sufficiently detailed in the compact register | Added NCSC baseline and PDF sources, the CNI sector source, and high-level Domain 6 topics |
| F-20 | High | The UAE national CIIP Policy and Dubai DESC ICS Standard could be conflated | Clarified national CII policy versus Dubai-specific ICS/OT standard and prohibited UAE-wide generalization |
| F-21 | Medium | GCC source register needed a dated primary-source refresh and additional official URLs | Added UAE, Dubai, Qatar and Bahrain primary sources with a 2026-11-27 review note |

### 12.3 Changes committed

- Updated `06-Global-Regulatory-Mapping/MIDDLE-EAST-AND-GCC-REGULATORY-REGISTER.md` with Qatar National ICS Standard v3.1, Bahrain NCSC baseline/CNI controls, and UAE CIIP Policy.
- Updated `06-Global-Regulatory-Mapping/GLOBAL-OT-REGULATORY-AND-CRITICAL-INFRASTRUCTURE-PLAYBOOK.md` with more precise Bahrain Domain 6 context, official source links, and UAE federal/Dubai scope distinctions.
- Expanded `references/SOURCE-REGISTER.md` with official GCC authority and government sources.

### 12.4 Primary sources consulted

- Saudi NCA OTCC: https://nca.gov.sa/en/regulatory-documents/controls-list/otcc/
- UAE Government CIIP Policy: https://u.ae/en/about-the-uae/strategies-initiatives-and-awards/policies/cyber-activities/Critical-Information-Infrastructure-Protection-Policy
- Dubai DESC Standards and Policies: https://www.desc.gov.ae/regulations/standards-policies/
- Qatar National ICS Security Standard v3.1: https://qcert.ncsa.gov.qa/sites/default/files/public/documents/cs_national_ics_security_standard_en_v3.1_0.pdf
- Bahrain NCSC Baseline Cyber Security Controls: https://ncsc.gov.bh/en/standards-controls/baseline-cyber-security-controls
- Bahrain Baseline Controls PDF: https://www.ncsc.gov.bh/assets/static_images/policies/baseline-cybersecurity-controls-v1.pdf
- Bahrain NCSC CNI Cybersecurity Controls: https://www.ncsc.gov.bh/en/standards-controls/CNI-cybersecurity-controls
- Bahrain National Cyber Security Strategy 2025–2028: https://ncsc.gov.bh/en/national-strategy/bahrain-national-cyber-security-strategy-2025-2028.html

**Status:** First-pass source verification only. No complete legal applicability opinion or control-by-control compliance crosswalk has been performed.

## 13. Industry engineering depth validation — first pass (2026-11-27)

### 13.1 Files inspected

| File | Previous size | Initial assessment | Action |
|---|---:|---|---|
| `07-Industry-and-Use-Cases/INDUSTRY-SPECIFIC-OT-SECURITY-ENGINEERING-PLAYBOOK.md` | 63,544 characters | Substantial cross-sector playbook with process context, common architecture, scenarios, assessments, AI, labs and source discipline | Retained as the central cross-sector reference; use it as the shared framework and avoid duplicating it wholesale |
| `07-Industry-and-Use-Cases/OIL-GAS-AND-LNG-OT-SECURITY.md` | 3,464 characters | Short orientation; lacked detailed process/asset mapping, engineering workflows, detection, recovery and deliverables | Expanded to version 1.1 |
| `07-Industry-and-Use-Cases/POWER-GRID-AND-SUBSTATION-OT-SECURITY.md` | 2,870 characters | Short orientation; limited control centre/substation architecture, protection engineering, detection and restoration detail | Expanded to version 1.1 |
| `07-Industry-and-Use-Cases/WATER-AND-WASTEWATER-OT-SECURITY.md` | 2,365 characters | Short orientation; limited treatment taxonomy, public-health dependencies, incident workflow and utility evidence | Expanded to version 1.1 |

### 13.2 Findings

| ID | Priority | Finding | Disposition |
|---|---|---|---|
| F-22 | High | Oil/gas handbook did not connect process segments, safety-related functions, remote access, controller integrity, detections and recovery into one engineering workflow | Added process/asset matrix, architecture, threat/control/detection table, assessment workflow, incident and recovery model, deliverables and metrics |
| F-23 | High | Power handbook did not sufficiently distinguish control centre, station bus, process bus, protection, telecom and time dependencies | Added reference architecture, protocol-specific concerns, protection setting integrity, time monitoring, response constraints and recovery evidence |
| F-24 | High | Water handbook lacked a process-oriented taxonomy and detailed public-health/quality response model | Added water/wastewater process taxonomy, criticality, architecture, dosing/quality scenarios, local fallback and recovery workflows |
| F-25 | High | Sector guides did not adequately distinguish general engineering recommendations from jurisdiction-specific obligations | Added explicit applicability caveats and a US-only NERC CIP/EPA context |
| F-26 | Medium | Recent sector evidence was not reflected in the supporting handbooks or source register | Added FBI/EPA July 2026 water-sector PSA, NIST October 2026 water-sector article, multi-agency asset taxonomy, NERC CIP catalogue and DOE CESER exercise source |
| F-27 | High | A historical TSA Pipeline-2021-01E document could be misread as a current directive even though its stated expiry date was 2 May 2026 | Handbook now labels it historical and requires checking the latest TSA directive/renewal before use |

### 13.3 Changes committed

- Oil, gas, LNG and petrochemical handbook: commit `b881c94f325d13d032b4854c571d850662c5096e`.
- Power generation, grid and substation handbook: commit `1b830738a2c2796bc25c343c7c04183ed80e2a08`.
- Water and wastewater handbook: commit `08b2717fdb612b107c73654e8f3e1115e663f307`.
- Source register expanded with sector-specific official sources: commit `964f3be19f36203c4fcc542a35ac5a2958377454`.

### 13.4 Official sources consulted

- FBI/EPA, water-sector PLC targeting PSA, 30 July 2026: https://www.fbi.gov/investigate/cyber/alerts/2026/malicious-cyber-actors-targeting-water-and-wastewater-sector-internet--facing-programmable-logic-controllers-causing-operational-disruptions
- EPA water/wastewater cybersecurity guidance: https://nepis.epa.gov/Exe/ZyPURL.cgi?Dockey=P101B9KL.txt
- CISA-led OT Asset Inventory Guidance: https://www.epa.gov/system/files/documents/2025-09/joint-guide-foundations-for-ot-cybersecurity-asset-inventory-guidance_508c.pdf
- NIST water/wastewater OT security insight, 1 October 2026: https://www.nist.gov/blogs/cybersecurity-insights/securing-water-and-wastewater-operational-technology-environments
- NERC CIP standards catalogue: https://www.nerc.com/standards/reliability-standards/cip
- NERC CIP-003-10: https://www.nerc.com/standards/reliability-standards/cip/cip-003-10
- NERC CIP-007-6: https://prod.nerc.com/standards/reliability-standards/cip/cip-007-6
- NERC CIP-010-4: https://www.nerc.com/standards/reliability-standards/cip/cip-010-4
- NERC CIP-013-2: https://www.nerc.com/standards/reliability-standards/cip/cip-013-2
- NERC/FERC CIP-014-4 approval announcement, 10 September 2026: https://www.nerc.com/newsroom/ferc-approves-reliability-standard-for-physical-security
- DOE CESER oil and natural gas security exercises, 22 June 2026: https://www.energy.gov/ceser/articles/ceser-supports-oil-and-natural-gas-subsector-critical-energy-security-exercises
- TSA Pipeline-2021-01E (historical 2025 version; stated expiry 2 May 2026): https://www.tsa.gov/sites/default/files/tsa-security-directive-pipeline-2021-01e-and-memo-508c.pdf

**Status:** This is a handbook depth and selected-source validation pass. It does not constitute site-specific engineering approval, protection study, process safety assessment, water quality determination or legal applicability opinion.



## 14. Audit status and change control

This document is the initial baseline. It must be updated as each audit workstream is completed.

For every future update, record:

- Audit date and reviewer.
- Files and sections inspected.
- Evidence sources used.
- Finding IDs added, changed or closed.
- Score changes and their justification.
- Remediation commit references.
- Remaining limitations and next actions.

**Current disposition:** Baseline inventory established. Detailed content, standards, regulatory, link and operational validation are pending.

---

## Appendix A: Principal playbook paths

- `01-OT-Fundamentals/OT-ICS-FOUNDATIONS.md`
- `02-Industrial-Architecture/REFERENCE-ARCHITECTURE-AND-ZONES.md`
- `03-Industrial-Assets-and-Systems/INDUSTRIAL-ASSET-TECHNICAL-REFERENCE.md`
- `04-Industrial-Protocols-and-Networks/PROTOCOL-SECURITY-ENGINEERING.md`
- `05-Standards-and-Frameworks/OT-STANDARDS-FRAMEWORKS-AND-COMPLIANCE-ENGINEERING.md`
- `06-Global-Regulatory-Mapping/GLOBAL-OT-REGULATORY-AND-CRITICAL-INFRASTRUCTURE-PLAYBOOK.md`
- `07-Industry-and-Use-Cases/INDUSTRY-SPECIFIC-OT-SECURITY-ENGINEERING-PLAYBOOK.md`
- `08-Threat-Intelligence/OT-THREAT-LANDSCAPE-THREAT-INTELLIGENCE-AND-ADVERSARY-ENGINEERING.md`
- `09-Vulnerabilities-and-Advisories/OT-VULNERABILITY-MANAGEMENT-AND-CVE-INTELLIGENCE.md`
- `10-OT-Security-Engineering/OT-SECURITY-ENGINEERING-HARDENING-AND-DEFENSIVE-ARCHITECTURE.md`
- `11-Assessment-and-Testing/OT-SECURITY-ASSESSMENT-AUDIT-AND-TESTING-PLAYBOOK.md`
- `12-Monitoring-and-Detection/OT-SOC-INDUSTRIAL-MONITORING-AND-DETECTION-ENGINEERING-PLAYBOOK.md`
- `13-Incident-Response-and-Recovery/OT-INCIDENT-RESPONSE.md`
- `14-Risk-Governance-and-Assurance/OT-RISK-ASSESSMENT-METHOD.md`
- `15-Tools-and-Technology/OT-SECURITY-TOOLS-TECHNOLOGY-ENGINEERING-PLAYBOOK.md`
- `16-Labs-and-Simulations/OT-CYBERSECURITY-LABS-DIGITAL-TWINS-AND-INDUSTRIAL-SIMULATION-PLAYBOOK.md`
- `17-AI-and-Agent-Workflows/AI-AND-AGENTIC-OT-SECURITY-ENGINEERING-PLAYBOOK.md`
- `18-Templates-and-Reference-Materials/OT-SECURITY-TEMPLATES-AND-PROFESSIONAL-DELIVERABLES-PLAYBOOK.md`
- `19-Research-and-Learning/OT-SECURITY-RESEARCH-THREAT-INTELLIGENCE-AND-LEARNING-PLAYBOOK.md`
- `20-Glossary-and-Indexes/OT-SECURITY-GLOSSARY-MASTER-INDEX-AND-KNOWLEDGE-ARCHITECTURE.md`

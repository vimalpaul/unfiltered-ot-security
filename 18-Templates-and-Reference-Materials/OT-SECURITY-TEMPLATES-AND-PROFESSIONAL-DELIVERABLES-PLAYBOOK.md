---
title: "OT Security Templates, Registers, Checklists and Professional Deliverables"
document_id: "UOTS-18-TEMPLATES"
version: "1.0"
status: "Reusable professional reference pack"
owner: "Unfiltered OT Security"
created: "2026-11-17"
last_reviewed: "2026-11-17"
review_due: "2027-02-17"
scope: "Reusable OT cybersecurity assessment, engineering, governance, operations and assurance templates"
classification: "Public"
---

# OT Security Templates, Registers, Checklists and Professional Deliverables

**Document ID:** UOTS-18-TEMPLATES | **Version:** 1.0 | **Status:** Reusable professional reference pack

**Audience:** OT security consultants, CISOs, OT engineers, plant operations, SOC teams, system integrators, auditors, risk owners, project managers and industrial asset owners.

> **Use and safety notice:** These are generic starting templates. Tailor them to the facility, process, jurisdiction, contract, asset owner requirements and approved standards editions. A completed template is not automatically evidence of compliance, safety approval or engineering authorization. Do not perform active testing, production changes or disruptive validation without written authorization and the site's change, safety and operational approvals.

# 1. Purpose

This chapter provides reusable structures for professional OT security work. It is designed to help teams collect consistent evidence, make decisions traceable, assign ownership and communicate findings to technical and executive audiences.

Templates are deliberately tool-neutral. They can be implemented in spreadsheets, document management systems, GRC platforms, ticketing systems or controlled project repositories. Field names should remain stable when records are exchanged between systems.

## 1.1 Template design principles

- Every record has a unique identifier.
- Every observation has a source and collection date.
- Separate fact, interpretation, risk and recommendation.
- Identify asset, site, process and accountable owner.
- Record confidence and limitations.
- Preserve evidence references and integrity metadata.
- Distinguish mandatory requirements from guidance.
- Record standard edition and clause only after verification.
- Assign an action owner, due date and closure evidence.
- Track status, approval and revision history.
- Minimize sensitive operational details in broadly shared reports.
- Use controlled access, retention and disposal.

# 2. Common data dictionary

Use consistent values across all registers.

| Field | Definition / expected format |
|---|---|
| Record_ID | Stable unique identifier, e.g. UOTS-ASSET-0001 |
| Site_ID | Approved site or facility identifier |
| Area_ID | Process area, unit, line or substation |
| Asset_ID | Unique asset register identifier |
| Source_ID | Evidence source or system reference |
| Owner | Accountable business or technical role |
| Created_Date | ISO 8601 date |
| Updated_Date | ISO 8601 date |
| Status | Proposed, Open, In Progress, Pending Review, Accepted, Closed, Rejected, Deferred |
| Priority | Critical, High, Medium, Low; define local criteria |
| Confidence | High, Medium, Low, Unknown, with rationale |
| Evidence_Ref | Controlled evidence repository reference |
| Reviewer | Person or role performing independent review |
| Approval_Ref | Change, risk, safety or management approval reference |
| Due_Date | Agreed completion date |
| Closure_Evidence | Evidence demonstrating completion and validation |

Do not use a blank cell to mean both "not applicable" and "not yet assessed". Use explicit values such as N/A, Unknown, Not Assessed or Pending.

# 3. Engagement initiation and scope template

## 3.1 Engagement charter

| Field | Entry |
|---|---|
| Engagement_ID | |
| Client / Asset Owner | |
| Engagement Name | |
| Business Objective | |
| Sites and Facilities | |
| Sector / Process | |
| In-Scope Systems | |
| Explicitly Out-of-Scope Systems | |
| Assessment Type | Architecture review, risk assessment, passive review, authorized test, audit support, incident readiness |
| Assessment Period | |
| Applicable Contract / SOW | |
| Rules of Engagement Reference | |
| Operational Contact | |
| OT Engineering Contact | |
| Security Contact | |
| Safety Contact | |
| Executive Sponsor | |
| Data Classification | |
| Deliverables | |
| Approval References | |
| Assumptions and Constraints | |

## 3.2 Scope and authorization checklist

- [ ] Asset owner and legal authority identified.
- [ ] Written authorization received.
- [ ] Sites, IP ranges and systems explicitly scoped.
- [ ] Production and safety-related exclusions documented.
- [ ] Permitted and prohibited test methods documented.
- [ ] Testing windows and blackout periods agreed.
- [ ] Plant operations and control room contacts identified.
- [ ] Safety review and permit requirements completed where applicable.
- [ ] Emergency stop and escalation contacts agreed.
- [ ] Data handling, retention and transfer approved.
- [ ] Third-party and OEM permissions confirmed.
- [ ] Evidence collection and reporting rules agreed.
- [ ] Change management and rollback requirements documented.
- [ ] Final report recipients and distribution approved.

The canonical OT asset identity, linked interface and dependency model, evidence confidence and criticality approval workflow are defined in the [OT Asset Inventory, Dependency Mapping and Criticality Engineering Playbook](../03-Industrial-Assets-and-Systems/OT-ASSET-INVENTORY-AND-CRITICALITY.md). Keep these templates aligned with that data model; do not create duplicate Asset_ID values for individual network interfaces.

# 4. OT asset inventory register

One row per uniquely managed asset. Where a device has multiple interfaces, model interfaces in a linked interface table rather than duplicating the asset identity.

| Column | Description |
|---|---|
| Asset_ID | Unique asset ID |
| Site_ID / Area_ID | Location and process area |
| Hostname / Asset_Name | Approved name |
| Asset_Type | PLC, RTU, HMI, SCADA server, DCS node, IED, EWS, historian, firewall, switch, sensor, gateway, SIS component, other |
| Manufacturer | OEM |
| Model | Exact model |
| Hardware_Revision | Hardware version |
| Firmware_Version | Verified firmware |
| OS_and_Version | Operating system if applicable |
| Serial_or_Tag | Controlled equipment tag; protect sensitive identifiers |
| Function | Operational purpose |
| Process_Criticality | Site-defined classification and rationale |
| Safety_Relationship | None known, safety-related, SIS, protection, unknown; validate with engineering |
| Zone_ID | Security zone |
| Network_Interface_Ref | Linked interface record |
| Protocols | Verified protocols |
| Owner | Asset owner |
| Support_Owner | Internal or supplier support |
| Lifecycle_Status | Supported, End of Support, Obsolete, Unknown |
| Backup_Status | Verified, Not Verified, Not Applicable |
| Last_Verified | Date and source |
| Discovery_Source | CMDB, engineering list, passive monitoring, vendor record |
| Confidence | High, Medium, Low, Unknown |
| Notes | Limitations and reconciliation notes |

### 4.1 Interface and communication register

| Flow_ID | Source_Asset_ID | Destination_Asset_ID | Source_Interface | Destination_Interface | Protocol / Service | Direction | Purpose | Business Owner | Approved_Ref | Observed_Ref | Last_Validated |
|---|---|---|---|---|---|---|---|---|---|---|---|

Record only the detail needed for controlled engineering and security use. Store sensitive topology in an access-controlled repository.

# 5. Asset criticality assessment worksheet

Assess consequence in the context of the actual process. Do not infer safety consequence from an IT classification alone.

| Dimension | Rating | Evidence / rationale |
|---|---|---|
| Personnel safety | | |
| Environmental impact | | |
| Production / service availability | | |
| Product quality | | |
| Equipment damage | | |
| Regulatory / legal impact | | |
| Financial impact | | |
| Public / customer impact | | |
| Recovery complexity | | |
| Dependency concentration | | |

Record:
- Assessment methodology and approved scale.
- Process owner and engineering reviewer.
- Worst credible consequence considered.
- Existing safeguards and assumptions.
- Dependencies and common-cause risks.
- Date and trigger for reassessment.

# 6. OT risk register

| Column | Description |
|---|---|
| Risk_ID | Unique risk identifier |
| Site_ID / Process_Area | Location and process |
| Asset_or_Service | Affected asset or service |
| Risk_Statement | Cause, event and consequence |
| Threat_or_Hazard_Context | Relevant scenario |
| Vulnerability_or_Condition | Verified weakness or exposure |
| Existing_Controls | Current safeguards |
| Likelihood | Rating under approved methodology |
| Consequence | Rating under approved methodology |
| Inherent_Risk | Before additional treatment |
| Treatment | Avoid, mitigate, transfer/share, accept |
| Action | Specific risk treatment |
| Residual_Risk | After treatment |
| Risk_Owner | Accountable owner |
| Action_Owner | Delivery owner |
| Due_Date | Target |
| Acceptance_Reference | Formal acceptance if applicable |
| Review_Date | Next review |
| Status | Lifecycle state |

### 6.1 Risk statement format

"Because of [cause or condition], [threat/event] could affect [asset/process], resulting in [operational, safety, environmental, financial or regulatory consequence]."

Avoid risk statements that simply repeat a scanner finding. Link technical condition to a credible process consequence and document uncertainty.

# 7. Zones and conduits design worksheet

| Zone_ID | Zone_Name | Purpose | Included_Assets | Trust_Level_Rationale | Security_Requirements | Owner | Boundary_Control | Approval |
|---|---|---|---|---|---|---|---|---|

| Conduit_ID | Source_Zone | Destination_Zone | Initiator | Protocol | Port / Service | Purpose | Direction | Authentication | Inspection | Owner | Approval |
|---|---|---|---|---|---|---|---|---|---|---|---|

Review questions:
- Is the system under consideration clearly bounded?
- Are assets grouped by function, risk and security requirements?
- Are conduits explicit and justified?
- Are remote access paths documented?
- Are temporary and emergency flows controlled?
- Are safety and availability constraints understood?
- Are shared services and dependencies identified?
- Are boundary controls owned, monitored and tested?
- Is the design consistent with the applicable IEC 62443 edition and project scope?

A Purdue model diagram is a useful reference view, not a substitute for a site-specific zones-and-conduits risk assessment.

# 8. Network communication and firewall review register

| Rule_ID | Device | Source | Destination | Service / Protocol | Direction | Business Purpose | Requestor | Owner | Logging | Expiry / Review | Change_Ref | Test_Evidence | Decision |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

Review criteria:
- Business and process purpose is documented.
- Source and destination are specific.
- Service is limited to what is required.
- Direction and initiation are understood.
- Rule owner is named.
- Temporary access has an expiry.
- Logging and monitoring are defined.
- Vendor and remote access are considered.
- Rule is tested through approved change process.
- Unused rules are identified for owner review.
- No rule is removed solely from an automated recommendation without engineering impact review.

# 9. OT vulnerability and exposure register

| Column | Description |
|---|---|
| Finding_ID | Unique finding |
| Asset_ID | Verified affected asset |
| Site / Zone | Context |
| Product / Model | Exact identification |
| Version | Verified version |
| Advisory_ID | CVE or vendor advisory |
| Source_URL | Authoritative source |
| Affected_Version_Check | Exact applicability evidence |
| Exposure | Reachability and attack path context |
| Exploitation_Evidence | Verified source and date |
| Technical_Severity | Source score and scoring version |
| Process_Impact | Site-specific consequence |
| Compensating_Controls | Existing controls |
| Vendor_Guidance | OEM-approved mitigation |
| Recommended_Treatment | Patch, mitigate, isolate, monitor, accept, investigate |
| Change_Approval | Reference |
| Owner | Accountable owner |
| Due_Date | Agreed target |
| Retest_Evidence | Validation record |
| Status | Lifecycle state |

Do not equate a CVSS score with OT risk. Record exact product/version evidence, exploit preconditions, exposure, process criticality, compensating controls and vendor guidance. Avoid active scanning or exploitation of production OT unless separately authorized and engineered.

# 10. Vendor advisory applicability worksheet

| Field | Entry |
|---|---|
| Advisory_ID | |
| Publisher | |
| Official_URL | |
| Publication_Date | |
| Last_Updated | |
| Product_Family | |
| Affected_Products | |
| Affected_Versions | |
| Fixed_Versions | |
| Preconditions | |
| Known_Exploitation_Status | |
| Site_Asset_Match | |
| Match_Evidence | |
| Exposure_Context | |
| OEM_Mitigation | |
| Operational_Constraints | |
| Applicability_Decision | Applicable, Not Applicable, Unconfirmed |
| Decision_Rationale | |
| Reviewer | |
| Review_Date | |

# 11. OT security assessment checklist

## 11.1 Governance and ownership
- [ ] OT security ownership defined.
- [ ] Asset owner and process owner identified.
- [ ] OT security policies approved and reviewed.
- [ ] Risk assessment process includes operational consequence.
- [ ] Exceptions and risk acceptance are authorized.
- [ ] Suppliers and integrators have defined security obligations.
- [ ] Incident and recovery roles are documented.

## 11.2 Asset and architecture
- [ ] Asset inventory has source and confidence.
- [ ] Critical assets and dependencies are identified.
- [ ] Network diagrams reflect verified current state.
- [ ] Zones and conduits are documented.
- [ ] Remote access paths are known.
- [ ] Wireless, IIoT and cloud connections are included.
- [ ] Legacy and unsupported assets are identified.

## 11.3 Identity and remote access
- [ ] Named accounts are used where supported.
- [ ] Shared and default accounts are assessed.
- [ ] MFA is applied to appropriate remote access paths.
- [ ] Privileged access is controlled.
- [ ] Supplier access is approved, time-bound and logged.
- [ ] Credentials are protected and rotated under policy.
- [ ] Joiner, mover and leaver procedures cover OT.

## 11.4 Network security
- [ ] Boundary controls are documented.
- [ ] Rules have owners and business purposes.
- [ ] Monitoring coverage and blind spots are known.
- [ ] Unapproved connections are investigated.
- [ ] Remote access is routed through approved controls.
- [ ] Time synchronization and logging dependencies are understood.

## 11.5 Endpoint and engineering security
- [ ] Supported endpoint protection strategy exists.
- [ ] Application control suitability is assessed.
- [ ] Engineering workstations are controlled.
- [ ] Removable media process is defined.
- [ ] Secure configuration baselines exist.
- [ ] Patch and vulnerability decisions consider process constraints.
- [ ] Backup and restoration are validated.

## 11.6 Detection and response
- [ ] OT-specific alert triage procedures exist.
- [ ] SOC has asset and process context.
- [ ] Escalation to operations is defined.
- [ ] Incident playbooks are exercised.
- [ ] Evidence preservation is defined.
- [ ] Recovery and return-to-service authority is clear.

For each checklist item record: result, evidence reference, applicability, rationale, owner, risk, action, due date and reviewer. A tick without evidence is not assurance.

# 12. Passive monitoring deployment checklist

- [ ] Monitoring objective and scope approved.
- [ ] Network owner and process owner identified.
- [ ] Sensor placement reviewed against topology.
- [ ] SPAN/TAP design reviewed by network engineering.
- [ ] No inline blocking introduced unintentionally.
- [ ] Sensor management interfaces isolated.
- [ ] Time synchronization configured and monitored.
- [ ] Asset identification method documented.
- [ ] Protocol parser coverage and limitations documented.
- [ ] Encrypted traffic visibility limitations documented.
- [ ] Packet loss and sensor health monitored.
- [ ] Storage, retention and privacy requirements approved.
- [ ] Alert ownership and escalation defined.
- [ ] Baseline period and maintenance windows recorded.
- [ ] Fail-safe behavior and maintenance procedure documented.
- [ ] Deployment validated under approved change control.

# 13. OT SOC use-case specification

| Field | Entry |
|---|---|
| Use_Case_ID | |
| Name | |
| Threat / Risk Hypothesis | |
| ATT&CK_for_ICS_Reference | Verified technique reference, if applicable |
| Required_Data_Sources | |
| Required_Fields | |
| Detection_Logic_Reference | |
| Asset_Context | |
| Baseline / Threshold | |
| Expected_Alert | |
| False_Positive_Scenarios | |
| Known_Blind_Spots | |
| Severity_Rationale | |
| Analyst_Triage | |
| OT_Escalation | |
| Test_Data | |
| Validation_Result | |
| Owner | |
| Version / Review_Date | |

A detection use case should state what evidence would support and disconfirm the hypothesis. ATT&CK mapping is contextual and must not be forced where evidence is absent.

# 14. Incident response record and timeline

## 14.1 Incident header

| Field | Entry |
|---|---|
| Incident_ID | |
| Date / Time Detected | |
| Site / Process Area | |
| Reporter | |
| Incident Commander | |
| OT Operations Lead | |
| Security Lead | |
| Safety Contact | |
| Severity | |
| Current Process State | |
| Affected Assets | |
| Initial Hypothesis | |
| Confirmed Facts | |
| Unknowns | |
| External Notifications | |
| Status | |

## 14.2 Event timeline

| Timestamp with timezone | Event_ID | Source | Observed Fact | Analyst Interpretation | Confidence | Evidence_Ref | Decision / Action | Owner |
|---|---|---|---|---|---|---|---|---|

## 14.3 Decision log

| Decision_ID | Time | Decision Required | Options Considered | Process / Safety Input | Decision Owner | Approval | Rationale | Review Trigger |
|---|---|---|---|---|---|---|---|---|

Keep observations separate from hypotheses. Do not change original timestamps or overwrite raw evidence.

# 15. Evidence register and chain of custody

| Evidence_ID | Incident / Assessment_ID | Description | Source_System | Collector | Collection_Time | Timezone | Method | Original_Location | Hash_Algorithm | Hash_Value | Transfer_Log | Access_Restrictions | Retention |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

Evidence handling procedure:
1. Confirm collection authority and scope.
2. Record source system and collection context.
3. Use approved read-only methods where feasible.
4. Preserve original evidence.
5. Calculate an approved cryptographic hash where integrity assurance is required.
6. Store a working copy separately.
7. Restrict access and log transfers.
8. Record tool and version used.
9. Preserve time zone and clock uncertainty.
10. Follow legal hold and retention requirements.

# 16. Backup and recovery validation record

| Field | Entry |
|---|---|
| Test_ID | |
| System / Asset_ID | |
| System Owner | |
| Backup Type | |
| Backup Source and Date | |
| Backup Integrity Evidence | |
| Restore Environment | |
| Isolation Confirmation | |
| Approved Recovery Procedure | |
| Recovery Point Objective | |
| Recovery Time Objective | |
| Actual Restore Time | |
| Configuration / Version Check | |
| Functional Validation | |
| Engineering Approval | |
| Exceptions | |
| Evidence References | |
| Result | Pass, Fail, Partial, Not Tested |
| Reviewer | |

A successful backup job is not proof of recoverability. Record an actual controlled restoration test and validation by the responsible system owner.

# 17. Management of Change (MOC) security review

| Field | Entry |
|---|---|
| MOC_ID | |
| Change Title | |
| Requestor | |
| Site / Process | |
| Affected Assets | |
| Change Description | |
| Business / Safety Reason | |
| Security Impact | |
| Network / Data Flow Changes | |
| Identity / Remote Access Impact | |
| Vendor / Firmware / Software Impact | |
| Vulnerability and Hardening Impact | |
| Monitoring Impact | |
| Backup / Rollback Plan | |
| Test Evidence | |
| Maintenance Window | |
| Operations Approval | |
| Engineering Approval | |
| Cybersecurity Approval | |
| Safety Approval, if applicable | |
| Final Authorization | |
| Post-Change Validation | |
| Closure Evidence | |

No security reviewer should independently approve a process change outside their delegated authority. Follow the site's MOC and safety governance.

# 18. Third-party and supplier OT security questionnaire

For each question record response, evidence, applicability, reviewer and risk.

## Governance and assurance
1. Do you maintain a documented security program for services delivered to the asset owner?
2. Are security responsibilities contractually defined?
3. Do you provide current independent assurance reports where relevant?
4. Are subcontractors and support providers disclosed?
5. Is vulnerability disclosure and incident notification defined?

## Product and engineering
6. Is a secure development lifecycle documented?
7. Are software components and dependencies managed?
8. Are product security advisories published?
9. Are supported versions and end-of-life dates available?
10. Are secure configuration guides provided?
11. Are default credentials and unnecessary services addressed?
12. Are product updates authenticated and integrity protected?

## Access and operations
13. Is supplier access named, approved and time-bound?
14. Is MFA supported for remote access?
15. Are privileged sessions logged?
16. Can access be disabled promptly by the asset owner?
17. Are support sessions coordinated with plant operations?
18. Are emergency access procedures documented?

## Data and cloud
19. Where is customer data processed and stored?
20. Are data retention and deletion defined?
21. Are tenant boundaries and encryption controls documented?
22. Are cross-border transfers disclosed?
23. Are AI model and data usage terms disclosed where AI is used?

## Incident and continuity
24. Are incident notification timelines contractually defined?
25. Are recovery and business continuity plans tested?
26. Can the supplier provide forensic evidence and support?
27. Are service dependencies and outage procedures documented?

# 19. AI and agent system assessment template

| Field | Entry |
|---|---|
| AI_System_ID | |
| Intended_Purpose | |
| Prohibited_Uses | |
| System_Owner | |
| OT_Data_Owner | |
| Model / Provider / Version | |
| Hosting_Location | |
| Data_Classification | |
| Data_Sources | |
| RAG_Corpus_and_Version | |
| Tools_and_Permissions | |
| Trust_Boundaries | |
| Human_Review | |
| Prompt_Injection_Test | |
| Data_Leakage_Test | |
| Tool_Authorization_Test | |
| Grounding_and_Citation_Test | |
| Availability_and_Fallback | |
| Safety_Review | |
| Legal_and_Privacy_Review | |
| Residual_Risk | |
| Approval_Reference | |
| Review_Date | |

Agent-specific controls:
- [ ] Tool allowlist and strict schemas.
- [ ] No unrestricted shell, browser or network access.
- [ ] No production control authority by default.
- [ ] Per-user and per-site authorization.
- [ ] Short-lived secrets and credential isolation.
- [ ] Tool-call logging and correlation IDs.
- [ ] Human approval for consequential decisions.
- [ ] Rate limits, timeouts and kill switch.
- [ ] Prompt injection and untrusted document testing.
- [ ] Manual fallback and recovery process.

# 20. Regulatory and standards applicability register

| Field | Description |
|---|---|
| Requirement_ID | Unique identifier |
| Country / Jurisdiction | Exact jurisdiction |
| Regulator / Authority | Official body |
| Legal_Instrument | Exact law, regulation, directive or binding instrument |
| Version / Edition | Published version |
| Clause / Article | Verified exact reference |
| Publication_Date | Official publication |
| Effective_Date | Legal effective date |
| Entity_Scope | Entities covered |
| Sector_Scope | Sector covered |
| System_Scope | Systems or data covered |
| Applicability_Decision | Applicable, Not Applicable, Under Review |
| Rationale | Legal and factual analysis |
| Related_Control | Internal control reference |
| Evidence_Required | Objective evidence |
| Control_Owner | Accountable owner |
| Legal_Reviewer | Qualified reviewer |
| Official_Source_URL | Primary source |
| Last_Verified | Date |
| Next_Review | Date |

Do not use a country strategy, regulator guideline, voluntary framework or draft as if it were a binding legal obligation. Legal applicability requires qualified jurisdiction-specific review.

# 21. Audit evidence and control assurance register

| Evidence_ID | Framework | Edition | Requirement_Ref | Control_ID | Control_Description | Owner | Evidence_Description | Evidence_Location | Period_Covered | Population | Sample_Method | Test_Procedure | Result | Exception_ID | Reviewer | Date |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

Evidence quality tests:
- Is it relevant to the exact requirement?
- Is it current for the audit period?
- Is the source authoritative?
- Is the population complete?
- Is the sample method documented?
- Is the evidence attributable to the control owner?
- Can another reviewer reproduce the conclusion?
- Are exceptions and limitations visible?

# 22. Project and remediation action tracker

| Action_ID | Source_Record_ID | Finding / Risk | Action Description | Priority | Owner | Dependency | Planned_Start | Due_Date | Status | Blocker | Evidence_Required | Reviewer | Closure_Date |
|---|---|---|---|---|---|---|---|---|---|---|---|---|

Closure requires:
- Defined acceptance criteria.
- Evidence of implementation.
- Validation by an appropriate reviewer.
- Residual risk recorded.
- Related diagrams, registers and procedures updated.
- Formal risk acceptance if the issue remains open.

# 23. CISO and executive reporting template

## 23.1 Executive summary structure

1. Reporting period and scope.
2. Overall OT security posture with methodology caveat.
3. Material changes since prior report.
4. Top operational and cyber risks.
5. Critical asset visibility and unknowns.
6. Exposure and vulnerability treatment status.
7. Monitoring and detection coverage.
8. Incident and recovery readiness.
9. Supplier and remote access risks.
10. Standards and regulatory obligations requiring attention.
11. Investment and resource decisions.
12. Decisions required from leadership.

## 23.2 Suggested metrics

| Metric | Definition | Interpretation caution |
|---|---|---|
| Inventory coverage | Verified in-scope assets / estimated in-scope assets | Denominator quality matters |
| Critical asset ownership | Critical assets with named accountable owner / critical assets | Ownership does not prove security |
| Zone/conduit documentation | In-scope zones and conduits reviewed / identified total | Review quality matters |
| Advisory applicability review | Relevant advisories assessed / relevant advisories received | Do not count irrelevant advisories |
| Overdue high-risk actions | High-risk actions past agreed due date | Explain accepted exceptions |
| Monitoring coverage | Assets or conduits with validated visibility / target scope | Visibility is not detection effectiveness |
| Detection validation | Use cases tested within period / planned use cases | Test quality and coverage matter |
| Recovery validation | Critical systems with successful restore evidence / target systems | State test scope and date |
| Supplier access review | Supplier paths reviewed / identified supplier paths | Unknown paths remain a risk |
| Risk acceptance currency | Accepted risks within review period / accepted risks | Expired acceptance must be visible |

Never combine unrelated measures into a single maturity percentage without a documented scoring model.

# 24. Assessment finding and recommendation report template

For each finding:
- Finding ID and title.
- Affected asset(s) and site.
- Observation: what was directly observed.
- Evidence: exact reference, time and method.
- Expected condition: source or requirement.
- Technical analysis.
- Process and business context.
- Impact and credible consequence.
- Likelihood rationale.
- Severity methodology and limitations.
- Recommendation and alternatives.
- Operational constraints.
- Compensating controls.
- Owner and target date.
- Retest and closure criteria.
- Residual risk and approval.

Avoid unsupported labels such as "critical" without a defined methodology and evidence-based rationale.

# 25. Document control and approval template

| Field | Entry |
|---|---|
| Document_ID | |
| Title | |
| Owner | |
| Author | |
| Technical Reviewer | |
| OT Operations Reviewer | |
| Safety Reviewer, if applicable | |
| Security Approver | |
| Version | |
| Classification | |
| Effective_Date | |
| Review_Date | |
| Supersedes | |
| Related_Documents | |
| Change_Summary | |
| Approval_Reference | |

# 26. Evidence collection and report quality gates

Before final issue:
- [ ] Scope and authorization are traceable.
- [ ] Every material observation has evidence.
- [ ] Evidence source and time are recorded.
- [ ] Facts and interpretation are separated.
- [ ] Asset and process context are validated.
- [ ] Severity methodology is stated.
- [ ] Standards edition and requirement references are verified.
- [ ] Legal requirements have jurisdictional review.
- [ ] Recommendations account for operational constraints.
- [ ] No unsafe or unauthorized action is implied.
- [ ] Owners and due dates are assigned.
- [ ] Exceptions and limitations are visible.
- [ ] Sensitive topology and credentials are removed from broad distribution.
- [ ] Independent technical review is complete.
- [ ] Distribution and document classification are approved.

# 27. Suggested implementation in spreadsheet and document systems

Recommended workbook tabs:
1. Read Me and Data Dictionary
2. Engagement Scope
3. Asset Inventory
4. Asset Interfaces
5. Communication Flows
6. Criticality Assessment
7. Risk Register
8. Zones and Conduits
9. Firewall Review
10. Vulnerability Register
11. Vendor Advisory Applicability
12. Assessment Checklist
13. Passive Monitoring Checklist
14. SOC Use Cases
15. Incident Timeline
16. Evidence Register
17. Backup and Recovery Tests
18. MOC Security Review
19. Supplier Questionnaire
20. AI System Assessment
21. Regulatory Applicability
22. Audit Evidence
23. Remediation Tracker
24. Executive Metrics
25. Change Log

Recommended document pack:
- Engagement charter and rules of engagement.
- Assessment plan and methodology.
- Site-specific architecture and scope.
- Technical findings report.
- Incident response plan and playbooks.
- Backup and recovery procedure.
- MOC security review procedure.
- Supplier security requirements.
- AI system risk assessment.
- Executive posture report.

## 27.1 Spreadsheet quality controls

- Use data validation for controlled status and priority fields.
- Freeze header rows and enable filters.
- Keep one record per row.
- Avoid merged cells in data tables.
- Use stable IDs and linked references.
- Separate raw evidence from calculated fields.
- Protect formula cells and document formulas.
- Record workbook version and owner.
- Avoid macros unless approved and signed.
- Test imports and exports before operational use.
- Apply access controls and encryption according to classification.
- Do not embed passwords, secrets or unrestricted topology.

# 28. Cross-framework mapping worksheet

| Mapping_ID | Source_Framework | Source_Edition | Source_Requirement | Internal_Control_ID | Control_Statement | OT_Asset_or_Process | Evidence_Reference | Applicability | Gap | Owner | Reviewer | Mapping_Rationale |
|---|---|---|---|---|---|---|---|---|---|---|---|

Mapping rules:
- One internal control may support multiple requirements, but document the relationship.
- One requirement may need multiple controls and evidence sources.
- Do not assume equivalence from similar wording.
- Keep legal, contractual, standard and guidance sources distinct.
- Record partial applicability and exclusions.
- Validate exact clause wording against licensed or authoritative material.
- Preserve edition and change history.

# 29. Glossary of reusable field values

| Field family | Controlled values to consider |
|---|---|
| Status | Proposed, Open, In Progress, Pending Review, Accepted, Closed, Rejected, Deferred |
| Applicability | Applicable, Not Applicable, Partially Applicable, Under Review, Unknown |
| Evidence result | Sufficient, Insufficient, Conflicting, Not Available, Not Tested |
| Confidence | High, Medium, Low, Unknown |
| Treatment | Avoid, Mitigate, Transfer/Share, Accept |
| Finding severity | Critical, High, Medium, Low, Informational, using defined methodology |
| Asset lifecycle | Supported, End of Support, Obsolete, Planned, Unknown |
| Test result | Pass, Fail, Partial, Not Tested, Not Applicable |
| Approval | Approved, Rejected, Conditional, Pending |
| Data quality | Verified, Partially Verified, Unverified, Stale, Conflicting |

# 30. References and further reading

Use the exact edition and scope applicable to the engagement. These sources provide frameworks and guidance; the templates in this chapter are original working structures and do not reproduce or certify compliance with the referenced standards.

1. **NIST SP 800-82 Rev. 3, Guide to Operational Technology Security.** https://csrc.nist.gov/pubs/sp/800/82/r3/final
2. **NIST Cybersecurity Framework 2.0.** https://www.nist.gov/cyberframework
3. **NIST SP 800-53 Rev. 5, Security and Privacy Controls.** https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final
4. **ISA/IEC 62443 series.** Industrial automation and control systems security. https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
5. **MITRE ATT&CK for ICS.** https://attack.mitre.org/matrices/ics/
6. **CISA Industrial Control Systems advisories.** https://www.cisa.gov/news-events/ics-advisories
7. **CISA Cross-Sector Cybersecurity Performance Goals.** https://www.cisa.gov/cross-sector-cybersecurity-performance-goals
8. **ISO/IEC 27001.** Information security management systems. https://www.iso.org/standard/27001
9. **ISO/IEC 42001:2023.** Artificial intelligence management systems. https://www.iso.org/standard/81230.html
10. **NIST AI Risk Management Framework.** https://www.nist.gov/itl/ai-risk-management-framework

# 31. Limitations and professional use

These templates are not legal advice, engineering design approval, safety approval, certification evidence or a substitute for the asset owner's procedures. Tailor each record to the site and verify applicable standards, legal requirements and contracts. Protect sensitive operational data. Use qualified OT, process, safety, security and legal reviewers where required.

## Revision history

| Version | Date | Change | Status |
|---|---|---|---|
| 1.0 | 2026-11-17 | Initial OT security templates and professional deliverables playbook | Reusable reference |

## Expansion backlog

1. Native XLSX workbook with data validation, filters, formulas and linked IDs.
2. Editable DOCX engagement charter, assessment plan and report templates.
3. OT risk scoring model with configurable consequence and likelihood scales.
4. IEC 62443 clause-level crosswalk with licensed-source verification.
5. Country-specific legal applicability registers with regulator source links.
6. Sector-specific assessment packs for energy, oil and gas, water, manufacturing and transport.
7. OT SOC detection engineering workbook and test case library.
8. Incident response forms and evidence chain-of-custody pack.
9. AI agent security assessment workbook and evaluation scorecard.
10. Automated document QA, version control and evidence traceability workflow.

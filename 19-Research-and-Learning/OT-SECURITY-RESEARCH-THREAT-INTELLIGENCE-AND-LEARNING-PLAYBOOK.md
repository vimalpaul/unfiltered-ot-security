---
title: "OT Security Research, Threat Intelligence and Professional Learning Playbook"
document_id: "UOTS-19-RESEARCH"
version: "1.0"
status: "Research and learning reference"
owner: "Unfiltered OT Security"
created: "2026-11-17"
last_reviewed: "2026-11-17"
review_due: "2027-02-17"
scope: "OT and ICS threat intelligence, research methods, incident studies, learning resources and evidence management"
classification: "Public"
---

# OT Security Research, Threat Intelligence and Professional Learning Playbook

**Document ID:** UOTS-19-RESEARCH | **Version:** 1.0 | **Status:** Research and learning reference

**Audience:** OT security analysts, threat intelligence teams, incident responders, researchers, SOC engineers, industrial asset owners, consultants, auditors, students and security leaders.

> **Research integrity notice:** This playbook is a research method and curated starting point, not a live threat feed or a claim that every listed source is current, complete or applicable to every sector. Record publication and retrieval dates. Distinguish confirmed facts, vendor statements, government advisories, research hypotheses and unverified reporting. Do not attribute an incident or actor without evidence. Do not reproduce operationally harmful instructions or conduct testing against systems without written authorization.

---

# 1. Purpose

Industrial cybersecurity decisions depend on reliable knowledge of threats, vulnerabilities, incidents, technologies, process environments and defensive controls. Research must be traceable and reproducible, particularly when it informs risk acceptance, incident response, regulatory reporting or investment.

This playbook establishes a consistent method to:
- Discover authoritative OT/ICS security information.
- Evaluate source credibility and evidence quality.
- Track threats, campaigns, malware and incidents.
- Research vulnerabilities and vendor advisories.
- Analyze industrial incidents without overclaiming causation.
- Translate research into detection, prevention, response and recovery improvements.
- Maintain a professional learning and research programme.
- Preserve references, publication dates, versions and uncertainty.
- Use AI to assist research without treating generated content as evidence.

# 2. Research principles

1. Prefer primary sources: regulators, national CERTs, affected vendors, standards bodies, court filings, incident owners and original research.
2. Record the source's exact publication date and the date retrieved.
3. Preserve the original claim and its context.
4. Separate confirmed facts from inference and speculation.
5. Do not equate an indicator, malware family or technique with attribution.
6. Verify product and version applicability before linking an advisory to an asset.
7. Record negative evidence and known visibility gaps.
8. Distinguish a reported incident from a technically confirmed intrusion.
9. Do not infer operational impact solely from IT service disruption.
10. Use independent corroboration for material claims.
11. Respect source licensing, privacy and disclosure restrictions.
12. Review time-sensitive intelligence before operational use.

# 3. Research lifecycle

\`\`\`mermaid
flowchart TD
  A["Define question and decision need"] --> B["Discover primary and secondary sources"]
  B --> C["Capture source metadata and exact claims"]
  C --> D["Assess credibility, recency and limitations"]
  D --> E["Corroborate material facts"]
  E --> F["Analyze relevance to assets, sectors and processes"]
  F --> G["Map threat, vulnerability and control context"]
  G --> H["Peer review and confidence assessment"]
  H --> I["Publish with citations and caveats"]
  I --> J["Track actions, corrections and review date"]
\`\`\`

## 3.1 Define the research question

A good research question states:
- What decision or knowledge gap is being addressed?
- Which sector, technology, asset class or geography is in scope?
- What time period matters?
- What evidence would answer the question?
- What evidence would disconfirm the hypothesis?
- Who will use the result?
- What level of confidence is required?

Avoid broad questions such as "Who is attacking OT?" without a defined sector, timeframe, source set or analytical purpose.

# 4. Source taxonomy and authoritative repositories

The following are starting points. Their existence does not mean each item contains current or relevant intelligence for a specific incident.

## 4.1 Government and national cybersecurity sources

| Source | Scope / value | Research use | Limitations |
|---|---|---|---|
| CISA ICS Advisories | Product vulnerabilities and mitigation information | Vendor and product advisory tracking | Primarily US government publication scope; verify vendor detail |
| CISA ICS Recommended Practices | Defensive guidance for industrial systems | Control and operational guidance | Guidance is not automatically a legal requirement |
| CISA Known Exploited Vulnerabilities Catalog | Vulnerabilities with evidence of exploitation | Exposure prioritization input | Inclusion does not prove exploitation in a particular OT environment |
| US FBI public statements | Public law enforcement information | Incident and attribution context | Public information may be incomplete |
| NCSC UK | UK national cybersecurity guidance and advisories | Threat and defensive research | Jurisdiction and audience matter |
| ENISA | EU cybersecurity publications and threat landscape | Sector and regional research | Reports may aggregate information and use defined scope |
| CERT-EU | EU institutions' cybersecurity advisories | Vulnerability and threat research | Specific constituency and publication scope |
| National CERTs and sector CSIRTs | Country-specific advisories and incident information | Jurisdiction-specific research | Availability, language and disclosure vary |
| CISA Cross-Sector Cybersecurity Performance Goals | Baseline cybersecurity practices | Defensive gap analysis | Not a substitute for applicable sector law or detailed engineering |

Primary links:
- CISA ICS Advisories: https://www.cisa.gov/news-events/ics-advisories
- CISA ICS Recommended Practices: https://www.cisa.gov/resources-tools/resources/ics-recommended-practices
- CISA KEV Catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog
- NCSC UK: https://www.ncsc.gov.uk/
- ENISA: https://www.enisa.europa.eu/
- CERT-EU: https://cert.europa.eu/
- FIRST: https://www.first.org/members/teams/

## 4.2 Standards and technical knowledge sources

| Source | Primary use | Important distinction |
|---|---|---|
| NIST Computer Security Resource Center | NIST publications and drafts | Check final, draft, withdrawn and superseded status |
| ISA / IEC 62443 | Industrial automation and control system security standards | Obtain licensed standards and verify edition |
| MITRE ATT&CK for ICS | Industrial adversary behavior knowledge base | A technique mapping is not proof of an event |
| MITRE ATLAS | Adversarial AI system techniques | Applies to AI system threat research, not OT attribution |
| NIST AI RMF | AI risk governance | Guidance; not an OT incident database |
| OWASP | Application and AI application security | Use for applicable software components |
| FIRST CVSS | Vulnerability severity scoring specification | Severity is not a complete OT risk assessment |
| FIRST EPSS | Exploitation probability estimation | A model output, not confirmation of exploitation at a site |

Links:
- NIST CSRC: https://csrc.nist.gov/publications
- ISA/IEC 62443: https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
- ATT&CK for ICS: https://attack.mitre.org/matrices/ics/
- MITRE ATLAS: https://atlas.mitre.org/
- FIRST CVSS: https://www.first.org/cvss/
- FIRST EPSS: https://www.first.org/epss/

## 4.3 Vendor and product security sources

For each relevant OEM and product, identify:
- Product security advisory portal.
- Security response team and disclosure policy.
- Product lifecycle and end-of-support notices.
- Firmware and software release notes.
- Security hardening guides.
- Supported configurations.
- Known limitations and mitigations.
- Contact and escalation process.

Use the affected product's official advisory as the primary source for version applicability. A third-party article may help discover an issue but should not replace the vendor's affected-version statement.

## 4.4 Research and academic sources

| Repository | Use | Evaluation |
|---|---|---|
| IEEE Xplore | Engineering and security research | Review paper type, methodology and access limitations |
| ACM Digital Library | Computing and security research | Assess peer review and reproducibility |
| USENIX | Systems and security research | Read methods, datasets and limitations |
| arXiv | Preprints and early research | Not necessarily peer reviewed |
| Google Scholar | Discovery of publications | Follow through to original publisher |
| Crossref | DOI and publication metadata | Metadata does not validate findings |
| Semantic Scholar | Research discovery and citation context | Verify against original paper |
| NIST publications | Government technical research | Check status and scope |

Links:
- IEEE Xplore: https://ieeexplore.ieee.org/
- ACM Digital Library: https://dl.acm.org/
- USENIX: https://www.usenix.org/publications
- arXiv: https://arxiv.org/
- Crossref: https://www.crossref.org/
- Semantic Scholar: https://www.semanticscholar.org/

# 5. Source credibility and evidence grading

Do not treat every source equally. Assess source authority, proximity to the event, technical detail, corroboration, recency and incentives.

## 5.1 Suggested evidence grades

| Grade | Description | Example |
|---|---|---|
| A | Primary authoritative evidence with clear scope and technical detail | Official vendor advisory, regulator notice, published incident report by responsible entity |
| B | Credible independent corroboration or well-documented technical research | Peer-reviewed paper, national CERT analysis, independently validated forensic research |
| C | Reputable secondary reporting with named sources and supporting references | Established media report citing primary statements |
| D | Single-source claim, incomplete disclosure or unclear methodology | Vendor marketing claim, unattributed report, incomplete incident summary |
| E | Unverified, speculative or anonymous claim without corroboration | Social post or copied claim with no traceable evidence |

Grades describe evidence quality for a particular claim, not the general reputation of an organization. A primary source may be authoritative about its own advisory but not about an unrelated actor attribution.

## 5.2 Confidence language

Use explicit terms:
- Confirmed: supported by authoritative evidence for the stated claim.
- High confidence: multiple independent and consistent sources or strong technical evidence.
- Moderate confidence: credible evidence exists but material gaps remain.
- Low confidence: limited or indirect evidence.
- Unknown: insufficient evidence to make a judgment.
- Disputed: credible sources conflict.

State what the confidence applies to. For example, "high confidence that a vendor advisory affects version X" is not the same as "high confidence that a site was exploited."

# 6. Threat intelligence record

| Field | Description |
|---|---|
| Intelligence_ID | Stable record identifier |
| Title | Concise description |
| Type | Actor, campaign, malware, technique, incident, indicator, advisory |
| Sector | Relevant industrial sector |
| Geography | Country or region, only when supported |
| Publication_Date | Source publication date |
| Retrieved_Date | Research retrieval date |
| Primary_Source | Original source |
| Corroborating_Sources | Independent sources |
| Claim_Summary | Neutral description |
| Affected_Technology | Verified product or asset class |
| ATT&CK_ICS_Mapping | Technique IDs with rationale |
| Indicator_References | Controlled indicator records |
| Evidence_Grade | A-E with explanation |
| Confidence | Defined confidence term |
| Limitations | Known information gaps |
| Defensive_Relevance | Detection, prevention, response or recovery implication |
| Analyst | Researcher |
| Review_Date | Next review |
| Status | Current, Superseded, Withdrawn, Under Review |

Do not publish sensitive indicators or details that could enable harm without checking disclosure rules and operational context.

# 7. Threat actor and campaign research

A threat actor profile should be evidence-led and should not merge different groups merely because they use similar tools or target similar sectors.

Record:
- Name and aliases exactly as used by each source.
- Source attribution and publication date.
- Whether attribution is government, vendor, academic or media.
- Targeted sectors and geographies as reported.
- Time period and campaign boundaries.
- Initial access observations.
- Known tools and malware with source attribution.
- ATT&CK for ICS techniques where evidence supports mapping.
- Operational objectives as assessed by the source.
- Confidence and alternative explanations.
- Contradictory reporting.
- Defensive opportunities.
- Last verified date.

## 7.1 Attribution safeguards

- Separate technical behavior from actor identity.
- Do not infer nationality or sponsorship from language, IP address or working hours.
- Do not treat malware reuse as definitive attribution.
- Preserve source-specific naming and alias disagreements.
- Distinguish the source's assessment from your own.
- Do not turn an allegation into a confirmed fact.

# 8. ICS malware research catalogue

Research malware by behavior, affected platform, delivery context, impact and source evidence. Avoid treating every malware family as an OT-native payload.

Potential research categories:
- Windows malware used in environments with OT connectivity.
- Industrial protocol-aware malware.
- Controller or engineering project manipulation.
- Wiper and destructive malware affecting industrial support systems.
- Ransomware affecting enterprise services and operational dependencies.
- Remote access trojans and credential theft.
- Firmware and boot-level threats.
- Supply-chain compromise.
- Linux and embedded device malware.
- Cloud and remote-management abuse affecting industrial operations.

## 8.1 Malware research record

| Field | Description |
|---|---|
| Malware_ID | Stable identifier |
| Family_Name | Source-specific name |
| Aliases | Source and naming caveats |
| First_Reported | Date and source |
| Primary_Analysis | Original technical analysis |
| Affected_Platforms | Verified systems |
| OT_Relevance | Direct, indirect, adjacent, unknown |
| Behaviors | Evidence-based summary |
| ATT&CK_Mapping | Supported techniques |
| Indicators | Restricted reference |
| Process_Impact | Confirmed or hypothesized, clearly labeled |
| Detection_Opportunities | Defensive recommendations |
| Mitigations | Authoritative guidance |
| Confidence | Claim-specific confidence |
| Review_Date | Next review |

## 8.2 Historical research starting points

Examples often discussed in industrial cybersecurity literature include Stuxnet, Industroyer/CrashOverride, TRITON/TRISIS, Industroyer2, PIPEDREAM/INCONTROLLER and destructive malware incidents affecting industrial organizations. Treat each as a separate research case; verify exact names, variants, timelines, technical claims and consequences from original reports. Do not infer that a historical tool is currently active or that a similar incident has the same actor.

Useful primary research starting points:
- CISA ICS Advisories: https://www.cisa.gov/news-events/ics-advisories
- Dragos research: https://www.dragos.com/resources/
- Mandiant research: https://cloud.google.com/blog/topics/threat-intelligence
- ESET research: https://www.welivesecurity.com/
- Microsoft Security research: https://www.microsoft.com/en-us/security/blog/
- Symantec / Broadcom threat research: https://symantec-enterprise-blogs.security.com/

Vendor research is valuable technical evidence but may reflect the vendor's visibility, customer base, telemetry and analytic judgments. Record those limitations.

# 9. Industrial incident case study method

Do not publish a case study as a narrative of certainty when public evidence is incomplete.

## 9.1 Required structure

1. Case identifier and title.
2. Organization and sector, only as publicly disclosed.
3. Incident date and reporting timeline.
4. Primary sources and independent corroboration.
5. Known affected systems.
6. Confirmed technical sequence.
7. Reported but unconfirmed claims.
8. Operational and safety consequences.
9. Business and service consequences.
10. Recovery and restoration facts.
11. Regulatory or government response.
12. ATT&CK for ICS mapping, with evidence.
13. Defensive lessons.
14. Unknowns and contradictory reporting.
15. Researcher confidence and review date.

## 9.2 Incident evidence matrix

| Claim_ID | Claim | Source | Source_Type | Direct_or_Indirect | Corroboration | Evidence_Grade | Confidence | Caveat |
|---|---|---|---|---|---|---|---|---|

## 9.3 Consequence classification

Distinguish:
- IT service disruption.
- Loss of view.
- Loss of control.
- Manipulation of process data.
- Unauthorized control action.
- Equipment damage.
- Safety impact.
- Environmental impact.
- Production interruption.
- Data disclosure.
- Recovery and restoration delay.

Do not infer loss of control or physical impact from a reported IT outage unless supported by evidence.

# 10. Industrial incident research themes

Use these as research categories, not claims of specific current incidents.

| Sector | Research questions |
|---|---|
| Oil and gas | Remote access, enterprise-to-OT dependencies, pipeline telemetry, engineering access |
| Refining and petrochemicals | DCS and SIS boundaries, process availability, vendor support |
| LNG | Distributed dependencies, remote operations, recovery and safety governance |
| Power generation | Control system access, engineering workstations, plant operations continuity |
| Transmission and distribution | Substation communications, protection engineering, remote access |
| Renewables | Inverter fleets, vendor connectivity, distributed asset management |
| Water and wastewater | Remote telemetry, operator visibility, public health and continuity |
| Manufacturing | PLC and HMI dependencies, production disruption, product quality |
| Mining | Remote operations, wireless infrastructure, fleet systems |
| Maritime and ports | Terminal operations, vessel and shore interfaces, supplier dependencies |
| Rail and transport | Signalling support systems, control centre dependencies, safety assurance |
| Airports | Baggage, building management, access and operational service dependencies |
| Building automation | HVAC, access control, energy management and connected devices |
| Data centres | Power, cooling, environmental monitoring and facility dependencies |

# 11. Vulnerability and advisory research

Use a source hierarchy:
1. Affected product vendor's security advisory.
2. National CERT or regulator advisory.
3. CVE record and CNA information.
4. CISA KEV where relevant.
5. NVD enrichment and scoring, where available.
6. Independent technical research.
7. Secondary reporting.

## 11.1 Advisory research checklist

- [ ] Exact vendor and product identified.
- [ ] Affected versions checked against official advisory.
- [ ] Fixed versions and mitigations checked.
- [ ] Product lifecycle and support status reviewed.
- [ ] Preconditions and attack vector recorded.
- [ ] Authentication and privilege requirements recorded.
- [ ] Network exposure assessed from verified architecture.
- [ ] Exploitation evidence distinguished from theoretical exploitability.
- [ ] CVSS version and score source recorded.
- [ ] EPSS date and meaning recorded if used.
- [ ] KEV status and date checked if relevant.
- [ ] OEM mitigation and process constraints recorded.
- [ ] Site-specific risk decision assigned to accountable owner.

## 11.2 Research tools and data sources

- CVE Program: https://www.cve.org/
- NIST NVD: https://nvd.nist.gov/
- CISA KEV: https://www.cisa.gov/known-exploited-vulnerabilities-catalog
- FIRST EPSS: https://www.first.org/epss/
- FIRST CVSS: https://www.first.org/cvss/
- Vendor product security portals.

A CVE record does not prove that a particular industrial installation is affected. Product matching, configuration and vendor guidance must be verified.

# 12. MITRE ATT&CK for ICS research and mapping

Use ATT&CK for ICS to structure behavioral analysis and defensive coverage. It is a knowledge base, not a compliance standard or proof of compromise.

For each technique mapping:
- Record technique ID and exact name.
- Record ATT&CK version or retrieval date.
- Link the source behavior and exact evidence.
- State whether the behavior was observed, reported or simulated.
- Identify the affected process or asset role.
- Identify potential detection and prevention controls.
- Record known visibility limitations.
- Assign confidence.
- Avoid mapping based solely on tool name or broad similarity.

Official resource: https://attack.mitre.org/matrices/ics/

# 13. Threat intelligence production and dissemination

## 13.1 Intelligence products

| Product | Audience | Purpose |
|---|---|---|
| Strategic assessment | Executive leadership | Long-term risk and investment context |
| Operational intelligence | SOC and incident management | Campaign and incident context |
| Tactical intelligence | Detection engineers and defenders | Techniques, behaviors and defensive opportunities |
| Technical advisory digest | Asset and product owners | Product/version applicability and mitigation |
| Sector alert | Industry stakeholders | Relevant verified information and action |
| Research note | Engineers and researchers | Detailed analysis and limitations |

## 13.2 Intelligence report template

- Title and unique ID.
- Executive summary.
- Key judgments with confidence.
- Scope and timeframe.
- Sources and collection method.
- Confirmed facts.
- Analysis and inference.
- Affected sectors and technology.
- Indicators and behavior references, if safe to disclose.
- ATT&CK for ICS mapping.
- Defensive recommendations.
- Known gaps and caveats.
- Analyst and reviewer.
- Publication and review date.
- Distribution and handling marking.

# 14. Research-to-control traceability

A research finding becomes useful when it leads to a justified defensive decision.

\`\`\`mermaid
flowchart LR
  INTEL["Research or incident evidence"] --> CLAIM["Verified claim and confidence"]
  CLAIM --> SCENARIO["Threat or failure scenario"]
  SCENARIO --> ASSET["Affected asset and process context"]
  ASSET --> RISK["Risk assessment"]
  RISK --> CONTROL["Candidate security controls"]
  CONTROL --> DETECT["Detection and response use cases"]
  CONTROL --> GOVERN["Policy, architecture or change action"]
  DETECT --> TEST["Controlled validation"]
  GOVERN --> TEST
  TEST --> EVIDENCE["Evidence and assurance record"]
  EVIDENCE --> REVIEW["Periodic review and feedback"]
\`\`

Traceability record:
| Research_ID | Claim_ID | Scenario_ID | Asset_Class | Risk_ID | Control_ID | Detection_ID | Test_ID | Evidence_Ref | Owner |
|---|---|---|---|---|---|---|---|---|---|

Do not force every research item into a control. Some information may be contextual, low confidence or not relevant to the organization's environment.

# 15. Professional research methodology

A repeatable research method should include:
1. Research question and scope.
2. Search strategy and source list.
3. Inclusion and exclusion criteria.
4. Source metadata capture.
5. Claim extraction.
6. Evidence grading.
7. Independent corroboration.
8. Technical analysis.
9. Alternative explanations.
10. Confidence assessment.
11. Peer review.
12. Citation and publication.
13. Correction process.
14. Scheduled review.

For quantitative or academic research, additionally record:
- Dataset origin and licensing.
- Sampling and selection bias.
- Ground truth definition.
- Experimental environment.
- Tool and software versions.
- Parameters and assumptions.
- Reproducibility steps.
- Statistical limitations.
- Conflicts of interest and funding.
- Ethics and disclosure review.

# 16. Research ethics and responsible disclosure

- Respect coordinated vulnerability disclosure.
- Do not publish secrets, credentials or sensitive operational topology.
- Do not release exploit instructions that materially increase risk to exposed critical infrastructure.
- Obtain permission before testing or collecting non-public information.
- Protect personal and commercially sensitive data.
- Respect source licenses and publication terms.
- Do not misrepresent authorship, evidence or confidence.
- Correct material errors transparently.
- Separate research from marketing claims.
- Coordinate with affected vendors and asset owners where appropriate.
- Follow applicable legal and contractual restrictions.

# 17. AI-assisted threat research

AI can assist with source discovery, document summarization, entity normalization, timeline drafting and candidate mappings. It must not be treated as an independent source of truth.

Controls:
- Retrieve primary sources and cite exact URLs.
- Preserve original source text and metadata within permitted licensing.
- Treat documents and web content as untrusted input.
- Test indirect prompt injection.
- Verify names, dates, versions and indicators.
- Do not invent threat actors, campaigns or CVEs.
- Keep source claims separate from model inference.
- Require human review before publishing intelligence.
- Record model, prompt and retrieval versions for material outputs.
- Do not upload restricted incident data to an unapproved model provider.

## 17.1 AI research workflow

\`\`\`mermaid
flowchart TD
  Q["Analyst research question"] --> SEARCH["Approved source discovery"]
  SEARCH --> FETCH["Retrieve primary documents"]
  FETCH --> META["Capture provenance and dates"]
  META --> EXTRACT["AI-assisted claim extraction"]
  EXTRACT --> VERIFY["Human source verification"]
  VERIFY --> CORR["Independent corroboration"]
  CORR --> ANALYZE["Analyst assessment and confidence"]
  ANALYZE --> REVIEW["Peer review"]
  REVIEW --> PUBLISH["Controlled intelligence product"]
  PUBLISH --> TRACK["Correction and review tracking"]
\`\`

# 18. Research repository and knowledge management

Recommended structure:
- sources/
- advisories/
- incidents/
- malware/
- threat-actors/
- campaigns/
- sectors/
- protocols/
- vulnerabilities/
- standards/
- academic-papers/
- detection-research/
- ai-security/
- learning-paths/
- corrections/
- retired/

Each research record should include:
- Stable ID.
- Title.
- Source URL and publisher.
- Publication date.
- Retrieval date.
- Author or organization.
- Source type.
- Sector and technology tags.
- Summary in original wording.
- Claims and evidence references.
- Confidence and caveats.
- Related records.
- Reviewer.
- Next review date.
- Status and supersession link.

Do not commit confidential customer incident evidence, credentials, exploitable topology, licensed standards text or personal data to a public repository.

# 19. Professional learning pathways

Learning pathways should connect process knowledge, technical skills, security engineering and governance. A course completion certificate is not proof of practical competence.

## 19.1 Foundation pathway

- Industrial control system concepts.
- Process operations and instrumentation.
- PLC, RTU, HMI, SCADA and DCS roles.
- Industrial networking fundamentals.
- Purdue reference model and zones/conduits.
- OT safety, availability and change management.
- Basic incident and risk terminology.

## 19.2 OT security engineering pathway

- Asset inventory and architecture review.
- Passive network monitoring.
- Industrial protocol analysis.
- Network segmentation and secure remote access.
- Vulnerability applicability and vendor advisories.
- Endpoint and engineering workstation hardening.
- Backup, recovery and configuration integrity.
- Authorized assessment planning.

## 19.3 OT SOC and incident response pathway

- OT telemetry and asset context.
- Detection engineering and ATT&CK for ICS.
- Alert triage and process consequence.
- Incident command and operational escalation.
- Evidence preservation.
- Tabletop exercises and recovery validation.
- Threat intelligence analysis.

## 19.4 Governance, risk and assurance pathway

- IEC 62443 series structure.
- NIST SP 800-82.
- Risk assessment and treatment.
- Regulatory applicability.
- Supplier security.
- MOC and lifecycle management.
- Audit evidence and executive reporting.

## 19.5 Advanced and specialist pathways

- Industrial malware research.
- Digital twins and cyber ranges.
- Industrial protocol security research.
- AI and agentic SOC security.
- Safety-aware security engineering.
- Sector-specific security architecture.
- Research methods and technical publication.

# 20. Books, courses and learning resources

Treat the following as discovery starting points. Verify current editions, availability, syllabus, instructor qualifications, prerequisites, pricing and accreditation directly with the publisher or provider.

| Resource | Focus | How to use |
|---|---|---|
| NIST SP 800-82 Rev. 3 | OT security guidance | Core reference for architecture and security context |
| CISA ICS training and resources | Industrial cybersecurity learning | Review current course availability and eligibility |
| MITRE ATT&CK for ICS | Adversary behavior | Technique analysis and detection mapping |
| ISA/IEC 62443 training | Industrial cybersecurity standards | Learn the standards structure and role-based application |
| SANS ICS training | Specialist OT security | Review course prerequisites and current syllabus |
| University research programmes | Industrial control and cyber-physical systems | Study methods, labs and research publications |
| Vendor technical training | Product-specific engineering | Learn only the supported product and version scope |

Links:
- CISA training: https://www.cisa.gov/ics-training-available-through-cisa
- ISA training: https://www.isa.org/training
- SANS ICS: https://www.sans.org/cyber-security-courses/ics-scada-cyber-security/
- NIST publications: https://csrc.nist.gov/publications
- MITRE ATT&CK for ICS: https://attack.mitre.org/matrices/ics/

# 21. Research programme and operating cadence

A research function should have defined priorities and review triggers.

| Activity | Suggested cadence | Trigger for additional review |
|---|---|---|
| Critical vendor advisory review | Daily or according to service criticality | New high-impact advisory or exploited vulnerability |
| Sector threat digest | Weekly or fortnightly | Significant incident or government warning |
| Incident case study review | Monthly | New primary evidence or correction |
| Standards and framework review | Quarterly | New edition, draft or withdrawal |
| Research paper review | Monthly | Material new research |
| Threat actor profile review | Quarterly | New credible attribution or campaign evidence |
| Learning content review | Quarterly | Course or resource changes |
| Source integrity and link review | Quarterly | Broken link or changed publisher |
| Public repository review | Each release | Sensitive data or licensing concern |

These are suggested operating intervals, not claims about the current threat level. Define urgency and service-level targets according to the organization's risk.

# 22. Research quality metrics

| Metric | Definition |
|---|---|
| Primary-source ratio | Material claims supported by primary sources / material claims sampled |
| Claim traceability | Claims with source references / claims published |
| Corroboration rate | High-impact claims with independent corroboration / high-impact claims |
| Freshness compliance | Records reviewed within defined interval / records due |
| Correction rate | Material corrections / published records |
| Applicability verification | Advisories with verified product/version applicability / relevant advisories |
| Mapping quality | ATT&CK mappings with evidence rationale / mappings sampled |
| Research-to-action traceability | Actionable findings linked to owner and decision / actionable findings |
| Peer review completion | Published research records reviewed / records requiring review |
| Reproducibility | Research exercises reproducible from retained method and sources / exercises sampled |

Do not optimize for publication volume at the expense of evidence quality.

# 23. Research correction and retirement procedure

When a source changes or a claim is challenged:
1. Identify affected records and publications.
2. Preserve the previous version.
3. Reopen the original source.
4. Check publisher correction, withdrawal or supersession.
5. Reassess related claims and mappings.
6. Update confidence and conclusions.
7. Record who approved the correction.
8. Publish a visible change note.
9. Notify downstream users where the change affects a decision.
10. Retire stale indicators and content according to policy.

# 24. References and authoritative starting points

1. **CISA ICS Advisories:** https://www.cisa.gov/news-events/ics-advisories
2. **CISA ICS Recommended Practices:** https://www.cisa.gov/resources-tools/resources/ics-recommended-practices
3. **CISA Known Exploited Vulnerabilities Catalog:** https://www.cisa.gov/known-exploited-vulnerabilities-catalog
4. **NIST SP 800-82 Rev. 3:** https://csrc.nist.gov/pubs/sp/800/82/r3/final
5. **MITRE ATT&CK for ICS:** https://attack.mitre.org/matrices/ics/
6. **MITRE ATLAS:** https://atlas.mitre.org/
7. **FIRST CVSS:** https://www.first.org/cvss/
8. **FIRST EPSS:** https://www.first.org/epss/
9. **NVD:** https://nvd.nist.gov/
10. **CVE Program:** https://www.cve.org/
11. **ENISA:** https://www.enisa.europa.eu/
12. **NCSC UK:** https://www.ncsc.gov.uk/
13. **CERT-EU:** https://cert.europa.eu/
14. **IEEE Xplore:** https://ieeexplore.ieee.org/
15. **ACM Digital Library:** https://dl.acm.org/
16. **USENIX:** https://www.usenix.org/publications
17. **arXiv:** https://arxiv.org/
18. **ISA/IEC 62443 series:** https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards

# 25. Limitations and professional use

This playbook is not a live threat intelligence service, legal opinion, incident attribution, vulnerability verification for a specific asset or guarantee of completeness. Sources can be incomplete, delayed, revised or withdrawn. Confirm current information with the original publisher before using it for operational, regulatory or risk decisions.

## Revision history

| Version | Date | Change | Status |
|---|---|---|---|
| 1.0 | 2026-11-17 | Initial research, threat intelligence and professional learning playbook | Research reference |

## Specialist expansion backlog

1. Source-by-source ingestion and metadata schema.
2. Verified incident case studies with primary-source evidence matrices.
3. Malware family research catalogue with original report references.
4. Country and sector CERT directory with scope and review date.
5. Vendor advisory collection and deduplication workflow.
6. ATT&CK for ICS technique-to-detection evidence catalogue.
7. Research paper review template and reproducibility checklist.
8. Threat intelligence publication templates for strategic, operational and tactical audiences.
9. Public repository source-link and citation validation automation.
10. Controlled AI research assistant with provenance and human review.

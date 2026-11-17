# OT Security AI Agent Use Case Catalogue

## Design objective

Use AI to reduce research and documentation effort while keeping humans accountable for engineering, safety, security, and compliance decisions.

## Use cases

| Use case | Inputs | Agent output | Required human validation |
|---|---|---|---|
| Asset normalization | Approved asset export | Normalized records and missing fields | Asset owner confirms identity and criticality |
| Advisory matching | Product and version inventory | Candidate advisories and affected-version evidence | Engineer confirms exact applicability |
| Threat brief | Public threat reports | Source-linked summary and ATT&CK mapping | Analyst validates attribution and relevance |
| Regulatory extraction | Official public instrument | Requirement register draft | Compliance/legal reviewer confirms scope and legal status |
| Architecture review | Sanitized diagrams and flow inventory | Potential boundary and documentation gaps | OT architect validates design |
| Alert triage | Sanitized logs and alert context | Timeline and investigation questions | SOC and operations validate event context |
| Incident reporting | Approved incident notes | Draft chronology and report | Incident commander approves facts and disclosure |
| Control evidence index | Policies and sanitized evidence metadata | Evidence-to-control candidate links | Control owner confirms sufficiency |
| Risk workshop support | Scenario and asset context | Structured risk register draft | Risk owner and engineering validate consequence |
| Learning assistant | Curated repository content | Explanations and exercises | Technical editor reviews accuracy |

## Common controls

- Read-only data access by default
- Explicit source allow-list
- Prompt injection resistance
- Evidence provenance and citation checks
- Sensitive data minimization
- Output uncertainty and confidence labels
- Human approval gates
- Audit logs and reproducibility
- Evaluation with synthetic and known-answer datasets

## Prohibited autonomous actions

Agents must not directly control industrial processes, issue commands to controllers, modify safety systems, run active discovery against production networks, isolate critical assets, approve risk acceptance, or submit compliance attestations.

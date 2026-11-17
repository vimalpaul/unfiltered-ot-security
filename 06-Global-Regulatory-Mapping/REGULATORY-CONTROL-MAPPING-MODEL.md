# Regulatory and Standards Control Mapping Model

## Purpose

Define a repeatable data model for connecting legal and regulatory instruments, standards, controls, technical requirements, industrial assets, and evidence.

## Core entities

### Jurisdiction
- Jurisdiction ID
- Country or territory
- Subnational authority, if applicable
- Official government portal
- Responsible regulator

### Instrument
- Instrument ID
- Exact title and identifier
- Issuer
- Instrument type
- Version, edition, and amendment
- Publication and effective dates
- Status and supersession
- Official source URL
- Access date
- Legal basis and applicability scope

### Requirement
- Requirement ID as published
- Parent instrument
- Original source locator
- Original wording reference, not copied wholesale
- Project summary in original language
- Mandatory or advisory status
- Covered entity and sector
- Applicability conditions
- Implementation deadline, if any

### Control
- Project control ID
- Control objective
- Asset or process scope
- Preventive, detective, responsive, or recovery function
- Responsible role
- Implementation guidance
- Evidence examples
- Verification method

### Mapping
- Source requirement ID
- Target control or framework ID
- Relationship: direct, partial, supporting, or no demonstrated relationship
- Rationale
- Confidence
- Reviewer
- Review date
- Known limitations

## Mapping rules

1. Never map based on title similarity alone.
2. Preserve source identifiers and edition.
3. Record jurisdiction and entity applicability separately from technical similarity.
4. Explain whether the mapping is legal, contractual, technical, or advisory.
5. A technical control may support several requirements without satisfying all of them.
6. A mapping does not establish compliance or certification.
7. Mark unknown or unverified mappings explicitly.
8. Do not reproduce copyrighted normative text; use short references and original summaries.

## Example relationship labels

- **Direct:** The target control addresses substantially the same control objective within the stated scope.
- **Partial:** The target control addresses only some aspects or has a narrower scope.
- **Supporting:** The target control contributes evidence or implementation support but does not satisfy the requirement alone.
- **No demonstrated relationship:** Evidence is insufficient to establish a meaningful mapping.

## Evidence status

- Not assessed
- Evidence requested
- Evidence received
- Reviewed and adequate for stated test
- Gap identified
- Not applicable with rationale
- Not verified

Do not use "compliant" unless a qualified assessment has been performed against the complete applicable requirement set and the responsible authority or assessor has accepted the conclusion.

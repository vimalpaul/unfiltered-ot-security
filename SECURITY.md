# Security Policy

## Purpose

This repository is a public educational reference. It is not an operational service and must not be used as authorization to test, scan, access, or modify any industrial environment.

## Reporting a vulnerability in this repository

For vulnerabilities in repository code, workflows, or publishing infrastructure, use GitHub's private vulnerability reporting feature if enabled. Otherwise contact the repository maintainer privately through a trusted channel. Do not publish exploit details in a public issue before maintainers have assessed the report.

Include the affected path or workflow, impact, reproducible evidence that does not expose secrets, and a suggested mitigation where possible.

## Industrial environment safety

- Never test a live PLC, RTU, DCS, SCADA, SIS, protection relay, safety controller, or production network without explicit written authorization and an approved site-specific plan.
- Passive observation is not automatically risk-free. Obtain site approval and assess sensor placement, network load, mirroring behavior, and data handling.
- Do not run vulnerability scanners, fuzzers, exploit code, protocol writes, or stress tests against production OT unless specifically approved by the asset owner, engineering authority, and safety stakeholders.
- Use isolated simulators, digital twins, hardware test benches, or dedicated lab networks for active exercises.
- Do not bypass interlocks, safety instrumented functions, process protections, or emergency procedures.
- Follow responsible disclosure requirements of vendors and affected organizations.

## Secrets and sensitive information

Never commit passwords, API tokens, private keys, customer records, facility identifiers, sensitive topology diagrams, or non-public incident information. If a secret is exposed, revoke or rotate it immediately; deleting the commit alone is not sufficient.

## Scope

This policy covers material maintained in this repository. It does not provide a vulnerability disclosure channel for third-party products, vendors, regulators, or industrial facilities.

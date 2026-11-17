# OT Security Tool Categories

## Purpose

Classify tools by function and operational risk. Inclusion is not an endorsement, certification, or assurance of compatibility with every industrial product.

## Tool categories

| Category | Typical purpose | Operational caution |
|---|---|---|
| Passive network monitoring | Observe communications and build baselines | Validate TAP/SPAN design and sensor impact |
| Asset inventory | Identify devices, software, and relationships | Active probes may disrupt fragile devices |
| Vulnerability management | Correlate versions and advisories | Confirm product/version accuracy; avoid unsafe scans |
| Network security monitoring | Detect unusual traffic and protocol behavior | Tune to process baseline and avoid inline disruption |
| Network segmentation | Enforce approved communication paths | Validate failover and process dependencies |
| Endpoint protection | Protect supported Windows/Linux endpoints | Confirm vendor support and performance impact |
| Application control | Restrict execution on workstations and servers | Test engineering tool compatibility |
| Remote access management | Govern vendor and engineer sessions | Preserve safe emergency access |
| Backup and recovery | Restore configurations and services | Test integrity and recovery sequence |
| Threat intelligence | Enrich threats and vulnerabilities | Validate attribution and applicability |
| SIEM and SOAR | Correlate events and coordinate workflows | Avoid automatic disruptive actions |
| Protocol analysis | Decode and inspect industrial traffic | Prefer offline captures and lab data |

## Selection criteria

Evaluate passive versus active behavior, supported protocols, device coverage, vendor support, deployment topology, latency and performance, data handling, authentication, logging, integration, update lifecycle, licensing, false-positive handling, recovery, and evidence quality.

## Tool assessment record

- Tool and publisher
- Version and support status
- Purpose and deployment model
- Supported products and protocols
- Passive or active capabilities
- Required privileges
- Network and endpoint impact
- Data collection and retention
- Security and update model
- Licensing and operating costs
- Lab validation results
- Operational approval and limitations

## Deployment principle

Do not deploy inline controls or active discovery agents in production OT solely because they are common in IT. Use vendor and asset-owner guidance, representative testing, change management, and a rollback plan.

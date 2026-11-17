# Manufacturing and Factory OT Security

## Scope

Discrete and process manufacturing, assembly, packaging, robotics, machine tools, production lines, MES, quality systems, and industrial edge platforms.

## Representative environment

- PLCs, PACs, remote I/O, drives, and motion controllers
- Robots, cobots, CNC machines, and machine vision
- HMI panels, line supervisory systems, and SCADA
- MES, batch, recipe, and quality systems
- Historians and production data platforms
- Engineering workstations and vendor maintenance systems
- Industrial wireless, scanners, and IIoT gateways
- Building and utility systems supporting production

## Business and operational objectives

Protect personnel, production continuity, recipe and batch integrity, product quality, equipment availability, intellectual property, and traceability.

## Threat scenarios

- Unauthorized recipe or parameter modification
- Ransomware affecting line supervision or MES integration
- Engineering workstation compromise
- Unauthorized robot or motion program changes
- Malware introduced through removable media
- Compromised machine vendor remote access
- Manipulation of quality or production data
- Flat network paths between enterprise and production cells
- Unsupported legacy equipment used as a pivot point

## Security engineering

- Segment production cells and lines based on process and risk.
- Control engineering workstation access and project changes.
- Maintain approved golden configurations and backups.
- Govern vendor maintenance and removable media.
- Monitor PLC program downloads and unusual engineering activity.
- Restrict machine-to-machine and cell-to-enterprise flows to approved requirements.
- Integrate cybersecurity changes with production planning and maintenance.
- Test restoration and line restart procedures with production engineering.

## Operational cautions

A security control can stop a line, invalidate a batch, affect motion safety, or compromise product quality. Validate changes in staging or during approved windows and involve production, safety, quality, and automation engineering.

## Reference families

IEC 62443, NIST SP 800-82, relevant machinery and functional safety standards, product security advisories, and applicable national manufacturing or critical infrastructure requirements.

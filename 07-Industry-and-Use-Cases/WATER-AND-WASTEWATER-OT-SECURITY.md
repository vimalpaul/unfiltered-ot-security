# Water and Wastewater OT Security

## Scope

Water intake, treatment, chemical dosing, pumping, storage, distribution, wastewater collection and treatment, telemetry, and remote facilities.

## Representative assets

- PLCs and RTUs at treatment and pumping facilities
- HMI, SCADA servers, and historians
- Flow, pressure, level, turbidity, pH, and other process instrumentation
- Chemical dosing and handling systems
- Pump, motor, and variable-frequency drive controls
- Remote telemetry and cellular or radio gateways
- Laboratory information and operational reporting systems
- Building, power, and backup systems

## Consequence dimensions

Consider public health, water quality, chemical exposure, environmental discharge, service continuity, equipment damage, and loss of operator visibility.

## Threat scenarios

- Unauthorized change to chemical dosing parameters
- Compromised remote access to a pumping station
- Loss of telemetry from distributed sites
- Ransomware affecting SCADA support systems
- Manipulation or spoofing of process measurements
- Unapproved controller logic change
- Loss of historian and alarm visibility
- Compromise of a supplier or managed service account

## Defensive priorities

- Separate corporate, treatment, distribution, and remote-site networks according to risk.
- Maintain a verified inventory of controllers, gateways, instruments, and communication paths.
- Protect engineering workstations and dosing configuration changes.
- Establish approved remote access with time-limited permissions and monitoring.
- Monitor critical setpoint, logic, alarm, and configuration changes.
- Maintain local operating procedures for communications loss.
- Protect backups and validate restoration.
- Coordinate cybersecurity with water quality, process safety, environmental, and public health stakeholders.

## Assessment cautions

Do not test chemical dosing, pump start/stop, valve operation, controller writes, or telemetry failover on live systems without explicit authorization, process engineering approval, and a documented safe test plan. Use simulated processes and isolated PLC test benches for exercises.

## Reference families

IEC 62443, NIST SP 800-82, applicable drinking water and wastewater regulator requirements, public health requirements, national critical infrastructure controls, and vendor advisories.

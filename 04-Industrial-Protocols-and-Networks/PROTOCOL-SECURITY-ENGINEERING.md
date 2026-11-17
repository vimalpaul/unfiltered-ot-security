# Industrial Protocol Security Engineering

## Purpose

Provide a protocol-neutral method for understanding and securing industrial communications. Protocol behavior and security features vary by edition, profile, vendor, firmware, and deployment.

## Protocol families to cover

| Family | Common contexts | Security topics |
|---|---|---|
| Modbus TCP and serial | PLCs, meters, process devices | Trust model, function codes, segmentation, gateways, monitoring |
| DNP3 | Utilities and telemetry | Authentication extensions, secure deployment, unsolicited responses, time and event integrity |
| OPC UA | Industrial interoperability | Certificates, trust lists, application identity, user identity, secure channels, policy configuration |
| PROFINET | Factory automation | Real-time traffic, device identity, engineering access, segmentation |
| EtherNet/IP and CIP | Industrial automation | Device identity, services, network boundaries, vendor hardening |
| IEC 61850 | Substation automation | GOOSE, MMS, sampled values, engineering files, time synchronization, network protection |
| BACnet | Building automation | Device discovery, routing, segmentation, secure connect deployments |
| HART and WirelessHART | Process instrumentation | Field access, gateways, device configuration, wireless security |
| FOUNDATION Fieldbus | Process automation | Segment design, engineering tools, device lifecycle |
| MQTT and industrial messaging | IIoT and edge integration | Broker identity, topic authorization, TLS, client certificates, bridge security |

## Protocol review method

1. Identify exact protocol, edition, profile, transport, and vendor implementation.
2. Identify endpoints, initiators, responders, gateways, and trust boundaries.
3. Determine whether authentication, authorization, integrity, confidentiality, replay protection, and key management are provided and enabled.
4. Identify engineering and management channels separately from process data.
5. Review broadcast, multicast, discovery, time synchronization, and failover behavior.
6. Determine which communications are safety- or availability-critical.
7. Establish passive monitoring and baseline behavior.
8. Apply segmentation and allow-listing based on approved process flows.
9. Validate controls in a lab or approved maintenance window.
10. Record unsupported devices and compensating controls.

## Common design weaknesses

- Flat networks with broad device reachability
- Unauthenticated or weakly authenticated command paths
- Shared engineering credentials
- Exposed management services
- Uncontrolled vendor access
- Inadequate certificate and key lifecycle management
- Unmonitored protocol gateways
- Unapproved protocol writes
- Insecure time sources
- Incomplete asset and flow inventories

## Safe assessment boundary

Do not issue write commands, fuzz, scan aggressively, or test malformed packets against production devices without explicit authorization, vendor and site approval, process safety review, and a documented test plan. Prefer passive capture, offline protocol analysis, and representative lab devices.

## Per-protocol page template

Create one page per protocol with: overview, architecture, message model, transport, security features, deployment options, common weaknesses, passive monitoring, secure configuration, vendor differences, safe lab, relevant standards, and primary references.

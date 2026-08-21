# VLAN Design

VLANs can separate traffic logically on a managed switched network.

## Example

| VLAN | Name | Subnet | Purpose |
|---:|---|---|---|
| 10 | MGMT | 192.168.10.0/24 | Network management |
| 20 | STAFF | 192.168.20.0/24 | Staff devices |
| 30 | GUEST | 192.168.30.0/24 | Guest Wi-Fi |
| 40 | CCTV | 192.168.40.0/24 | Cameras/NVR |

## Access ports

An access port normally carries one untagged VLAN for an endpoint.

Examples:

- Staff PC → VLAN 20
- Camera → VLAN 40
- Management laptop → VLAN 10

## Trunk ports

A trunk/uplink can carry multiple VLANs between compatible network devices.

Examples:

- Router ↔ managed switch
- Switch ↔ access point
- Switch ↔ another managed switch

The exact tagging/native-VLAN configuration depends on the equipment vendor and topology.

## Security

Inter-VLAN traffic should be controlled by firewall policies. Guest networks should normally have restricted access to internal business and management networks.

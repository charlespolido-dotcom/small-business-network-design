# IP Addressing Plan

Use private IPv4 ranges for internal networks. The following example uses separate /24 networks for different functions.

| Network | Example CIDR | Gateway | Typical use |
|---|---|---|---|
| Management | 192.168.10.0/24 | 192.168.10.1 | Network equipment |
| Staff | 192.168.20.0/24 | 192.168.20.1 | PCs and business devices |
| Guest | 192.168.30.0/24 | 192.168.30.1 | Guest Wi-Fi |
| CCTV | 192.168.40.0/24 | 192.168.40.1 | Cameras/NVR |

## DHCP planning

A DHCP scope should document:

- Network address
- Gateway
- DNS servers
- Lease range
- Reserved addresses
- Lease duration

Reserve addresses for infrastructure that needs predictable addressing, such as switches, access points, NVRs, printers, and servers.

Do not copy this example directly into production without checking the existing network.

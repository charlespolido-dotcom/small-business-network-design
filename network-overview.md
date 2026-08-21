# Network Overview

A small-business network normally combines an internet connection, router/firewall, switching, wireless access points, and endpoint devices.

## Recommended logical flow

```text
ISP
 |
ONT/Modem
 |
Router/Firewall
 |
Managed Switch
 |---- Staff computers
 |---- Printers
 |---- Wireless APs
 |---- CCTV/PoE
 |---- NAS/Servers
```

## Core responsibilities

### Router/firewall

- Internet gateway
- DHCP
- DNS forwarding
- NAT
- Firewall rules
- VPN where required

### Managed switch

- VLAN assignment
- Trunk/uplink connectivity
- PoE for compatible devices
- Port monitoring

### Wireless access points

- Staff SSID
- Guest SSID
- Optional dedicated IoT/CCTV wireless networks
- Centralized management when available

## Documentation

Record:

- Device hostname
- Management IP
- Physical location
- Switch port
- VLAN
- Serial number
- Firmware version
- Backup location

Never publish real customer credentials, public IP addresses, VPN secrets, API keys, or other sensitive information in a public repository.

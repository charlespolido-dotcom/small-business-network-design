# Small Business Network Design Guide

Practical reference material for planning a reliable small-business network.

**Maintainer:** Charles Polido  
**Focus:** Network design, Wi-Fi, MikroTik, switching, VLANs, PoE/CCTV, and troubleshooting in small-business environments.

🌐 **Portfolio:** https://portfolio-6yu.pages.dev/

> This repository is an educational/reference project. Configuration examples are generic and should be adapted and tested for the actual network, ISP, hardware, and security requirements.

## What this project covers

- Small-business network architecture
- IP addressing and DHCP planning
- VLAN segmentation
- Wi-Fi design
- PoE and CCTV network considerations
- Basic MikroTik concepts
- Network troubleshooting
- Documentation and change-management practices

## Example topology

```text
                    Internet / ISP
                          |
                    [ISP Modem/ONT]
                          |
                    [Router / Firewall]
                          |
                    [Managed Switch]
              _________|_____|__________
             |         |     |          |
          [Office]   [APs] [CCTV]   [Servers/NAS]
             |         |     |
          PCs/Printers Wi-Fi  Cameras
```

See [`diagrams/network-topology.md`](diagrams/network-topology.md) for the design notes.

## Documentation

- [Network overview](docs/network-overview.md)
- [IP addressing](docs/ip-addressing.md)
- [VLAN design](docs/vlan-design.md)
- [Wi-Fi design](docs/wifi-design.md)
- [CCTV network](docs/cctv-network.md)
- [Troubleshooting](docs/troubleshooting.md)

## Design principles

1. Keep the network simple enough to troubleshoot.
2. Separate important traffic where appropriate.
3. Document IP addresses, VLANs, ports, and equipment.
4. Use strong authentication and change default credentials.
5. Avoid exposing management interfaces directly to the public internet.
6. Back up router and switch configurations.
7. Test changes before applying them to production.
8. Label physical cabling and network equipment.

## Example IP plan

| Purpose | Example subnet | Example gateway |
|---|---|---|
| Management | 192.168.10.0/24 | 192.168.10.1 |
| Staff | 192.168.20.0/24 | 192.168.20.1 |
| Guest Wi-Fi | 192.168.30.0/24 | 192.168.30.1 |
| CCTV | 192.168.40.0/24 | 192.168.40.1 |

These are example private addresses, not a recommendation for every deployment.

## MikroTik note

A MikroTik router can provide routing, DHCP, DNS forwarding, firewalling, NAT, VPN, and bandwidth-management functions. Exact commands depend on the RouterOS version and network design, so test configurations in a lab or maintenance window before production use.

## Troubleshooting workflow

When a device cannot reach the network:

1. Check power and physical link.
2. Check Ethernet/fiber connections.
3. Check link/activity LEDs.
4. Verify the device IP address and gateway.
5. Test the local gateway.
6. Test another device on the same network.
7. Check DHCP leases.
8. Check VLAN membership and switch ports.
9. Check firewall/NAT rules when internet access is affected.
10. Review logs and recent configuration changes.

## About the author

Charles Polido is an IT and networking professional focused on practical technology solutions, including network infrastructure, Wi-Fi, fiber optic connectivity, troubleshooting, and IT support.

For professional services and project inquiries:

**Portfolio:** https://portfolio-6yu.pages.dev/

## Disclaimer

The examples in this repository are for educational and planning purposes. Always verify vendor documentation and test changes before applying them to a production network.

## License

This project is released under the MIT License. See [`LICENSE`](LICENSE).

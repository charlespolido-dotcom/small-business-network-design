# Example Network Topology

```text
                         INTERNET
                            |
                         [ ISP ]
                            |
                       [ ONT/MODEM ]
                            |
                    [ ROUTER/FIREWALL ]
                            |
                       802.1Q TRUNK
                            |
                     [ MANAGED SWITCH ]
                     /       |        \
                    /        |         \
               VLAN 20    VLAN 30    VLAN 40
                STAFF      GUEST      CCTV
                  |          |          |
              PCs/Printers  APs      PoE Cameras
                                        |
                                       NVR
```

## Notes

- VLAN 10 can be reserved for management.
- VLAN 20 can carry staff devices.
- VLAN 30 can provide isolated guest access.
- VLAN 40 can be dedicated to CCTV.
- Inter-VLAN access should be controlled by firewall rules.
- Access points can use a trunk/uplink when multiple SSIDs map to different VLANs.

This is a conceptual topology. Actual port modes, VLAN tagging, IP ranges, and firewall rules must match the hardware and deployment.

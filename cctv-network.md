# CCTV Network Design

IP cameras commonly use Ethernet and Power over Ethernet (PoE) to receive both network connectivity and power from a compatible switch.

## Example

```text
                 Router/Firewall
                       |
                 Managed Switch
                       |
                 PoE Switch
              _____|_____|_____
             |       |         |
          Camera  Camera     NVR
```

Depending on the deployment, cameras and NVRs may be placed on a dedicated CCTV VLAN.

## Basic checks when a camera is offline

1. Confirm the camera has power.
2. Check the PoE switch port.
3. Check Ethernet cabling.
4. Confirm the camera link LED if available.
5. Verify the camera IP address.
6. Check whether the camera and NVR are on compatible networks/VLANs.
7. Test connectivity from the appropriate management workstation.
8. Check NVR camera status and logs.
9. Review recent power outages or switch reboots.

## After a power outage

If cameras do not return automatically:

- Check PoE switch status.
- Check switch uplink.
- Check DHCP or static IP assignments.
- Check NVR network settings.
- Check camera PoE negotiation.
- Check for IP conflicts.

Do not publish customer camera addresses, passwords, screenshots containing credentials, or public-facing details in a public repository.

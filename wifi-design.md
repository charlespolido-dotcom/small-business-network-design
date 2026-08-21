# Wi-Fi Design

Good Wi-Fi is a combination of radio planning, placement, capacity, configuration, and wired backhaul.

## Planning checklist

- Identify the coverage area.
- Estimate the number of clients.
- Identify walls and sources of interference.
- Prefer wired Ethernet backhaul for access points when practical.
- Place APs based on coverage and capacity rather than simply maximizing transmit power.
- Use appropriate 2.4 GHz and 5 GHz settings for the environment.
- Create a separate guest SSID when guest access is required.
- Keep AP management traffic on an appropriate management network.

## Guest Wi-Fi

A guest network should normally:

- Receive internet access.
- Be isolated from internal business devices.
- Use a separate VLAN/subnet when supported.
- Use a reasonable bandwidth policy.

## Troubleshooting poor Wi-Fi

Check:

1. Signal strength.
2. Channel utilization/interference.
3. Client count.
4. AP placement.
5. Wired uplink speed.
6. DHCP availability.
7. DNS performance.
8. VLAN configuration.
9. Roaming behavior.

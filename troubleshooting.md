# Network Troubleshooting

Use a structured troubleshooting process instead of changing many settings at once.

## Layer 1 — Physical

Check:

- Power
- Patch cables
- Fiber connectors
- SFP modules
- Link LEDs
- PoE status
- Switch port state

## Layer 2 — Switching

Check:

- Correct switch port
- VLAN assignment
- Trunk configuration
- MAC address table
- STP events
- Port errors

## Layer 3 — IP

Check:

- IP address
- Subnet mask
- Default gateway
- DHCP lease
- Duplicate IPs
- DNS configuration

## Internet connectivity

Test in order:

```text
Client
  ↓
Default gateway
  ↓
Router
  ↓
Public IP connectivity
  ↓
DNS resolution
  ↓
Application/website
```

For example, successful connectivity to an IP address but failed domain resolution can indicate a DNS issue.

## Change management

Before a significant production change:

1. Export/backup the current configuration.
2. Record the planned change.
3. Identify rollback steps.
4. Make one logical change at a time.
5. Test.
6. Document the result.

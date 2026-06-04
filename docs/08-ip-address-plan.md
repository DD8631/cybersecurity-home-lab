# IP Address Plan

Last Updated: June 2026

## Purpose

This document defines the IP addressing standards used throughout the Home Network Project.

The addressing scheme is designed to:

- Simplify troubleshooting
- Support future expansion
- Align with VLAN assignments
- Improve documentation readability

---

# Addressing Standard

The third octet matches the VLAN ID.

Example:

| VLAN | Network |
|--------|----------|
| 10 | <internal-address-redacted> |
| 20 | <internal-address-redacted> |
| 30 | <internal-address-redacted>|
| 40 | <internal-address-redacted> |
| 50 | <internal-address-redacted> |
| 60 | <internal-address-redacted> |
| 70 | <internal-address-redacted> |

---

# VLAN Networks

| VLAN | Name | Network | Gateway |
|--------|--------|--------|--------|
| 10 | Management | <internal-address-redacted> | <internal-address-redacted> |
| 20 | Trusted-Wired | <internal-address-redacted>| <internal-address-redacted> |
| 30 | Trusted-Wireless | <internal-address-redacted> | <internal-address-redacted> |
| 40 | Services | <internal-address-redacted> | <internal-address-redacted> |
| 50 | Mullvad | <internal-address-redacted> | <internal-address-redacted> |
| 60 | IoT | <internal-address-redacted> | <internal-address-redacted> |
| 70 | Guest | <internal-address-redacted> | <internal-address-redacted> |

---

# Address Allocation Standard

## Infrastructure

Reserved:

<internal-address-redacted> – <internal-address-redacted>

Purpose:

- Switches
- Access Points
- Hypervisors
- Infrastructure Devices

---

## Servers and Services

Reserved:

<internal-address-redacted> – <internal-address-redacted>

Purpose:

- Pi-hole
- Grafana
- Home Assistant
- Future Services

---

## DHCP Pool

Reserved:

<internal-address-redacted> – <internal-address-redacted>

Purpose:

- Client Devices
- Wireless Clients
- Temporary Devices

---

## Static Devices

Reserved:

<internal-address-redacted> – <internal-address-redacted>

Purpose:

- Permanent devices requiring static assignments

---

# Management VLAN Assignments

## VLAN 10

| Device | Address |
|----------|----------|
| OPNsense | <internal-address-redacted> |
| MS308E | <internal-address-redacted> |
| EAP610 | <internal-address-redacted> |
| Proxmox | <internal-address-redacted> |

---

# Services VLAN Assignments

## VLAN 40

| Service | Address |
|----------|----------|
| Pi-hole | <internal-address-redacted> |
| Grafana | <internal-address-redacted> |
| Home Assistant | <internal-address-redacted> |

---

# Current Deployment Status

Current State:

- Flat LAN
- VLANs not yet implemented

Future State:

- VLAN-based addressing using this document as the authoritative source

---

# Change Log

## 2026-06

Initial addressing plan created.

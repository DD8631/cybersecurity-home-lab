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
| 10 | 192.168.10.0/24 |
| 20 | 192.168.20.0/24 |
| 30 | 192.168.30.0/24 |
| 40 | 192.168.40.0/24 |
| 50 | 192.168.50.0/24 |
| 60 | 192.168.60.0/24 |
| 70 | 192.168.70.0/24 |

---

# VLAN Networks

| VLAN | Name | Network | Gateway |
|--------|--------|--------|--------|
| 10 | Management | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Trusted-Wired | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Trusted-Wireless | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Services | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Mullvad | 192.168.50.0/24 | 192.168.50.1 |
| 60 | IoT | 192.168.60.0/24 | 192.168.60.1 |
| 70 | Guest | 192.168.70.0/24 | 192.168.70.1 |

---

# Address Allocation Standard

## Infrastructure

Reserved:

192.168.X.2 – 192.168.X.19

Purpose:

- Switches
- Access Points
- Hypervisors
- Infrastructure Devices

---

## Servers and Services

Reserved:

192.168.X.20 – 192.168.X.49

Purpose:

- Pi-hole
- Grafana
- Home Assistant
- Future Services

---

## DHCP Pool

Reserved:

192.168.X.50 – 192.168.X.199

Purpose:

- Client Devices
- Wireless Clients
- Temporary Devices

---

## Static Devices

Reserved:

192.168.X.200 – 192.168.X.254

Purpose:

- Permanent devices requiring static assignments

---

# Management VLAN Assignments

## VLAN 10

| Device | Address |
|----------|----------|
| OPNsense | 192.168.10.1 |
| MS308E | 192.168.10.2 |
| EAP610 | 192.168.10.3 |
| Proxmox | 192.168.10.4 |

---

# Services VLAN Assignments

## VLAN 40

| Service | Address |
|----------|----------|
| Pi-hole | 192.168.40.10 |
| Grafana | 192.168.40.20 |
| Home Assistant | 192.168.40.30 |

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

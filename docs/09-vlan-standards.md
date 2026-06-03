# VLAN Standards

Last Updated: June 2026

## Purpose

This document defines the VLAN standards used throughout the Home Network Project.

These VLANs provide network segmentation, improve security, and support future expansion.

---

# VLAN Design Principles

The VLAN architecture follows several core principles:

- Separate administrative systems from user devices
- Isolate guest devices from trusted resources
- Isolate IoT devices whenever possible
- Support VPN-specific routing policies
- Maintain a dedicated management network
- Minimize unnecessary inter-VLAN communication

---

# VLAN Assignments

| VLAN ID | Name | Purpose | Status |
|----------|----------|----------|----------|
| 10 | Management | Infrastructure management | Planned |
| 20 | Trusted-Wired | Administrative PCs and laptops | Planned |
| 30 | Trusted-Wireless | Trusted wireless devices | Planned |
| 40 | Services | Proxmox-hosted services | Planned |
| 50 | Mullvad | VPN-routed devices | Planned |
| 60 | IoT | Smart home devices | Planned |
| 70 | Guest | Guest internet access | Planned |

---

# VLAN 10 - Management

## Purpose

Dedicated management network for infrastructure devices.

## Intended Devices

- OPNsense Management
- MS308E Management
- EAP610 Management
- Proxmox Management

## Access Policy

Accessible only from trusted administrative devices.

---

# VLAN 20 - Trusted Wired

## Purpose

Administrative and primary computing devices.

## Intended Devices

- MacBook (when wired)
- ThinkPad E15
- Lenovo Yoga
- Future administrative systems

## Access Policy

Full access to management resources and internal services.

---

# VLAN 30 - Trusted Wireless

## Purpose

Trusted wireless devices.

## Intended Devices

- Phones
- Tablets
- Family wireless devices

## Access Policy

Access to internal services.

Limited access to management resources.

---

# VLAN 40 - Services

## Purpose

Internal infrastructure services.

## Intended Systems

- Pi-hole
- Grafana
- Home Assistant
- Future self-hosted services

## Access Policy

Accessible from trusted networks.

Not directly accessible from guest networks.

---

# VLAN 50 - Mullvad

## Purpose

Policy-based VPN routing.

## Intended Devices

- Streaming devices
- TVs
- Selected privacy-focused clients

## Access Policy

Outbound internet traffic routed through Mullvad VPN.

---

# VLAN 60 - IoT

## Purpose

Segmentation of smart devices.

## Intended Devices

- Smart home equipment
- Future IoT devices

## Access Policy

Internet access only.

Inter-VLAN communication restricted unless explicitly required.

---

# VLAN 70 - Guest

## Purpose

Visitor internet access.

## Intended Devices

- Guest phones
- Guest tablets
- Temporary devices

## Access Policy

Internet only.

No access to:

- Management VLAN
- Services VLAN
- Trusted VLANs

---

# Current Deployment Status

Current State:

- VLANs not yet deployed
- Single flat LAN currently in use

Next Steps:

1. Create VLAN interfaces in OPNsense
2. Configure VLANs on MS308E
3. Configure SSID-to-VLAN mapping on EAP610
4. Migrate clients to appropriate networks
5. Validate inter-VLAN firewall policies


# Network Design

Last Updated: June 2026

## Purpose

This document describes the logical architecture of the Home Network Project.

It serves as the authoritative reference for network topology, segmentation strategy, and service placement.

---

# Design Goals

- Security
- Segmentation
- Privacy
- Monitoring
- Reliability
- Expandability

---

# Physical Topology

Fiber ONT

↓

Protectli VP4650

↓

NETGEAR MS308E

↓

Connected Devices

- EAP610
- Patch Panel
- Proxmox Host
- Future Expansion

---

# Core Components

## Firewall

Protectli VP4650

Responsibilities:

- Routing
- Firewalling
- DHCP
- DNS
- VPN Services

---

## Switching

NETGEAR MS308E

Responsibilities:

- Layer 2 Switching
- VLAN Transport
- Infrastructure Connectivity

---

## Wireless

TP-Link Omada EAP610

Current Networks:

- Trusted
- Guest

Future:

- VLAN-aware SSID mapping

---

## Virtualization

Lenovo M700

Hypervisor:

- Proxmox VE

Current Services:

- Monitoring LXC

Future Services:

- Pi-hole
- Home Assistant

---

# Monitoring Architecture

Node Exporter

↓

Prometheus

↓

Grafana

↓

Dashboards

Monitoring LXC:

192.168.10.50

---

# Current Network Architecture

Current State:

Flat LAN

Characteristics:

- Single broadcast domain
- No VLAN separation
- Simplified deployment

---

# Future VLAN Architecture

| VLAN | Purpose |
|--------|----------|
| 10 | Management |
| 20 | Trusted Wired |
| 30 | Trusted Wireless |
| 40 | Services |
| 50 | Mullvad |
| 60 | IoT |
| 70 | Guest |

---

# VPN Architecture

## WireGuard

Purpose:

- Remote administration
- Remote dashboard access
- Secure travel connectivity

---

## Mullvad

Purpose:

- Policy-based routing
- Privacy-focused internet access
- Streaming devices

---

# DNS Architecture

Current:

- Unbound DNS

Future:

- Pi-hole
- Local DNS records
- DNS filtering

Fallback:

- OPNsense Unbound

---

# Security Model

Current:

- Stateful firewall
- Flat network

Future:

- VLAN segmentation
- Inter-VLAN firewall rules
- IoT isolation
- Guest isolation
- VPN segmentation

---

# Future Expansion

Planned:

- Pi-hole
- Home Assistant
- WireGuard
- Mullvad
- Enhanced monitoring

Potential:

- NAS
- Additional AP
- Additional Proxmox Nodes
- AI Cluster
- IDS/IPS


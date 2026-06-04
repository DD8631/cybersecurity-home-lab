# Decisions and Rationale

Last Updated: June 2026

## Purpose

This document records significant project decisions and the reasoning behind them.

The goal is to preserve context and prevent future confusion when revisiting design choices.

---

# Firewall Platform

## Decision

Protectli VP4650

## Alternatives Considered

- Protectli VP2420
- Protectli VP6630
- CWWK firewall appliances
- Firewalla Gold Plus

## Rationale

The VP4650 provided:

- Sufficient processing power
- Multiple network interfaces
- OPNsense compatibility
- Future VPN capability
- Long-term expandability

---

# Wireless Platform

## Decision

TP-Link Omada EAP610

## Alternatives Considered

- EERO Pro 6E

## Rationale

The EAP610 supports:

- VLAN-aware SSID mapping
- Enterprise-style segmentation
- Future multi-AP deployments

The EERO platform lacked the flexibility required for VLAN-based wireless design.

---

# VPN Provider

## Decision

Mullvad VPN

## Alternatives Considered

- ProtonVPN

## Rationale

Mullvad was selected as the long-term VPN provider for policy-based routing and privacy-focused internet access.

---

# DNS Architecture

## Decision

Unbound on OPNsense with future Pi-hole integration

## Rationale

This design provides:

- Local DNS resiliency
- DNS filtering
- Ad blocking
- Local host records

If Pi-hole becomes unavailable, OPNsense can continue providing DNS services.

---

# Monitoring Platform

## Decision

Prometheus + Grafana + Node Exporter

## Rationale

Provides:

- Open-source monitoring
- Historical metrics
- Dashboard visualization
- Future alerting capabilities

Monitoring was prioritized before additional services to establish operational visibility.

---

# Virtualization Platform

## Decision

Proxmox VE

## Rationale

Provides:

- LXC containers
- Virtual machines
- Backup capabilities
- Flexible service deployment

---

# VLAN Strategy

## Decision

Dedicated VLANs for management, trusted devices, services, VPN devices, IoT, and guests.

## Rationale

Supports:

- Segmentation
- Security
- Easier troubleshooting
- Future growth

---

# Documentation Philosophy

## Decision

Git repository as the authoritative source of documentation.

## Rationale

Provides:

- Version control
- Change tracking
- Disaster recovery documentation
- Learning journal

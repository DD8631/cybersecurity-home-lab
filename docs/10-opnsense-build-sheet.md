# OPNsense Build Sheet

Last Updated: June 2026

## Purpose

This document records the configuration of the Protectli VP4650 firewall appliance.

It serves as:

- Configuration reference
- Change tracking document
- Disaster recovery reference
- Rebuild guide

---

# Hardware

## Appliance

Protectli VP4650

### Specifications

| Component | Value |
|------------|------------|
| CPU | Intel Core i5 |
| Memory | 16GB DDR4 |
| NVMe | 256GB |
| SATA SSD | 480GB |

---

# Software

| Component | Value |
|------------|------------|
| Operating System | OPNsense |
| Status | Operational |

---

# WAN Configuration

## Interface

WAN

### Connection Type

DHCP

### Upstream Provider

Fiber ONT

### Status

Operational

---

# LAN Configuration

## Interface

LAN

### Status

Operational

### Notes

Currently operating as a flat network.

VLAN migration planned.

---

# DNS Configuration

## Resolver

Unbound DNS

### Status

Enabled

### Notes

Currently serving as primary DNS resolver.

Future state includes Pi-hole integration.

---

# DHCP

## Current State

Enabled

### Notes

Infrastructure devices currently use static addresses or DHCP reservations.

Exact assignments to be documented in:

08-ip-address-plan.md

---

# VPN Services

## WireGuard

Status: Not Configured

Purpose:

- Remote administration
- Secure remote access
- Dashboard access

---

## Mullvad VPN

Status: Not Configured

Purpose:

- Policy-based routing
- Streaming devices
- Privacy-focused clients

---

# VLAN Interfaces

## Current State

Not Implemented

---

## Planned VLANs

| VLAN | Name |
|--------|--------|
| 10 | Management |
| 20 | Trusted-Wired |
| 30 | Trusted-Wireless |
| 40 | Services |
| 50 | Mullvad |
| 60 | IoT |
| 70 | Guest |

---

# Firewall Policy

## Current State

Flat network.

---

## Future State

Default deny between VLANs.

Explicit allow rules only.

---

# Backup Procedure

## OPNsense Configuration Backup

Required after:

- VLAN changes
- VPN changes
- Firewall rule changes
- DNS changes

Backup Location:

To be documented.

---

# Change Log

## 2026-06

- OPNsense installed
- WAN operational
- LAN operational
- Unbound enabled

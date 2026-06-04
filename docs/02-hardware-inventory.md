# Hardware Inventory

Last Updated: June 2026

## Firewall Appliance

**Device:** Protectli VP4650  
**Role:** Primary firewall and router  
**Operating System:** OPNsense  
**Status:** Operational  

### Specifications

| Component | Specification |
|---|---|
| CPU | Intel Core i5 |
| Memory | 16GB DDR4 |
| Primary Storage | 256GB NVMe SSD |
| Secondary Storage | 480GB SATA SSD |

## Core Switch

**Device:** NETGEAR MS308E  
**Role:** Core access switch  
**Status:** Operational  
**Notes:** Firmware updated; web GUI accessible.

## Wireless Access Point

**Device:** TP-Link Omada EAP610  
**Part Number:** 015601040  
**Management Mode:** Standalone  
**Status:** Operational  

### Current SSIDs

- Trusted
- Guest

### Pending

- VLAN-aware SSID tagging

## Virtualization Host

**Device:** Lenovo ThinkCentre M700 Tiny  
**Role:** Proxmox virtualization host  
**Status:** Operational  

### Specifications

| Component | Specification |
|---|---|
| CPU | Intel Core i7-6700T |
| Cores / Threads | 4 Core / 8 Thread |
| Memory | 16GB DDR4 |
| OS Drive | 256GB SSD |
| Data Drive | 1TB SSD |
| Hypervisor | Proxmox VE |

## Rack and Power

| Component | Status |
|---|---|
| DeskPi RackMate T2 | Operational |
| Rack Fan Module | Operational |
| Rack PDU | Operational |
| CyberPower UPS | Operational |
### Current Services

#### Monitoring LXC

Role:

Centralized monitoring platform

Address:

192.168.10.50

Services:

- Prometheus
- Grafana
- Node Exporter

Status:

Operational

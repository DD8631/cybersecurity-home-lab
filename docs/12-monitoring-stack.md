# Monitoring Stack

Last Updated: June 2026

## Overview

The monitoring platform provides visibility into infrastructure health, performance, and future service availability.

The monitoring solution is currently hosted on a dedicated Monitoring LXC running on the Proxmox node.

---

# Monitoring LXC

## Address

192.168.10.50

## Role

Centralized monitoring platform.

## Services

- Prometheus
- Grafana
- Node Exporter

---

# Architecture

Node Exporter
↓
Prometheus
↓
Grafana
↓
Dashboards

---

# Prometheus

## Status

Operational

## Purpose

- Metrics collection
- Time-series database
- Historical monitoring

## URL

<internal-address-redacted>

## Validation

Verified operational.

Prometheus targets reporting successfully.

---

# Node Exporter

## Status

Operational

## Purpose

- CPU metrics
- Memory metrics
- Disk metrics
- Filesystem metrics
- Network metrics
- Host health monitoring

## URL

<internal-address-redacted>

## Validation

Metrics successfully scraped by Prometheus.

---

# Grafana

## Status

Operational

## Purpose

- Dashboard visualization
- Historical trend analysis
- Future alerting platform

## URL

<internal-address-redacted>

## Data Source

Prometheus

Status: Connected

---

# Dashboard Configuration

## Installed Dashboard

Node Exporter Full

Dashboard ID:

1860

Status:

Operational

---

## Visible Metrics

- CPU utilization
- Memory utilization
- Disk usage
- Disk I/O
- Network throughput
- System load
- Uptime
- Filesystem statistics

---

# Prometheus Targets

## Verified Targets

| Job | Status |
|------|------|
| prometheus | UP |
| node | UP |

All configured targets currently reporting healthy.

---

# Future Monitoring Goals

## Infrastructure

- Proxmox host metrics
- OPNsense firewall metrics
- Switch monitoring
- Access Point monitoring

## VPN Monitoring

- WireGuard statistics
- Mullvad VPN status
- Tunnel availability

## Alerting

- Email notifications
- Grafana mobile alerts

## Visualization

- Rack dashboard display
- Single-pane-of-glass monitoring

---

# Milestones

## Monitoring Phase A

Completed

- Prometheus deployed
- Node Exporter deployed
- Grafana deployed
- Dashboard imported
- Monitoring stack validated

## Monitoring Phase B

Planned

- Proxmox host monitoring
- OPNsense monitoring
- VPN monitoring
- Alerting

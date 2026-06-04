cat > docs/05-deployment-status.md <<'EOF'
# Deployment Status

Last Updated: June 2026

## Purpose

This document tracks deployment progress for the Home Network Project.

Status values:

- Planned
- In Progress
- Operational
- Deferred

---

# Phase 1 - Core Infrastructure

| Component | Status |
|------------|------------|
| Rack Assembly | Operational |
| Fan Module Installation | Operational |
| VP4650 Installation | Operational |
| OPNsense Installation | Operational |
| WAN Connectivity | Operational |
| LAN Connectivity | Operational |
| MS308E Deployment | Operational |
| EAP610 Deployment | Operational |
| Cable Labeling | Operational |
| Patch Panel Installation | Operational |
| UPS Deployment | Operational |

Phase Status:

✅ Complete

---

# Phase 2 - Core Network Services

| Component | Status |
|------------|------------|
| Unbound DNS | Operational |
| DHCP Services | Operational |
| Static Infrastructure Addressing | Operational |
| VLAN Design | Complete |
| VLAN Implementation | Planned |
| Inter-VLAN Firewall Rules | Planned |

Phase Status:

🟡 In Progress

---

# Phase 3 - Virtualization

| Component | Status |
|------------|------------|
| Proxmox Installation | Operational |
| Local Storage Configuration | Operational |
| Monitoring LXC Creation | Operational |

Phase Status:

🟡 In Progress

---

# Phase 4 - Monitoring

## Monitoring LXC

Address:

192.168.10.50

### Components

| Component | Status |
|------------|------------|
| Prometheus | Operational |
| Node Exporter | Operational |
| Grafana | Operational |
| Dashboard Import | Operational |
| Prometheus Targets Validation | Operational |

### Verified URLs

Prometheus:

http://192.168.10.50:9090

Grafana:

http://192.168.10.50:3000

Node Exporter:

http://192.168.10.50:9100/metrics

Phase Status:

✅ Monitoring Phase A Complete

---

# Phase 5 - VPN Services

| Component | Status |
|------------|------------|
| WireGuard | Planned |
| Mullvad VPN | Planned |
| Policy Routing | Planned |

Phase Status:

⚪ Not Started

---

# Phase 6 - Future Services

| Component | Status |
|------------|------------|
| Pi-hole | Planned |
| Home Assistant | Planned |
| Alerting | Planned |
| Rack Dashboard Display | Planned |

Phase Status:

⚪ Not Started

---

# Current Project Summary

Operational:

- OPNsense
- Unbound DNS
- MS308E
- EAP610
- Proxmox
- Prometheus
- Grafana
- Node Exporter

In Progress:

- Documentation
- Monitoring Expansion

Planned:

- VLAN Deployment
- WireGuard
- Mullvad
- Pi-hole
- Home Assistant
- Alerting

---

# Next Milestone

Implement VLANs on:

- OPNsense
- MS308E
- EAP610

Then migrate devices into their intended segmented networks.
EOF

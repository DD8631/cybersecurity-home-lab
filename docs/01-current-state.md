# Current State

Last Updated: June 2026

## Project Status

Core network infrastructure is operational.

The environment currently provides internet access through OPNsense while additional segmentation, VPN services, and monitoring capabilities are under development.

---

## Firewall

### Status

Operational

### Completed

- OPNsense installed
- WAN operational
- LAN operational
- Internet access operational
- Unbound DNS enabled

### Pending

- VLAN interfaces
- WireGuard
- Mullvad VPN routing
- Advanced firewall policy implementation

---

## Switching

### Status

Operational

### Completed

- Firmware updated
- Management interface accessible

### Pending

- VLAN implementation
- Port assignment documentation

---

## Wireless

### Status

Operational

### Completed

- EAP610 deployed
- Trusted SSID operational
- Guest SSID operational

### Pending

- VLAN-aware SSID mapping

---

## Virtualization

### Status

Operational

### Completed

- Proxmox VE installed
- Monitoring LXC deployed
- Prometheus deployed
- Grafana deployed
- Node Exporter deployed

### Pending

- Management network design
- Pi-hole
- Home Assistant

---

## Physical Infrastructure

### Completed

- Rack assembled
- Fan module installed
- Patch panel installed
- Cable labeling completed
- UPS deployed

---

## Next Milestone

Implement network segmentation through VLAN deployment and prepare infrastructure for:

- WireGuard remote access
- Mullvad VPN routing
- Pi-hole deployment
- Inter-VLAN firewall policy implementation

## Monitoring

### Status

Operational

### Completed

- Prometheus installed
- Node Exporter installed
- Grafana installed
- Dashboard imported and operational
- Prometheus targets verified healthy

### Monitoring Services

| Service | Status |
|----------|----------|
| Prometheus | Operational |
| Node Exporter | Operational |
| Grafana | Operational |

### Monitoring LXC

Address:

<internal-address-redacted>

### URLs

Prometheus:
<internal-address-redacted>

Grafana:
<internal-address-redacted>

Node Exporter:
<internal-address-redacted>

### Pending

- Proxmox host monitoring
- OPNsense monitoring
- VPN monitoring
- Alerting
- Rack dashboard display

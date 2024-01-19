# monitoring

The **monitoring** project provides **infrastructure monitoring and dashboards** for your lab.

It uses:

- **Prometheus** – time-series database and scraper for metrics.
- **Grafana** – dashboards and visualizations.
- Optional alerting via **Prometheus alerting rules**.

Typical use:

- Monitor Proxmox nodes, PBS, NAS, AI server, and other services.
- Watch CPU, RAM, disk, network, and service health.
- Build graphs for traffic, resource usage, and uptime.

---

## 1. High-Level Overview

```text
Proxmox / PBS / NAS / AI server / etc.
       ↑         ↑           ↑
   (exporters / HTTP metrics)
       ↓         ↓           ↓
   Prometheus (monitoring stack, scrapes metrics)
       ↓
   Grafana (dashboards for metrics + alerts)

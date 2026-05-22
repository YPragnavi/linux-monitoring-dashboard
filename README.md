# Linux Monitoring Dashboard using Grafana & Prometheus

A real-time Linux infrastructure monitoring project built using Prometheus, Grafana, and Node Exporter for monitoring system performance, resource utilization, and network activity.

---

# Project Overview

This project demonstrates how modern monitoring tools can be integrated to monitor Linux server health and visualize system metrics through interactive dashboards.

The setup continuously tracks:

- CPU Usage
- Memory Utilization
- Disk Usage
- Network Traffic
- System Uptime
- Linux Services Status

The project simulates a real-world infrastructure monitoring environment commonly used in DevOps, Cloud, and Cybersecurity operations.

---

# Technologies Used

- Ubuntu Server
- Prometheus
- Grafana
- Node Exporter
- VirtualBox

---

# Project Architecture

```text
Ubuntu Server
     ↓
Node Exporter
     ↓
Prometheus
     ↓
Grafana Dashboard
```

---

# Features

- Real-time Linux monitoring
- Interactive Grafana dashboards
- CPU, RAM, Disk, and Network visualization
- Prometheus metrics collection
- Alert rules configuration
- Infrastructure observability

---

# Installation Steps

## 1. Install Ubuntu Server

Create an Ubuntu Server virtual machine using VirtualBox.

---

## 2. Install Node Exporter

```bash
wget https://github.com/prometheus/node_exporter/releases/download/v1.8.1/node_exporter-1.8.1.linux-amd64.tar.gz
```

---

## 3. Install Prometheus

```bash
wget https://github.com/prometheus/prometheus/releases/download/v2.52.0/prometheus-2.52.0.linux-amd64.tar.gz
```

---

## 4. Install Grafana

```bash
sudo apt install grafana -y
```

---

## 5. Configure Prometheus

Edit:

```bash
prometheus.yml
```

Add Node Exporter target:

```yaml
scrape_configs:
  - job_name: 'node_exporter'

    static_configs:
      - targets: ['localhost:9100']
```

---

# Access URLs

| Service | URL |
|---|---|
| Grafana | http://localhost:3000 |
| Prometheus | http://localhost:9090 |
| Node Exporter | http://localhost:9100/metrics |

---

# Screenshots

## Ubuntu Terminal — Services Running

![Ubuntu Terminal](ubuntu_terminal-services_running.jpeg)

---

## Prometheus Targets Page

![Prometheus Targets](prometheus_target_page.jpeg)

---

## Node Exporter Metrics Page

![Node Exporter](node_exporter_page.jpeg)

---

## Grafana Dashboard

![Grafana Dashboard](grafana_dashboard.jpeg)

---

## Grafana Alert Rules Page

![Grafana Alerts](garafana_alert_rules_page.jpeg)

---

# Key Learnings

- Linux system administration
- Infrastructure monitoring
- Prometheus metrics collection
- Grafana dashboard creation
- Observability concepts
- Alert management

---

# Future Improvements

- Dockerize the setup
- Add Loki for log monitoring
- Configure Alertmanager
- Monitor multiple Linux servers
- Add cybersecurity-focused alerts

---

# Conclusion

This project successfully demonstrates a complete Linux monitoring environment using Grafana and Prometheus. It provides practical exposure to monitoring, observability, and infrastructure management concepts used in real-world environments.

---

# Author

**Pragnavi Yemireddy**

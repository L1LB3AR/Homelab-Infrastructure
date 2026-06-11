# 🏠 Homelab Infrastructure

Base setup for a self-hosted private cloud running on dedicated hardware.
This repository documents the full configuration of my home lab server —
from initial OS setup to monitoring and security hardening.

## 🖥️ Hardware

| Role | Device | Specs |
|---|---|---|
| Server | ASUS ROG Strix | Intel i7 · 16GB RAM · 256GB SSD + 1TB HDD |
| Workstation | ASUS Zenbook 16 | AMD Ryzen 9 · 32GB RAM |

## 🛠️ Stack

- **OS:** Ubuntu Server 24.04 LTS
- **Containers:** Docker + Portainer
- **Monitoring:** Prometheus + Grafana + Node Exporter
- **Security:** Fail2ban, UFW, SSH key authentication
- **Access:** SSH hardened, no password login, root disabled

## ✅ Roadmap

- [x] Ubuntu Server 24.04 installation — full 1TB disk
- [x] WiFi configuration with netplan
- [x] SSH hardening — ed25519 key-based auth
- [x] Disable password authentication
- [x] Disable root login
- [x] UFW firewall configuration
- [x] Fail2ban setup
- [x] Prometheus installation
- [x] Node Exporter installation
- [x] Grafana deployed as Docker container
- [x] Live monitoring dashboard — CPU, RAM, disk, network
- [x] Docker installed and configured
- [x] Portainer deployed — web UI for container management
- [ ] Docker Compose workflows
- [ ] Automated backups
- [ ] Alert rules in Grafana
- [ ] Static IP configuration

## 🔐 Security Hardening

SSH configured with ed25519 key pair. Password authentication
and root login disabled. UFW allows only necessary ports.
Fail2ban monitors and blocks brute force attempts automatically.

## 📊 Monitoring Stack

- **Prometheus** → collects metrics on port 9090
- **Node Exporter** → exposes system metrics on port 9100
- **Grafana** → visualizes metrics on port 3000 using dashboard ID 1860

## 📐 Architecture

```
ASUS Zenbook 16 (Workstation)
        ↓ SSH / Browser
ASUS ROG Strix (Ubuntu Server 24.04)
        ├── Prometheus :9090
        ├── Node Exporter :9100
        ├── Grafana (Docker) :3000
        └── Portainer (Docker) :9000
```

## 📚 Key Commands

```bash
# Check SSH service
sudo systemctl status sshd

# Check Fail2ban
sudo systemctl status fail2ban

# Check firewall rules
sudo ufw status

# Check Prometheus
sudo systemctl status prometheus

# Check Grafana
sudo systemctl status grafana-server

# Check running containers
docker ps
```

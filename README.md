# 🏠 Homelab Infrastructure

Base setup for a self-hosted private cloud running on dedicated hardware.
This repository documents the full configuration of my home lab server —
from initial OS setup to monitoring and security hardening.

## 🖥️ Hardware

| Role | Device | Specs |
|---|---|---|
| Server | ASUS ROG Strix | Intel i7 · 16GB RAM · 256GB SSD + 1TB HDD |
| Workstation | ASUS Professional | AMD Ryzen 9 · 32GB RAM |

## 🛠️ Stack

- **OS:** Ubuntu Server 24.04 LTS
- **Monitoring:** Prometheus + Grafana
- **Security:** Fail2ban, UFW, SSH key authentication
- **Access:** SSH hardened, no password login

## ✅ Roadmap

- [ ] Ubuntu Server 24.04 installation
- [ ] SSH hardening — key-based auth, disable root login
- [ ] UFW firewall configuration
- [ ] Fail2ban setup
- [ ] Prometheus installation
- [ ] Grafana dashboard setup
- [ ] System metrics monitoring (CPU, RAM, disk, temperature)

## 📐 Architecture

*Diagram coming soon*

## 📚 Documentation

Each step is documented as it is completed.
Configurations and scripts are included in this repository.

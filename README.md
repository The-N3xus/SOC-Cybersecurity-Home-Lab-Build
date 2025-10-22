# SOC-Cybersecurity-Home-Lab-Build
This repository documents the design, build, and management of a self-contained home lab environment dedicated to advanced cybersecurity practice.

## Goals
- Build practical SOC Analyt Skills
- Learn security tools (SIEM,IDS, automation)
- Practice networking concepts
- Prepare for security certifications

## Hardware
- All-in-one PC (Main workstation)
- Old Macbook (analysis Station)
- 4GB RAM PC (Server)

## Lab Architecture Overview

```
Internet
    ↓
Router
    ↓
┌─────────────────────────────────────┐
│         Home Network                │
├─────────────────────────────────────┤
│                                     │
│  [4GB PC]                          │
│  - Pi-hole (DNS/Ad-blocking)       │
│  - Wazuh Agent                     │
│  - Docker (lightweight containers) │
│  - n8n for automation              │
│                                     │
│  [All-in-One PC]                   │
│  - VirtualBox/VMware               │
│  - Security Onion / Wazuh Manager  │
│  - Kali Linux VM                   │
│  - Vulnerable VMs (Metasploitable) │
│  - SIEM Dashboard                  │
│                                     │
│  [MacBook]                         │
│  - Monitoring Dashboard            │
│  - Splunk/ELK Stack                │
│  - Documentation workspace         │
│  - Backup analysis station         │
└─────────────────────────────────────┘
```

---


# Phase 1: Network Services Hub (Date: 10/21/2025)

### Hardware Used:
- 4GB RAM PC (Ubuntu Server 24.04 LTS)

### What I Installed:
- Ubuntu Server 24.04 LTS
- Docker version: 28.2.2
- N8N
- Wazuh Agent: v-4.9.2

### IP Addresses:
- 4GB PC: 192.168.0.179

### What I learned:
- How to install Ubuntu Server
- Basic Linux Commands (apt, docker, ip addr)
- Why Docker is important for security tasks
- When setting up servers there is a difference in commands when connecting to the internet using ethernet or WIFI

# Phase 2: Main Workstation (Date: 10/22/2025)

### Hardware Used:
- All-in-one PC (Windows 11, 8GB RAM, Ryzen 5 5500U)

### What I installed:
- VirtualBox Version: 7.2.4
- Wazuh v.4.9.2.ova
- Kali-linux-2025.3

### IP Addresses:
- All-in-one PC: 192.168.0.184
- Wazuh Manager: 192.168.0.119
- Kali-linux VM: 192.168.0.192.195

### What I learned:
- 



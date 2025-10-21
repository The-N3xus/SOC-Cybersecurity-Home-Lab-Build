# SOC-Cybersecurity-Home-Lab-Build
This repository documents the design, build, and management of a self-contained home lab environment dedicated to advanced cybersecurity practice.
## Day 1: Foundation Setup (Date: 10/21/2025)
### Prepare Network Services Hub
# Hardware Used:
- 4GB RAM PC (Ubuntu Server 24.04 LTS)
# What I Installed:
- Ubuntu Server 24.04 LTS
- Docker version: 28.2.2
# IP Addresses:
- 4GB PC: 192.168.0.179
# Challenges Faced:
- This PC didn't have an Ethernet port so I had to use WIFI and so the interface that I needed to use changed from "enp3s0" to "wl01" but I hadn't taken that into account so that proved to be a bit of an issue down the line
# What I learned:
- how to install Ubuntu Server
- Basic Linux Commands (apt, docker, ip addr)
- Why Docker is important for security tasks
- When setting up servers there is a difference in commands when connecting to the internet using ethernet or WIFI

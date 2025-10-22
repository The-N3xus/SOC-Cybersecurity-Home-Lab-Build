# Project 1: Pi-hole Network-Wide Ad Blocking
Completion Date:** [10/21/2025]  
**Status:** ✅ Active and Running

## Objective
Deploy a network-level DNS sinkhole to block advertisements and trackers across all devices on my home network while gaining hands-on experience with DNS, Linux server administration, and network security monitoring.

## Skills Demonstrated
- Linux server administration (Ubuntu Server 22.04)
- DNS protocol understanding
- Docker containerization
- Network configuration
- Router administration
- Security logging and monitoring

## Architecture

### Hardware
- **Host:** 4GB RAM PC running Ubuntu Server 22.04 LTS
- **IP Address:** [192.168.0.150]
- **Network Role:** Primary DNS server for home network

### Network Topology
```
Internet
    ↓
Router (DNS configured to Pi-hole IP)
    ↓
Pi-hole (4GB PC) - DNS filtering and logging
    ↓
Home Devices (laptops, phones, tablets, IoT)
```

## Implementation Steps

### 1. System Preparation
```bash
# Updated Ubuntu Server
sudo apt update && sudo apt upgrade -y
```

### 2. Pi-hole Installation
```bash
# One-line installation
curl -sSL https://install.pi-hole.net | bash
```

**Installation Choices Made:**
- Upstream DNS Provider: [Which did you choose? Google/Cloudflare/etc]
- Interface: [wlo1]
- IP Protocol: IPv4
- Web Interface: Enabled
- Logging: Enabled

### 3. Router Configuration
- **Router Model:** [Your router model/brand]
- **Changed:** Primary DNS to Pi-hole IP
- **Result:** All network devices now route DNS through Pi-hole

## Results

[INSERT SCREENSHOT: Pi-hole dashboard showing statistics]

### Statistics (After 24 hours)
- **Total Queries:** [Check your dashboard]
- **Queries Blocked:** [Number]
- **Percentage Blocked:** [%]
- **Active Blocklists:** [Number - usually ~1-2 default]

### Top Blocked Domains
[Screenshot or list top 5-10 blocked domains]

### Security Insights
**Interesting findings from logs:**
- [Example: Discovered smart TV attempting to contact tracking domains]
- [Example: Mobile apps generating excessive ad requests]
- [Note any suspicious domains or patterns]

## Security Value

### From a SOC Perspective:
1. **DNS Visibility:** Can now monitor all DNS requests across network
2. **Threat Intelligence:** Pi-hole blocklists contain known malicious domains
3. **Baseline Establishment:** Understanding normal DNS patterns helps detect anomalies
4. **Log Aggregation:** DNS logs will feed into Wazuh SIEM (next phase)

### Real-World Applications:
- Detecting DNS tunneling attempts
- Identifying compromised devices (C2 callbacks)
- Tracking data exfiltration attempts
- Spotting unusual domain queries (DGA malware)

## Challenges & Solutions

### Challenge 1: [Any issues you encountered?]
**Solution:** [How you fixed it]

### Challenge 2: [Network devices not using Pi-hole]
**Solution:** Verified router DNS settings and rebooted router

## Future Enhancements

- [ ] Add additional blocklists (malware domains, tracking)
- [ ] Configure DHCP on Pi-hole for better control
- [ ] Set up Pi-hole as recursive DNS with Unbound
- [ ] Forward logs to Wazuh SIEM for analysis
- [ ] Create custom blocklists for threat intelligence
- [ ] Set up Pi-hole failover/redundancy

## Lessons Learned

1. **DNS is critical infrastructure:** Everything depends on it
2. **Network-level blocking is powerful:** No per-device configuration needed
3. **Visibility matters:** Seeing DNS requests reveals device behavior
4. **Logging is essential:** Will use these logs for security analysis

## References
- [Pi-hole Official Documentation](https://docs.pi-hole.net/)
- [Pi-hole GitHub Repository](https://github.com/pi-hole/pi-hole)
- DNS Security Best Practices: [Any articles you referenced]

## Next Steps
→ Deploy n8n automation platform  
→ Set up Wazuh SIEM for log aggregation  
→ Integrate Pi-hole logs with SIEM for analysis

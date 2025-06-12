# 📡 Analyzing syslog for Port Scanning Activity

## What Was Done

Simulated a port scan using Nmap and analyzed `/var/log/syslog` for unusual activity, such as connections to multiple ports in rapid succession.

## Why It Matters

Port scans are a common reconnaissance tactic used by attackers to discover services and vulnerabilities. Identifying scans helps organizations take proactive steps to protect exposed services.

## Commands Used

To simulate a scan:

```bash
To simulate a scan:
nmap -sS -T4 -p 1-1000 localhost

To search syslog:
grep -i "scan" /var/log/syslog

To identify suspicious traffic:
grep "DPT=" /var/log/syslog



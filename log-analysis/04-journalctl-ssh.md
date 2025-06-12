# 🧾 Using journalctl for SSH Log Analysis

## What Was Done

Used `journalctl` to query systemd-managed logs for SSH-related authentication attempts.

## Why It Matters

`journalctl` provides a powerful way to access logs on systems using `systemd`. It enables querying specific services or time ranges, useful in incident response and forensic analysis.

## Commands Used

```bash
Query SSH service logs:
journalctl -u ssh.service

Filter for failed logins:
journalctl -u ssh.service | grep "Failed password"

Query by time
journalctl -u ssh.service --since "1 hour ago"

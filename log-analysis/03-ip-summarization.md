# 🧮 Summarizing Suspicious IP Addresses

## What Was Done

Extracted IP addresses from log files and used text processing tools to count and rank them by frequency of failed access attempts.

## Why It Matters

High-frequency failed attempts from an IP indicate potential brute-force or scanning behavior. Summarizing IPs helps in blocking malicious sources or feeding into tools like Fail2Ban.

## Commands Used

```bash
From auth.log:

grep "Failed password" /var/log/auth.log | awk '{print $(NF-3)}' | sort | uniq -c | sort -nr

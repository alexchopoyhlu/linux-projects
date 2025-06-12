# 🔐 Inspecting auth.log for Failed SSH Logins

## What Was Done

Simulated multiple failed SSH login attempts using incorrect credentials and inspected the `/var/log/auth.log` file to identify suspicious activity.

## Why It Matters

Brute-force attacks are a common method used by attackers to gain unauthorized access. Detecting repeated failed logins from the same IP can help identify these attacks early.

## Commands Used

```bash
grep "Failed password" /var/log/auth.log

To extract and count offending IPs:
grep "Failed password" /var/log/auth.log | awk '{print $(NF-3)}' | sort | uniq -c | sort -nr

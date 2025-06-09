# 🚫 Install and Configure Fail2Ban

## What Was Done

Installed Fail2Ban to protect SSH by banning IPs after multiple failed login attempts.

## Why It Matters

Fail2Ban reduces brute-force attacks by automatically banning suspicious IPs temporarily, limiting the chance of unauthorized access.

## Commands Used

Install Fail2Ban:

```bash
sudo apt install fail2ban -y
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local 
sudo nano /etc/fail2ban/jail.local

# Ensure [sshd] section looks like the following:

[sshd]
enabled = true
port = ssh
logpath = %(sshd_log)s
backend = %(sshd_backend)s
maxretry = 5
findtime = 10m
bantime = 1h

sudo systemctl restart fail2ban
sudo fail2ban-client status sshd

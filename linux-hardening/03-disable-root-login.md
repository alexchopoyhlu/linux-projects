# 🔒 Disable Root Login via SSH

## What Was Done

Disabled remote SSH login directly as the root user by editing the SSH daemon configuration.

## Why It Matters

Direct root login increases risk by allowing attackers to target the most powerful account directly. Disabling it enforces the use of a regular user with `sudo`, improving security and accountability.

## Commands Used

```bash
sudo nano /etc/ssh/sshd_config

# Change
PermitRootLogin yes
# Into
PermitRootLogin no

sudo systemctl restart ssh

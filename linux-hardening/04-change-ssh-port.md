# 🔧 Change Default SSH Port

## What Was Done

Changed the SSH port from default 22 to a custom port to reduce automated attacks.

## Why It Matters

Port 22 is widely scanned and targeted by bots and brute force attacks. Changing the port helps reduce this noise and lowers attack surface.

## Commands Used

```bash
sudo nano /etc/ssh/sshd_config

# Change
Port 22
# Into
Port (desired port)

sudo ufw allow (desired port)/tcp
sudo systemctl restart ssh

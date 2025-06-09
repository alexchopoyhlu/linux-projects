# 🔒 Disable Root Login Over SSH

## What Was Done

Modified the SSH daemon config to block direct root login.

## Why It Matters

Root access gives full control over a system. Allowing direct root login — especially over SSH — is dangerous. Disabling it forces users to log in with a regular account and use `sudo` for privileged actions, improving security and accountability.

## ⚙Commands Used

```bash
sudo nano /etc/ssh/sshd_config

Changed
# PermitRootLogin prohibit-password
into
# PermitRootLogin no

sudo systemctl restart ssh

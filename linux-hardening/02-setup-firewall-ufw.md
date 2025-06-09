# 🔥 Set Up a Firewall (UFW)

## What Was Done

Configured UFW (Uncomplicated Firewall) to allow only necessary incoming connections and block all others.

## Why It Matters

A firewall controls incoming and outgoing network traffic, reducing exposure to unauthorized access and attacks.

## Commands Used

```bash
sudo ufw enable
sudo ufw allow ssh
sudo ufw status verbose

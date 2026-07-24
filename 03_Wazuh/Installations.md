# Wazuh SIEM Installation

## Objective

Deploy an All-in-One Wazuh SIEM server on Ubuntu 24.04 LTS running inside Oracle VirtualBox and connect a Windows 11 endpoint as the first monitored agent.

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Host OS | Windows 11 |
| Hypervisor | Oracle VirtualBox |
| SIEM Server | Ubuntu 24.04 LTS |
| SIEM Platform | Wazuh 4.14.6 |
| Endpoint | Windows 11 |
| Network Mode | Bridged Adapter |

---

# Architecture

```

Windows 11
(Wazuh Agent)
│
│
▼

Ubuntu 24.04 VM
(Wazuh Manager
+ Indexer
+ Dashboard)

```

---

# Installation Steps

## 1. Ubuntu Preparation

Update packages

```bash
sudo apt update
sudo apt upgrade
```

---

## 2. Download Installer

```bash
curl -sO https://packages.wazuh.com/4.14/wazuh-install.sh
```

---

## 3. Start Installation

```bash
sudo bash wazuh-install.sh -a
```

The installer automatically deployed

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Filebeat

---

# Installation Issues

During installation the deployment failed while installing Filebeat because Ubuntu automatic updates locked the APT package manager.

Observed error:

```

Another process is using APT.
Waiting for it to release the lock.

```

---

# Troubleshooting

Verified running processes

```bash
ps -ef | grep -E "apt|dpkg|unattended"
```

Stopped unattended upgrades

```bash
sudo systemctl stop unattended-upgrades
```

Stopped APT services

```bash
sudo systemctl stop apt-daily.service
sudo systemctl stop apt-daily-upgrade.service
```

Killed remaining processes

```bash
sudo pkill -f unattended-upgrade
sudo pkill -f apt.systemd.daily
```

Repaired package manager

```bash
sudo dpkg --configure -a
```

Updated package index

```bash
sudo apt update
```

Restarted installation

```bash
sudo bash wazuh-install.sh -a -o
```

Installation completed successfully.

---

# Service Verification

Verified all major Wazuh services.

Manager

```bash
sudo systemctl status wazuh-manager
```

Indexer

```bash
sudo systemctl status wazuh-indexer
```

Dashboard

```bash
sudo systemctl status wazuh-dashboard
```

Filebeat

```bash
sudo systemctl status filebeat
```

---

# Network Configuration

Initially VirtualBox used NAT networking.

Changed Adapter 1 to

```

Bridged Adapter

```

Verified server IP

```bash
hostname -I
```

Server IP

```

10.157.129.127

```

---

# Dashboard Access

Opened Wazuh dashboard

```

https://localhost

```

Retrieved admin credentials from

```bash
sudo tar -O -xvf wazuh-install-files.tar wazuh-install-files/wazuh-passwords.txt
```

---

# Windows Agent Deployment

Used the Deploy New Agent wizard.

Configuration

| Setting | Value |
|----------|-------|
| Operating System | Windows |
| Architecture | x64 |
| Manager Address | 10.157.129.127 |

Started service

```cmd
NET START WazuhSvc
```

Verified successful connection.

---

# Final Result

Successfully deployed

- Ubuntu Wazuh Server
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Filebeat
- Windows 11 Agent

Dashboard Status

```

1 Active Endpoint

```

---

# Screenshots

> Insert screenshots sequentially

1. Ubuntu Installation
2. APT Lock Error
3. Troubleshooting
4. Successful Installation
5. Dashboard Login
6. Agent Deployment
7. Active Windows Endpoint


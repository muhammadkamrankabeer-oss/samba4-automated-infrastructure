![Banner](docs/screenshots/banner.png)

# 🚀 Samba4 Enterprise Identity Suite

> Enterprise-grade Samba4 Active Directory infrastructure automated with Ansible, Linux hardening, monitoring, and Infrastructure as Code.

![Samba4](https://img.shields.io/badge/Samba4-AD--DC-orange?style=for-the-badge)
![Ansible](https://img.shields.io/badge/Ansible-Automation-red?style=for-the-badge)
![Debian](https://img.shields.io/badge/Debian-12-A81D33?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-Enterprise-yellow?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production--Style-success?style=for-the-badge)

---

## 📌 Overview

This project automates the deployment of a production-style centralized Identity & Access Management (IAM) environment using Samba4 Active Directory Domain Services on Linux.

The infrastructure is designed as an open-source alternative to traditional Windows Active Directory environments for:

- Educational Labs
- Offices & SMEs
- Linux-based infrastructure environments
- Training centers
- DevOps learning labs

Using Infrastructure as Code (IaC) principles, the platform provisions:

- Samba4 Active Directory Domain Controller
- Linux client integration
- Automated domain joining
- Infrastructure hardening
- Monitoring & administration tools
- Shared storage environments

---

## ⚙️ Technology Stack

| Technology | Purpose |
|---|---|
| Samba4 | Active Directory Domain Controller |
| Ansible | Automation & Configuration Management |
| Debian 12 | Linux Server Operating System |
| Vagrant | Infrastructure Virtualization |
| VirtualBox | Local Infrastructure Lab |
| Cockpit | Monitoring & Web Administration |
| SSSD / Realmd | Linux Domain Authentication |
| Bash | Automation & Scripting |

---

## 🏗️ Enterprise Architecture

### Infrastructure Components

| Component | Purpose |
|---|---|
| DC1 | Samba4 Active Directory Domain Controller |
| Linux Clients | Domain Joined Workstations |
| DNS & Kerberos | Centralized Authentication |
| Ansible Control Node | Infrastructure Automation |
| Cockpit | Monitoring & Management |

### Infrastructure Flow

```
Host Machine (Xubuntu)
        │
        ├── Ansible Control Node
        │
        ├── Vagrant Infrastructure
        │
        ├── Samba4 Domain Controller
        │
        ├── Linux Domain Clients
        │
        └── Monitoring & Administration
```

---

## 📂 Project Structure

```
samba4-enterprise-identity-suite/
├── ansible/
│   ├── inventories/
│   ├── playbooks/
│   ├── roles/
│   ├── group_vars/
│   └── host_vars/
├── backups/
├── docs/
│   ├── architecture/
│   ├── screenshots/
│   └── troubleshooting/
├── monitoring/
├── terraform/
├── scripts/
├── README.md
├── Vagrantfile
└── ssh_config
```

---

## 🎯 Business Outcomes

This project demonstrates how open-source technologies can provide enterprise identity and access management capabilities traditionally associated with commercial Active Directory environments.

Key outcomes include:

* Centralized identity management for Linux systems
* Automated Active Directory deployment using Infrastructure as Code
* Kerberos-based secure authentication
* Automated Linux domain joining and account management
* Reduced manual administration through Ansible automation
* Monitoring and operational visibility using Cockpit
* Repeatable and idempotent infrastructure deployment
---
## 🛠 Challenges Solved

### Challenge

Managing user accounts individually across Linux systems creates operational overhead, inconsistent access controls, and increased security risks.

### Solution

This platform centralizes authentication and identity management using Samba4 Active Directory while automating deployment and configuration through Ansible.

### Benefits

* Single source of truth for user identities
* Consistent authentication across systems
* Reduced manual configuration effort
* Improved operational efficiency
* Repeatable deployments using Infrastructure as Code
---

## 📈 Project Metrics

| Metric                    | Value                   |
| ------------------------- | ----------------------- |
| Ansible Playbooks         | 10                      |
| Ansible Roles             | 5                       |
| Domain Controllers        | 1                       |
| Linux Clients             | Multiple                |
| Authentication Method     | Kerberos                |
| Identity Platform         | Samba4 Active Directory |
| Monitoring Solution       | Cockpit                 |
| Infrastructure Automation | Ansible                 |
| Deployment Platform       | Vagrant                 |

---
## 🚀 Core Features

| Feature | Description |
|---|---|
| ⚡ Infrastructure Automation | Automated deployment using Ansible |
| 🔐 Centralized Authentication | Samba4 Active Directory Domain |
| 🖥️ Linux Domain Join | Automated Linux client integration |
| 📁 Shared Storage | Centralized SMB shares |
| 🛡️ Security Hardening | SSH hardening, firewall, secure authentication |
| 📊 Monitoring | Cockpit monitoring dashboard |
| 🔄 Idempotent Playbooks | Safe repeatable deployments |
| 🧠 Infrastructure as Code | Reproducible environments |

---

## 🏢 Enterprise Use Cases

This platform can be adapted for:

- Educational Labs & Campuses
- Small & Medium Businesses (SMEs)
- Linux-based Office Infrastructure
- Open-source Active Directory Environments
- Centralized Authentication Systems
- Hybrid Linux Infrastructure Labs
- IT Training Environments
- Automated Infrastructure Demonstrations

---

## 🚀 Quick Start

### 1. Clone Repository

```bash
git clone https://github.com/muhammadkamrankabeer-oss/samba4-enterprise-identity-suite.git
cd samba4-enterprise-identity-suite
```

### 2. Start Infrastructure

```bash
vagrant up
```

### 3. Run Infrastructure Automation

```bash
ansible-playbook -i ansible/inventories/lab/hosts.ini ansible/playbooks/provision_dc.yml

ansible-playbook -i ansible/inventories/lab/hosts.ini ansible/playbooks/join_and_secure.yml
```

---

## 📸 Screenshots

### 🖥️ Vagrant Infrastructure

**Vagrant Status**

![Vagrant Status](docs/screenshots/vagrant-status.png)

**Vagrant Up**

![Vagrant Up](docs/screenshots/vagrant-up.png)

---

### ⚙️ Ansible Automation

**Ansible Ping Success**

![Ansible Ping Success](docs/screenshots/ansible-ping-success.png)

**Provision DC Success**

![Provision DC Success](docs/screenshots/provision-dc-success.png)

**Idempotent Playbook Run**

![Idempotent Playbook](docs/screenshots/idempotent-playbook.png)

**Cockpit Playbook Execution**

![Cockpit Playbook](docs/screenshots/cockpit-playbook.png)

---

### 🏢 Domain Controller

**Samba Service Running**

![Samba Service Running](docs/screenshots/samba-service-running.png)

**Domain Level Check**

![Domain Level Check](docs/screenshots/domain-level-check.png)

**Domain Info, User List & Kerberos Ticket**

![Domain Info, User List & klist](docs/screenshots/domain-info_userlist_klist.png)

---

### 🖥️ Linux Domain Join

**Domain Joining Process**

![Domain Joining](docs/screenshots/domainjoining.png)

**Linux Domain Join Success**

![Linux Domain Join Success](docs/screenshots/linux-domain-join-success.png)

**SSSD Service Running**

![SSSD Service Running](docs/screenshots/sssd-service-running.png)

---

### 🔐 Authentication

**Domain Login Success**

![Domain Login Success](docs/screenshots/domain-login-success.png)

**Domain User Authentication**

![Domain User Authentication](docs/screenshots/domain-user-authentication.png)

---

### 📊 Monitoring

**Cockpit Enterprise Dashboard**

![Cockpit Dashboard](docs/screenshots/cockpit-dashboard-enterprise.png)

---

## 🧩 Main Playbooks

| Playbook | Purpose |
|---|---|
| `provision_dc.yml` | Deploy Samba4 Domain Controller |
| `prepare_dc.yml` | Prepare Domain Controller environment |
| `join_and_secure.yml` | Join Linux clients to domain |
| `join_linux_client.yml` | Linux client domain join |
| `setup_monitoring.yml` | Deploy Cockpit monitoring |
| `setup_shares.yml` | Configure shared folders |
| `setup_home_folders.yml` | Configure user home directories |
| `setup_dns_forwarding.yml` | Configure DNS forwarding |
| `deploy_students.yml` | Deploy student user accounts |
| `backup_ad.yml` | Backup Active Directory environment |

---

## 🔍 Validation Commands

### Verify Kerberos Authentication

```bash
kinit administrator
klist
```

### Verify Domain Membership

```bash
realm list
```

### List Samba Users

```bash
sudo samba-tool user list
```

---

## 🔐 Security Features

- SSH hardening
- Linux firewall configuration
- Kerberos-secured authentication
- Centralized user access control
- Infrastructure isolation using Vagrant

---

## 🧠 Skills Demonstrated

- Linux System Administration
- Infrastructure Automation
- Configuration Management
- Identity & Access Management (IAM)
- Infrastructure as Code (IaC)
- Ansible Automation
- Enterprise Networking
- DNS & Kerberos
- Monitoring & Observability
- Virtualization
- Security Hardening
- Troubleshooting & Operations

---

## 🧠 Future Improvements

- [ ] Automated daily backups
- [ ] Prometheus + Grafana monitoring
- [ ] Terraform-based cloud deployment
- [ ] Role-based access control
- [ ] CI/CD pipeline validation
- [ ] Automated infrastructure testing
- [ ] Multi-site Samba replication
- [ ] AWS deployment architecture

---

## 👨‍💻 Author

**Muhammad Kamran Kabeer**
DevOps Engineer focused on Linux infrastructure, automation, cloud engineering, and Infrastructure as Code.

🌐 Website: [https://www.devriston.com.pk](https://www.devriston.com.pk)
💼 LinkedIn: [https://www.linkedin.com/in/kamrankabeer/](https://www.linkedin.com/in/kamrankabeer/)
🐙 GitHub: [https://github.com/muhammadkamrankabeer-oss](https://github.com/muhammadkamrankabeer-oss)

---

## ⭐ Support

If you found this project useful, consider giving it a star ⭐

This helps others discover the project and supports open-source learning.

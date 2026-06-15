# Samba4 Enterprise Identity Suite Architecture

## Overview

This project implements a centralized Identity and Access Management (IAM) platform using Samba4 Active Directory Domain Services.

The environment is automated with Ansible and deployed within a Vagrant-based lab environment.

## Components

### Ansible Control Node

Responsible for:

* Infrastructure automation
* Playbook execution
* Configuration management
* Domain provisioning

### Samba4 Domain Controller

Provides:

* Active Directory services
* DNS services
* Kerberos authentication
* User and group management

### Linux Clients

Domain-joined Linux systems using:

* SSSD
* Realmd
* Kerberos

These clients authenticate directly against Active Directory.

### Cockpit Monitoring

Provides:

* System monitoring
* Service management
* Administrative dashboard

## Authentication Flow

1. User enters credentials on Linux client.
2. SSSD forwards authentication request.
3. Kerberos validates credentials against Samba4 AD.
4. Ticket Granting Ticket (TGT) is issued.
5. User receives authenticated session.

## Automation Workflow

1. Vagrant provisions infrastructure.
2. Ansible prepares domain controller.
3. Samba4 domain is configured.
4. Linux clients join the domain.
5. Monitoring services are deployed.
6. Validation commands verify authentication.

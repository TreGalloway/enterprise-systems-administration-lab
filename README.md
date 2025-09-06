# Enterprise Systems Administration Lab

> **Comprehensive systems administration project demonstrating Windows/Linux enterprise management, network administration, and operational automation skills.**

[![Project Status](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)](https://github.com/yourusername/enterprise-sysadmin-lab)
[![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-blue.svg)](https://www.microsoft.com/windows-server)
[![Linux](https://img.shields.io/badge/Linux-Ubuntu%2022.04-orange.svg)](https://ubuntu.com)
[![Network+](https://img.shields.io/badge/CompTIA-Network%2B-green.svg)](https://www.comptia.org/certifications/network)
[![AWS](https://img.shields.io/badge/AWS-Cloud%20Practitioner-orange.svg)](https://aws.amazon.com/certification/certified-cloud-practitioner)

---

## 🎯 Project Overview

**Goal**: Build a production-ready enterprise environment demonstrating core systems administration competencies required for modern IT operations.

**Target Role**: Systems Administrator  
**Timeline**: 8 weeks  
**Platform**: Proxmox VE hypervisor environment

## 🏗️ Architecture Diagram

 ┌─────────────────────────────────────────────────────────────┐
│                    Proxmox VE Host                          │
│                                                             │
│  Management VLAN (10.0.1.0/24)                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │ pfSense     │  │ Domain      │  │ File Server         │ │
│  │ Firewall    │  │ Controller  │  │ Windows 2022        │ │
│  │             │  │ Win 2022    │  │                     │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
│                                                             │
│  Server VLAN (10.0.2.0/24)                                │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │ Web Server  │  │ Database    │  │ Monitoring          │ │
│  │ Ubuntu      │  │ Server      │  │ & Tools             │ │
│  │ NGINX       │  │ MySQL       │  │ Linux               │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
│                                                             │
│  Workstation VLAN (10.0.3.0/24)                           │
│  ┌─────────────┐  ┌─────────────┐                         │
│  │ Windows 11  │  │ Ubuntu      │                         │
│  │ Client      │  │ Workstation │                         │
│  └─────────────┘  └─────────────┘                         │
└─────────────────────────────────────────────────────────────┘

 
## 🛠️ Technology Stack

### **Infrastructure**
- **Hypervisor**: Proxmox VE 8.x
- **Firewall**: pfSense with VLAN segmentation
- **Windows**: Server 2022 (Domain Controller, File Server)
- **Linux**: Ubuntu 22.04 LTS (Web, Database, Tools)

### **Administration Tools**
- **Windows**: PowerShell, Group Policy, Active Directory
- **Linux**: Bash scripting, systemd, package management
- **Network**: VLAN configuration, firewall rules, DNS/DHCP
- **Custom Tools**: Go applications for system management

### **Services & Applications**
- **Directory Services**: Active Directory Domain Services
- **Web Services**: NGINX, IIS
- **Database**: MySQL, SQL Server Express
- **File Services**: DFS, Samba, NFS
- **Update Management**: WSUS, automated patching

---

## 📋 Project Components & Progress

### **Phase 1: Windows Domain Infrastructure** (Weeks 1-2)

#### Domain Controller Setup
- [ ] **Windows Server 2022 Installation**
  - [x] VM creation and base OS install
  - [ ] Static IP configuration (10.0.1.10)
  - [ ] Computer rename and domain preparation
  - [ ] Windows Updates and initial hardening

- [ ] **Active Directory Domain Services**
  - [ ] AD DS role installation
  - [ ] Forest creation (enterprise.lab)
  - [ ] DNS configuration and testing
  - [ ] Site and Services configuration

- [ ] **Organizational Unit Structure**
 enterprise.lab
├── Corporate
│   ├── Users
│   │   ├── Administrators
│   │   ├── IT Staff
│   │   ├── Sales Team
│   │   └── Marketing Team
│   ├── Computers
│   │   ├── Servers
│   │   ├── Workstations
│   │   └── Laptops
│   └── Service Accounts
└── Groups
├── Security Groups
└── Distribution Groups

 
- [ ] **User Management Implementation**
- [ ] User account creation and management
- [ ] Security group assignment
- [ ] Home folder creation automation
- [ ] Password policies and account lockout

#### File Server & Storage
- [ ] **File Services Configuration**
- [ ] File Server role installation
- [ ] Shared folder creation with proper permissions
- [ ] DFS namespace implementation
- [ ] Shadow copies configuration

- [ ] **Group Policy Management**
- [ ] Security policies implementation
- [ ] Software deployment policies
- [ ] User environment management
- [ ] Computer configuration policies

#### System Maintenance
- [ ] **Windows Update Services (WSUS)**
- [ ] WSUS server installation and configuration
- [ ] Client-side targeting setup
- [ ] Automatic approval rules
- [ ] Reporting and monitoring

- [ ] **Backup Strategy**
- [ ] Windows Server Backup configuration
- [ ] Scheduled backup jobs
- [ ] Backup verification scripts
- [ ] Disaster recovery documentation

### **Phase 2: Linux Systems Management** (Weeks 3-4)

#### Linux Server Deployment
- [ ] **Ubuntu Web Server**
- [ ] Ubuntu 22.04 installation and hardening
- [ ] NGINX installation and configuration
- [ ] SSL certificate implementation
- [ ] Log rotation and management

- [ ] **Database Server**
- [ ] MySQL installation and security configuration
- [ ] Database creation and user management
- [ ] Automated backup scripts
- [ ] Performance monitoring setup

#### System Administration
- [ ] **Package Management**
- [ ] Automated update scripts
- [ ] Security patch management
- [ ] Software installation procedures
- [ ] Repository management

- [ ] **Service Management**
- [ ] Systemd service configuration
- [ ] Service monitoring scripts
- [ ] Startup/shutdown procedures
- [ ] Failed service alerting

- [ ] **User & Security Management**
- [ ] Local user account management
- [ ] SSH key authentication setup
- [ ] Sudo policies configuration
- [ ] Security audit procedures

#### Integration with Windows Domain
- [ ] **Samba Integration**
- [ ] Samba installation and domain join
- [ ] File sharing with Windows clients
- [ ] Permission mapping and testing
- [ ] Authentication integration

### **Phase 3: Network Infrastructure** (Week 2 & Ongoing)

#### pfSense Firewall
- [ ] **pfSense Deployment**
- [ ] pfSense VM installation
- [ ] Interface configuration (WAN/LAN)
- [ ] VLAN creation and tagging
- [ ] Inter-VLAN routing rules

- [ ] **Security Implementation**
- [ ] Firewall rule creation
- [ ] Network segmentation testing
- [ ] VPN configuration (future)
- [ ] Intrusion detection setup

#### Network Services
- [ ] **DNS/DHCP Management**
- [ ] DHCP scope configuration
- [ ] DNS forwarder setup
- [ ] Static lease management
- [ ] Network troubleshooting procedures

### **Phase 4: Operations & Monitoring** (Weeks 5-6)

#### System Monitoring
- [ ] **Custom Monitoring Tools (Go)**
- [ ] System inventory collector
- [ ] Backup verification utility
- [ ] Security audit scanner
- [ ] Simple alerting system

- [ ] **Operations Dashboard**
- [ ] Web-based status dashboard
- [ ] System health indicators
- [ ] Recent activity logs
- [ ] Quick action buttons

#### Automation Scripts
- [ ] **Daily Operations**
- [ ] System health check scripts
- [ ] Automated maintenance tasks
- [ ] Report generation
- [ ] Log analysis automation

- [ ] **Incident Response**
- [ ] Common issue playbooks
- [ ] Troubleshooting procedures
- [ ] Escalation procedures
- [ ] Documentation templates

### **Phase 5: Documentation & Portfolio** (Weeks 7-8)

#### Professional Documentation
- [ ] **Operations Procedures**
- [ ] Daily/weekly/monthly checklists
- [ ] Incident response playbooks
- [ ] Change management procedures
- [ ] User onboarding/offboarding guides

- [ ] **Technical Documentation**
- [ ] Network diagram and IP assignments
- [ ] Service configuration details
- [ ] Backup and recovery procedures
- [ ] Security policies and procedures
---

## 🚀 Getting Started

### **Prerequisites**
- Proxmox VE 8.x installed and running
- Sufficient hardware (32GB RAM, 500GB storage recommended)
- Network+ and AWS Cloud Practitioner knowledge
- Basic PowerShell and Bash familiarity

### **Quick Start**
1. **Clone this repository**
 ```bash
 git clone https://github.com/yourusername/enterprise-sysadmin-lab.git
 cd enterprise-sysadmin-lab
 	2.	Follow the deployment guides
	▪	Windows Domain Setup 	▪	Linux Server Deployment 	▪	Network Configuration 	3.	Track progress using this README
	▪	Check off completed tasks 	▪	Document any deviations or issues 	▪	Update with lessons learned
📖 Documentation
	•	Architecture Guide - Detailed system design 	•	Deployment Guides - Step-by-step procedures 	•	Operations Runbooks - Daily operational tasks 	•	Troubleshooting - Common issues and solutions 	•	API Documentation - Custom tool APIs
---

## **How to Use This README** 📝

### **Progress Tracking:**
1. **Check off completed tasks** as you finish them
2. **Update status sections** with current progress
3. **Document lessons learned** in comments
4. **Add screenshots** to the portfolio section

### **Professional Benefits:**
- **Shows project management skills** to hiring managers
- **Demonstrates systematic approach** to complex projects
- **Provides talking points** for interviews
- **Creates portfolio narrative** of your capabilities


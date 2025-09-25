# Secure Hybrid Network Lab (Azure + Python SDK)
> **Secure Hybrid Network Lab** is a hands-on, automated project that simulates a hybrid cloud environment by connecting a local (on-premises) VM to an Azure Virtual Network (VNet) using a site-to-site VPN Gateway.  
All Azure resources are deployed and managed using the official **Azure Python SDK**, with teardown scripts for full lifecycle management.  
This project is designed to build and demonstrate real-world skills for cloud support and sysadmin roles, with a focus on secure networking, automation, and troubleshooting.


[![Project Status](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)](https://github.com/yourusername/secure-hybrid-network-lab)
[![Azure](https://img.shields.io/badge/Azure-Network-blue.svg)](https://azure.microsoft.com)
[![Linux](https://img.shields.io/badge/Linux-Ubuntu%2022.04-orange.svg)](https://ubuntu.com)
[![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-blue.svg)](https://www.microsoft.com/windows-server)
[![Network+](https://img.shields.io/badge/CompTIA-Network%2B-green.svg)](https://www.comptia.org/certifications/network)
[![Cloud Support](https://img.shields.io/badge/Cloud-Support%2FAdmin-important.svg)](https://learn.microsoft.com/en-us/azure/networking/)
[![Security](https://img.shields.io/badge/Security-Hardened-red.svg)](https://www.cisa.gov/uscert/bsi/articles/best-practices)

---

## Features

-  Automated deployment and teardown of Azure networking resources via Python SDK
-  Local VM setup guide for simulating on-premises infrastructure (Ubuntu 22.04 or Windows Server 2022)
-  Secure VPN connection between local VM and Azure VNet
-  Modular, well-documented code suitable for cloud support/admin portfolios
-  Optional Raycast integration for one-click operations

---

> **Status:** _In Progress_  
> **Target Audience:** Entry-level cloud support, sysadmin, and IT professionals building hands-on Azure networking and automation skills

---

## Features

-  Automated deployment and teardown of Azure networking resources
-  Step-by-step local VM setup for on-prem simulation
-  Secure VPN connection between local VM and Azure VNet
-  Raycast integration for one-click deployment (optional)

---

## Architecture

 [Local VM] <--VPN Tunnel--> [Azure VPN Gateway] <---> [Azure VNet/Subnet/VM]


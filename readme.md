# Windows File Server Lab

A Windows domain lab environment demonstrating Active Directory, DNS and a dedicated File Server providing centralized network storage and access control.

---

## Overview

**Domain:** `matrix.local`

### Systems

* **DC-01** — Domain Controller 
* **FS-01** — File Server 
* **CLIENT-01** — Domain Client 

---

## Network Configuration

### DNS Servers

All systems use the following DNS server:

* `192.168.178.199`

---

## Software Requirements

* VMware Workstation Pro
  https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion

* Windows Server 2022 Evaluation
  https://www.microsoft.com/en-gb/evalcenter/download-windows-server-2022

* Windows 10 Enterprise Evaluation
  https://www.microsoft.com/en-gb/evalcenter/download-windows-10-enterprise

---

## Objectives

* Deploy Active Directory Domain Services (AD DS)
* Configure DNS for domain services
* Join Windows clients to the domain
* Configure a dedicated File Server
* Create and manage SMB shares
* Implement NTFS and share permissions
* Map Network drives as a user.

---

## File Server Structure

### Shared Folders

```text
C:\Shares\Public
C:\Shares\Oracle
C:\Shares\Private
```

### Network Share

```text
\\FS01\Shares
```

---

## Security Model

### Active Directory

* User authentication
* Group-based access control
* Centralized identity management

### File Server (FS01)

* Shared storage management
* NTFS permissions
* Share permissions

### Group Policy

* Drive mapping
* User configuration
* Centralized policy management

---

## Documentation

* [DC Setup](DC-setup.md) – Active Directory and DNS configuration
* [File Server Setup](FS-setup.md) – SMB shares and permissions
* [Client Domain Join](client-join.md) – Joining Windows clients to the domain
* [Drive Mapping](client-map-drive.md) – Drive mapping configuration

---

## Lab Architecture

```text
matrix.local

DC-01      Domain Controller
FS-01      File Server
CLIENT-01  Domain Client
```

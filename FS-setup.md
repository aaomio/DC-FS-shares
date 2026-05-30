# File Server Setup (FS-01)

This guide covers configuration of **FS-01** as a domain-joined file server for the **matrix.local** environment.

---

## Configure Network Settings

Open Network Connections:

```text
Win + R
ncpa.cpl
```

Configure IPv4 settings:

```text
IP Address:      192.168.178.20
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.178.2
DNS Server:      192.168.178.199
```

---

## Configure Computer Name

Open System Properties:

```text
Win + R
sysdm.cpl
```

Rename the server:

```text
FS-01
```

Restart the system if prompted.

---

## Join the Domain

Open System Properties:

```text
sysdm.cpl
```

Join the domain:

```text
matrix.local
```

Authenticate using:

```text
matrix\Administrator
```

Restart the server after the domain join completes.

---

## Create Shared Folder Structure

```text
C:\Shares
C:\Shares\Public
C:\Shares\Oracle
C:\Shares\Private
```

---

## Configure File Share

Open:

```text
C:\Shares: Properties\Sharing\Advanced Sharing
```

Share name:

```text
Shares
```

Network path:

```text
\\FS-01\Shares
```

---

## Configure Permissions

### Share Permissions

* Domain Users: Read
* Domain Admins: Full Control

### NTFS Permissions

* Authenticated Users: Read
* Domain Admins: Full Control

---

## Access Test

From CLIENT-01:

* Open File Explorer
* Navigate to:

```text
\\FS-01\Shares
```

* Confirm access to shared folders


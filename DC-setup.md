# Domain Controller Setup (DC-01)

This guide covers the installation and configuration of Active Directory Domain Services (AD DS) on **DC-01** for the **matrix.local** domain.

---

## Configure Network Settings

Open Network Connections:

```text
Win + R
ncpa.cpl
```

Configure the IPv4 adapter settings:

```text
IP Address:      192.168.178.199
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.178.2
Preferred DNS:   192.168.178.199
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
DC-01
```

Restart the server if prompted.

---

## Install Active Directory Domain Services

1. Open **Server Manager**
2. Select **Add Roles and Features**
3. Choose **Role-based or feature-based installation**
4. Select **Active Directory Domain Services**
5. Install any required features when prompted
6. Complete the installation

---

## Promote Server to Domain Controller

After installation:

1. Select **Promote this server to a domain controller**
2. Choose **Add a new forest**
3. Enter the root domain name:

```text
matrix.local
```

4. Configure the Directory Services Restore Mode (DSRM) password
5. Complete the configuration wizard
6. Allow the server to restart

---

## Verify Active Directory

Open **Active Directory Users and Computers** and confirm:

* `matrix.local` exists
* DC-01 appears as a Domain Controller
* Default Organizational Units are present

---

## Verify DNS

Open Command Prompt and run:

```cmd
nslookup matrix.local
```

Expected result:

```text
Name:    matrix.local
Address: 192.168.178.199
```


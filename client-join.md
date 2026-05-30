# Windows 10 Client Domain Join (CLIENT01)

This guide covers joining **CLIENT01** to the **matrix.local** domain.

---

## Configure Network Settings

Open Network Connections:

```text
Win + R
ncpa.cpl
```

Configure the DNS server:

```text
Preferred DNS: 192.168.178.199
```

---

## Configure Computer Name

Open System Properties:

```text
Win + R
sysdm.cpl
```

Rename the computer:

```text
CLIENT01
```

Restart the system if prompted.

---

## Join the Domain

Open System Properties:

```text
sysdm.cpl
```

Select **Change** and join the following domain:

```text
matrix.local
```

Authenticate using a domain account:

```text
matrix\Administrator
```

Restart the system after the domain join completes.

---

## Verify Domain Membership

Open System Properties:

```text
sysdm.cpl
```

Confirm the following:

```text
Domain: matrix.local
```

---

## Verify in Active Directory

On **DC01**, open **Active Directory Users and Computers** and confirm:

* `CLIENT01` exists in the **Computers** container
* The computer account is enabled


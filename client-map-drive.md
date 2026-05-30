# Manual Drive Mapping (FS-01 Shares)

This document covers manual mapping of FS-01 shared folders on CLIENT-01.

---

## Shared Path

-01 share:

```text
\\FS-01\Shares
```

---

## Map Network Drive (GUI Method)

On CLIENT-01:

Open **File Explorer**.

Right-click **This PC**.

Select **Map network drive**.

Configure:

- **Drive letter:** `Z:`
- **Folder:** `\\FS-01\Shares`

Enable **Reconnect at sign-in**.

Click **Finish**.

---

## Map Network Drive (Command Method)

```cmd
Win + R
cmd
```

```cmd
net use Z: \\FS-01\Shares
```

---

## Persistent Mapping

```cmd
net use Z: \\FS-01\Shares /persistent:yes
```

---

## Remove Mapped Drive

```cmd
net use Z: /delete
```

---

## Notes

* Ensure DNS is resolving FS-01 correctly
* Verify share permissions if access fails

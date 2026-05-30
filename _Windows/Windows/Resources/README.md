# `[DRIVE]\Windows\Resources`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical, themes, cursors, and other UI resources
files to function properly and minimally without any mounting
(e.g. `[DRIVE]\Program Files` is not ready or absent).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Generally, you **SHOULD NOT** place any files in here unless you are a Microsoft
Windows OS developer.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

The structure is something like:

```
[DRIVE]\Windows\Resources\
  ...
```

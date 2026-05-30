# `[DRIVE]\Windows\System32\winevt\Logs`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical and distributor supplied
Windows Event Logs's log data files to enable the operating system (OS)
function properly and minimally without any mounting (e.g.
`[DRIVE]\Program Files` is not ready or absent).

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like facilitating
`[DRIVE]/Program Files` OS System Resources directories for functionalities
extension, performing self-rescue, or straight up operational in resources
constraint environment. The OS achieves *Minimum & Critical* stage when the
initialization is successful.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Generally, you **SHOULD NOT** place any files in here unless you are a Microsoft
Windows OS developer.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Microsoft Windows specifically designed its Windows Event Log's log data files.
Refer to OS distributor's documentations for specifications.

The internal structure is something like:

```
[DRIVE]\Windows\System32\winevt\Logs\
  ...
```

# `[DRIVE]\Windows\System32\DriverStore`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical and distributor trusted main
drivers repository installed into this operating system (OS) for "plug and play"
and rollpack purposes to function properly and minimally without any mounting
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

Microsoft Windows specifically designed its main drivers files bundles used by
its kernel in this directory. Refer to OS distributor's documentations for
specifications.

The internal structure is something like:

```
[DRIVE]\Windows\System32\DriverStore\
  c_battery_inf_amd64...\
    ...
  ...
```

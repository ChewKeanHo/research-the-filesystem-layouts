# `Users\[USERNAME]\AppData\Local\Temp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s user-specific,
 non-critical, temporary data files to function properly.

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
[DRIVE]\Windows\Temp\
  ...
```

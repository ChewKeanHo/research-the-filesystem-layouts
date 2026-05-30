# `[DRIVE]\System Volume Information`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s distributor supplied
non-critical hidden protected system folder Volume Shadow Copy (VSS) and
System Restore points data files. This directory appears on each drive's root
directory.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are visible but unavailable to all users.

Generally, you **SHOULD NOT** place any files in here and let the OS takes over.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

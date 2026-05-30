# `[DRIVE]\Windows\Boot`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing critical bootloading programs, applications,
and configuration files to bootstrap the operating system (OS) from hardware
using one or more bootloader type like Extensible Firmware Interface (EFI),
Unified Extensible Firmware Interface (UEFI), or (legacy) BIOS Grub bootloader.
This partition has specific rules where it **MUST** be the first readable
partition where a hardware is scanning its content for bootloader and has boot
flag enabled.

The goal is plain simple: boot up the OS with a hardware-software matching boot
configurations, initialize kernel until the OS can take over for achieving
`Minimal & Critical` functionalities stage.

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

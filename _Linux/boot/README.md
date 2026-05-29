# `/boot`

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

Generally, you **SHOULD ONLY** place bootloading programs and their
configuration files inside this directory. Due to early boot sequences are
hardware specific which can be very complex yet critical, this directory is
often housing the bootloading artifacts reliably and systematically generated
from the higher OS functionalities.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

No restrictions. It is all depending on the chosen bootloader (e.g. `U-Boot`,
`Grub`, etc), hardware, firmware, etc). Some bootloaders have strict partitions
setup, strict file names and pathing, stricts locations, and etc.

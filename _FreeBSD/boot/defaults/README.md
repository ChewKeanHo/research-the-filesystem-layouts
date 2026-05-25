# `/boot/defaults`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing default bootloader configuration files for
restoration purposes.

The goal is plain simple: factory-reset bootloader when it is always available.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD NOT** edit anything here. Only read and overwrite the
runtime version for restoration.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

No restrictions. It is all depending on the chosen bootloader (e.g. `U-Boot`,
`Grub`, etc), hardware, firmware, etc). Some bootloaders have strict partitions
setup, strict file names and pathing, stricts locations, and etc.

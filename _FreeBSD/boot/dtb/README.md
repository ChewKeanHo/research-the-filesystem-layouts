# `/boot/dtb`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing the compiled flattened device tree (FDT)
files using a device tree compiler (DTC). This is used to describe the hardware
abstraction layer (HAL) of a hardware.

The goal is plain simple: describe hardware using device tree.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** edit anything here. Only read and overwrite the
runtime version for restoration.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

No restrictions. It is all depending on the chosen DTC.

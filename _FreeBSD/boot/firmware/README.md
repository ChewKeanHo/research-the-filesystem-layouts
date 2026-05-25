# `/boot/firmware`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all the loadable binary firmware kernel
modules.

The goal is plain simple: enable and load the hardware with their specific
firmware.

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

Refer OS distributor for specifications.

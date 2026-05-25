# `/boot/loader.conf.d`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all bootloader configuration files using the
`.d` configuration directory pattern where 1 file is 1 configuration.

The goal is plain simple: to facilitate kernel module for hardware
initialization.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD NOT** edit anything here unless you are the FreeBSD
boodloader and kernel developer.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Accepted configuration can be both conventional `.conf` file or the new `.lua`
file.

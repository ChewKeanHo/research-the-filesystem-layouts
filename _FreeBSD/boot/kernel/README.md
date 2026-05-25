# `/boot/kernel`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all dynamic loadable FreeBSD kernel and
modules.

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

Refer OS distributor's documentations for specifications.

# `/etc/pkg`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s `pkg` package manager's
configuration file using the `.d` configuration directory pattern where 1 file
is 1 configuration. This means it can operate in `Single-User` mode in
BSD realm or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

FreeBSD practices the use of `/usr/local/etc` so use
`/usr/local/etc/pkg` instead. Therefore, generally, you **SHOULD NOT**
place or modify the configuration files that are very critical to the OS.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `pkg(8)` manual for specification.

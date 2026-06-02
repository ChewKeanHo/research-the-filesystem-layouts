# `/etc/periodic`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s cron scheduler's
periodic configuration directories. Each directory designates a periodic meaning
such as but not limited to `daily`, `weekly`, `monthy`, etc. Each directory
contains their respective cron files. It can operate minimally without any
mounting (e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

FreeBSD practices the use of `/usr/local/etc` so use `/usr/local/etc/periodic`
instead. Therefore, generally, you **SHOULD NOT** place or modify the
configuration files that are very critical to the OS.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `cron(8)` and `periodic(8)` manuals for specifications.

# `/usr/ports`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, operating system (OS)
distributor supplied, non-critical FreeBSD-specific Ports Collections workspaces
of an OS to function properly. This means it can operate in `Multi-User` mode in
BSD realm or `Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Minimum & Critical* stage to
*Full Catalogue* stage achieving full distributor-grade warranted capabilities.
All payloads, filepaths, configurations, data, etc. are strictly registered by
the OS distributor for achieving uniformity and consistency across ALL hardware
(fleet management).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way. Use `pkg` command instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `ports(7)` manual for specifications.

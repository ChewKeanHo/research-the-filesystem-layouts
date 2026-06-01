# `/proc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all process nodes (special files) of an
operating system (OS) to function properly and minimally without any mounting
(e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient `procfs` interface made available
enough for basic functionalities to perform critical tasks like mounting `/usr`
UNIX System Resources directory for OS capabilities extension, performing
self-rescue, or straight up being operational in this resources constraint
environment such as but not limited to OpenWRT embedded router.

This directory is now deprecated across all UNIX-based OSes but still
facilitated for backward compatibilities sake.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Linux-based OSes, the development is now shifted to `/sys`, `/run`, and for
some OS variant like Red Hat Linux or Fedora: `/srv` directories.

In FreeBSD, this directory can only be available when enabled. The OS disabled
it by default.

In Apple `MacOS`, this directory is unavailable.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `procfs(4)` manual for specifications.

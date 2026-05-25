# `/usr/freebsd-dist`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing FreeBSD distribution release files for
building a whole new FreeBSD operating system (OS). This directiory is
accessible system-wide, OS distributor supplied, non-critical programs and
applications to extend the OS' functionalities from *Critical & Minimal* stage
to *Full Catalogue* stage. This means it can operate in both `Multi-User` mode
in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All programs' and applications' names and
locations are registered by OS distributor. Therefore, they are available
consistently and uniformly across all the machines.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `release(7)` and `bsdinstall(8)` manuals.

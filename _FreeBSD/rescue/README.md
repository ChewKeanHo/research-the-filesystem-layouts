# `/rescue`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all programs, applications,
configurations, data files of an operating system (OS) to perform self-rescue
during `Single-User` mode in BSD realm.

The goal is to self-rescue the OS.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD ONLY** place files vital to perform the OS self-rescue
operation only.

In Linux-based OSes, this directory is unavailable.

In FreeBSD, this directory is used.

In Apple `MacOS`, this directory is unavailable.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `rescue(8)` manual for specifications.

# `/proc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all process nodes (special files). This
directory appears only when absolutely needed (e.g. FreeBSD enabling Linux
inter-compatibility layer which requires `/proc` to exist). On Linux, it is
always exist for backward compatibilities purposes.

The goal is simple: allow OS process filesystems (e.g. `procfs`) to map every
process files into filesystems for use.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `procfs(4)` manual for specifications.

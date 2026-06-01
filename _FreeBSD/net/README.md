# `/net`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all network-mounted network area storage
(NAS) and share drives. The first sub-directory is the network filesystem
server's label.

The purpose is to cater for one or more sharable network drive. Unlike `/media`,
this is mainly cater for network communication mediums.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is unused and is facilitated via its `/Network`
directory instead.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `auto_master(5)` manual for specifications.

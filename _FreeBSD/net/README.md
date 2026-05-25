# `/net`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all auto-mounted network area storage (NAS)
share drives. Its function is similar to `/media`. The first sub-directory is
the network filesystem server's label.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `auto_master(5)` manual for specifications.

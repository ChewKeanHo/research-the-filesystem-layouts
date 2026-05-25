# `/nonexistent`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all users that do not need a dedicated
`/home` directory.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

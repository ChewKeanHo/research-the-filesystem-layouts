# `/nonexistent`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a centralized user home data directory for users that do
not need a dedicated `/home` directory. Depending on the OS's engineering
specification, this directory can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **MUST NOT** place anything here **UNLESS ABSOLUTE NECESSARY**.
This is to avoid any conflict with the OS.

# `/etc/ssl/certs`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s OpenSSL's trusted
certificates store. It can readable in `Single-User` mode in BSD realm or
`Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place or modify anything here. Instead, place the
cert in `/usr/local/share/certs/trusted` and use `certctl(8)` to update the OS'
SSL certs archives.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `certctl(8)` manual for specifications and file directory structures.

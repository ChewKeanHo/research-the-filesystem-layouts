# `/compat/linux`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all cross Linux-based operating systems (OS)
programs, applications, and files.

The goal is simple: to facilitate Linux-based operating systems' (OS) programs,
applications, and files in this OS.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

You **SHOULD ONLY** place distributor's registered files in here only. The first
sub-directories layer denotes the origin OS.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

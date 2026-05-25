# `/dev/pts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all pseudo-terminal nodes.

The goal is simple: the operating system (OS) maps all the virtual terminal
nodes.

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

Refer `pts` manual for specifications.

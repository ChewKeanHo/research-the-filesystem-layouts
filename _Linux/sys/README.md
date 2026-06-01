# `/sys`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all Linux kernel's runtime query nodes
(special files) of an operating system (OS) to function properly.

The goal is simple: allowing Linux kernel to map its control surfaces into the
filesystems for use.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In any Linux-based OSes, the directory is available.

In FreeBSD, this directory is unused.

In Apple `MacOS`, this directory is unused.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

# `/sys`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all kernel, devices, drivers, and process
nodes (special files) for Linux kernel.

The goal is simple: allowing Linux kernel to map its control surfaces into the
filesystems for use.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentation for the device nodes
definitions.

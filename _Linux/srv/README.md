# `/srv`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all serving site-specific data of an
operating system (OS) to function properly. The goal is to provision network
services (e.g. FTP, WWW, CVS) for serving designated data files.

This directory is **ENTIRELY OPTIONAL** depending on the type of Linux-based
OSes. By default, it is absent. Only Ret Hat Linux is using this directory.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

In FreeBSD, this is unused.

In Linux-based OSes, this is mostly unused except Red Hat Linux OS.

In MacOS, this is unused.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

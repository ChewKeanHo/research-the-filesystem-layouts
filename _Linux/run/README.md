# `/run`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all runtime nodes (special files) of an
operating system (OS) to function properly and minimally without any mounting
(e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to provision an interface for querying and monitoring the OS runtime
status data.

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

In Linux-based OSes, many OSes are migrating the runtime `tmpfs` into this
directory mainly for reducing the total use of `tmpfs` counts. For supporting
backward compatibility, some OSes is symlinking this directory to `/var/run`
directory.

In MacOS, this is unused.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

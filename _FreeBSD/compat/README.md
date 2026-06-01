# `/compat`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing programs and applications of an
operating system (OS) capable of inter-operate other OSes functionalities to
function properly and minimally without any mounting
(e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is simple: to facilitate multiple operating systems' (OS) programs,
applications, and files in this OS.

The goal is to facilitate multiple OSes programs and applications capabilities
into this OS.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/bin` directory.

In Linux-based OSes, this directory is unused.

In Apple `MacOS`, this directory is unused.

You **SHOULD ONLY** place distributor's registered files in here only. The first
sub-directories layer denotes the origin OS.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

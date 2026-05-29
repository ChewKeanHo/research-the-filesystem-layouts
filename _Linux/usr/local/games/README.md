# `/usr/local/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical gaming programs and applications to extend
the OS' functionalities from *Critical & Minimal* stage to *Full Catalogue*
stage. This means it can operate in both `Multi-User` mode in BSD realm or
`Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All programs' and applications' names and
locations are registered by OS distributor. Therefore, they are available
consistently and uniformly across all the machines.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD** place your own custom programs and applications here.
It will be made available only for you.

This directory **MUST NOT** have any sub-directory.

In many Linux OSes like SystemD and UAPI, this directory is
**DEPRECATED AND REMOVED** in favor of using `/home/[USERNAME]/.local/games`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

# `/usr/libexec/lpr`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical, non-user, system-only, line printing
system's programs and applications to extend the OS' functionalities from
*Critical & Minimal* stage to *Full Catalogue* stage. This means it can operate
in both `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All programs' and applications' names and
locations are registered by OS distributor. Therefore, they are available
consistently and uniformly across all the machines.

All programs and applications here are **NOT AVAILABLE** as callable commands to
any user. Anyone can execute them via full filepath manually.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `lpr(1)` manual for specifications.

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

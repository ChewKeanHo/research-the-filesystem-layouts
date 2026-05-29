# `/usr/local/sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user's system-wide, custom supplied,
non-critical, system administrators (sysadmins) programs and applications to
extend the operating system (OS)'s functionalities from *Full Catalogue* stage
to *Complete* stage. This means it can operate in both `Multi-User` mode in BSD
realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities to its complete form by isolating
OS distributor's packages away from user's system-wide OS customizations. These
customizations, in theory, only specific to this machine instance.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are **ONLY** available to sysadmins (users in `wheel` group) and
`root` account.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

This directory **MUST NOT** have any sub-directory.

In many Linux OSes like SystemD and UAPI, this directory is
**DEPRECATED AND REMOVED** in favor of using `/home/[USERNAME]/.local/sbin`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

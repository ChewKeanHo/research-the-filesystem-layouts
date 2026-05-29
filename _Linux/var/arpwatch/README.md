# `/var/arpwatch`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `arpwatch` databases and
control files. Due to its processing nature, one **MUST** carefully work here to
prevent any data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage. In
Red Hat Linux, it is by default for arp spoofing monitoring.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `arpwatch` manual for specification.

# `/var/preserve`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) unused and presented for
historical reasons data files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is marked **AS RESERVED** by Linux's Filesystems
Standards (https://specifications.freedesktop.org/fhs/latest/varRequirements.html).
However, in practice, this directory is **OPTIONAL** depending on the runtime
OS uses and specifications.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to the OS distributor's documentations for specifications.

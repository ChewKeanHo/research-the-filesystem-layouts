# `/var/db/pkg`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) FreeBSD package database. Due
to its processing nature, one **MUST** carefully work here to prevent any data
poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Avoid using this directory to prevent OS-level fatal corruption.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's manual for specifications.

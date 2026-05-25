# `/var/log/cups`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses production log files from one or many programs' and
applications' runtime printing files and nodes across the entire operating
system (OS).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

It is best **NOT TO** place anything here and let the OS and CUPS take over
entirely.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `cups(1)` manual for specifications.

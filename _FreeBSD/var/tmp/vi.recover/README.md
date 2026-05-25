# `/var/tmp/vi.recover`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's temporary files and directory.
Unlike `/tmp` base directory, this temporary directory **GET PERSISTED (without
deletion on reboot)** enabling post booting forensic analytics use.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `vi(1)` manual for specifications.

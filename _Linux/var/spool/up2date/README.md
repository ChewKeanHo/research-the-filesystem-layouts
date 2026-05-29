# `/var/spool/up2date`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `.rpm` rollback data files
for `rpm`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `rpm` and `rpmbuild` manuals for specifications.

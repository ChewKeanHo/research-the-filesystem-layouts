# `[DRIVE]\PerfLogs`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s distributor supplied
non-critical Performance Monitor's and Data Collector Sets' system performance
reports and logs data files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Generally, you **SHOULD NOT** place any files in here unless you are a Microsoft
Windows OS developer.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

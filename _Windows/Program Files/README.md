# `[DRIVE]\Program Files`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide;
OS distributor supplied; non-critical; 64-bits programs, applications, and
software to extend the OS' functionalities from *Critical & Minimal* stage to
*Complete* stage.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD NOT** place any files in here unless you are a software
developer. Installed programs are housed in this directory. If you want
user-specific installation, use `C:\Users\%USERNAME%\AppData\Local\Programs`
instead.

This directory is accessible via the the following environment variables:

* `%PROGRAMFILES%`
* `%PROGRAMW6432%` (deprecated)




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each downstream directory in details. Once done, head over to
[`User's Local App Data`](/_Windows/Users/USERNAME/AppData/Local) directory
which is the next system-level layer for functionalities expansions.

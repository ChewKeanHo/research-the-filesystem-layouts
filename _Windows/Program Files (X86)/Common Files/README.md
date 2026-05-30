# `[DRIVE]\Program Files (x86)\Common Files`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide;
OS distributor supplied; non-critical; 32-bits shared libraries, frameworks, and
repositories' data files to extend the OS' functionalities from
*Critical & Minimal* stage to *Complete* stage.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

This directory is accessible via the the following environment variables:

* `%COMMONPROGRAMFILES(X86)%`




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

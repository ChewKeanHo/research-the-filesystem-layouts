# `[DRIVE]\Users\Public`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all users' data directory. Depending on the operating
system (OS)'s engineering specification, this directory can be
**ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to create, read, update, and delete
including all sysadmins and `root` accounts.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD** place your files here that are publicly accessible by
all users.

This directory is accessible via the the following environment variables:

* `%ALLUSERSPROFILE%`




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

For example, when this directory is further extended with [User](/User)
filesystems, it should have the following visible structure:

```
[DRIVE]\Users\Public\
  Desktop\
  Documents\
  Downloads\
  Pictures\
  Videos\
  Public\
  Music\
```

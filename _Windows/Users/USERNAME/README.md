# `[DRIVE]\Users\[USERNAME]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's data directory. Depending on the operating
system (OS)'s engineering specification, this directory can be
**ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
can access this directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here.

This directory is accessible via the the following environment variables:

* `%USERPROFILE%`
* `%HOMEPATH%`




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When this directory is further extended with [User](/User) filesystems, it
should have the following visible structure:

```
[DRIVE]\Users\[USERNAME]\
  Desktop\
  Documents\
  Downloads\
  Pictures\
  Videos\
  Public\
  Music\
```

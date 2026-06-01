# `[DRIVE]\Users\[USERNAME]\AppData\Local\Temp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s user-specific,
 non-critical, temporary data files to function properly.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place anything temporary here for data processing.
You are **STRONGLY RECOMMENDED** to remove the files before and after use for
preventing data file poisoning.

This directory is accessible via the the following environment variables:

* `%TEMP%`
* `%TMP%`




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

The structure is something like:

```
[DRIVE]\Users\[USERNAME]\AppData\Local\Temp\
  ...
```

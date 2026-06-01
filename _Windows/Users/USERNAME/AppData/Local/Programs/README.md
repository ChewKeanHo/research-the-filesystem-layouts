# `[DRIVE]\Users\[USERNAME]\AppData\Local\Programs`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s user-specific,
 non-critical, installed applications and programs to function properly.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD NOT** place anything here. Let the OS takes over
entirely.

This directory is accessible via the the following environment variables:

* `%LOCALAPPDATA%\Programs`




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

The structure is something like:

```
[DRIVE]\Users\[USERNAME]\AppData\Local\Programs\
  ...
```

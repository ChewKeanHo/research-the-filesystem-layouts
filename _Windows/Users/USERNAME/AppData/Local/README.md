# `[DRIVE]\Users\[USERNAME]\AppData\Local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's machine-specific data (e.g. local caches,
downloaded payloads) directory. Depending on the operating system (OS)'s
engineering specification, this directory can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
can access this directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD NOT** place anything here. Let the OS takes over
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

# `[DRIVE]\Users\[USERNAME]\AppData`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's data directory. Depending on the operating
system's engineering specification, this directory can be **ENTIRELY OPTIONAL**.

Unlike other user directories (e.g. `Desktop`), this directory is explicitly
hidden as internal operating data directory.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD NOT** place anything here. Let the OS takes over
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer OS distributor's documentations for specifications.

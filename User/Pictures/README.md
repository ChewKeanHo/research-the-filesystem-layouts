# `Pictures`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's images files. The initial design was to let the
user save all images in this directory. Expected files are `.png`, `.jpg`,
`.svg`, `.webp`, `.avif`, and etc.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## OS Deployment

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory was first spotted in the following OSes:

1. `FreeBSD`.
2. `Linux`-based OSes.
3. Apple's `MacOS`.
4. Microsoft `Windows`.
